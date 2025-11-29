# Dining Philosophers Simulator 🍽️

This project is a **visual, interactive simulation** of the **Dining Philosophers Problem** using **HTML, CSS, and JavaScript** for educational purposes. It helps you understand concurrency, deadlock, and starvation handling in the classic synchronization problem.

## Live Demo

> 🔗 **Deployed Link:**  
> [https://dining-philosopher-preemptive.vercel.app/](https://dining-philosopher-preemptive.vercel.app/)

## Features

✅ Visual circular layout with **5 philosophers and 5 forks**  
✅ Manual **buttons** to simulate philosophers taking and putting forks  
✅ **Color-coded states**:
- **Blue:** Thinking
- **Orange:** Hungry
- **Red:** Starving (>10s)
- **Green:** Eating  
✅ Fork color indicators (gray = available, red = in use)  
✅ **Starvation detection:** Automatically forces a philosopher to eat if waiting >10s  
✅ **Deadlock detection:** Detects and resolves deadlock automatically  
✅ Displays **wait time** for each philosopher when hungry

## How it works

- Each philosopher requires **two forks (left and right)** to eat.
- Uses a **mutex lock** (simulated in JavaScript) to prevent race conditions.
- Philosophers transition:
  - THINKING → HUNGRY → EATING → THINKING
- **Deadlock detection:** triggers if all philosophers are hungry and no forks are held.
- **Starvation detection:** forces eating if a philosopher has been hungry for >10 seconds.

## File Structure

This simulator is contained in a **single HTML file**:
- Inline CSS for styling
- JavaScript for the simulation logic
- Buttons for manual controls
- Circle layout visualization

## How to Run

1. Download or copy the `index.html` file.
2. Open it in your **web browser** (Chrome, Firefox, Edge).
3. Use the buttons to manually simulate philosophers taking and putting forks.
4. Observe the live state updates and automatic deadlock/starvation handling.

## Controls

- `Philosopher X take forks` – Attempt to pick up forks for Philosopher X.
- `Philosopher X put forks` – Put down forks for Philosopher X, returning to thinking.

## Visualization Details

- **Philosophers (P0–P4):** Positioned in a circle, each shows:
  - ID (e.g., `P0`)
  - Wait time (in seconds) when hungry
- **Forks (F0–F4):** Placed between philosophers, color indicates availability.

## Learning Objectives

✅ Understand **mutual exclusion, deadlock, and starvation** in concurrency.  
✅ Visualize the impact of neighbors on philosopher state transitions.  
✅ Observe how **deadlock and starvation are detected and resolved** in practice.

## Customization

- Adjust the number of philosophers by modifying the `N` constant and adding/removing philosopher and fork divs.
- Modify the starvation threshold (`10000` ms) to tune starvation detection.
- Extend with **automatic round-robin or random simulation logic** if desired.

## License

This project is provided for **educational and personal learning**.  
Feel free to modify, extend, or adapt for your OS, DBMS, or concurrency labs.
