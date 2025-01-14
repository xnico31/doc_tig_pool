# How TIG Pool Works

The TIG Pool connects the computational power of miners, allowing them to share the rewards of collective efforts. Since the transition to **TIG V2**, the number of unique benchmarkers has significantly decreased due to the increasing difficulty of challenges. Mining pools have become, and will increasingly be, essential for continuing mining on TIG.

---

## Balancing

The pool dynamically manages nonce balancing per challenge for you. This ensures optimal performance without requiring any configuration on your part.

- You can view this balancing in the **[TIGSTAT](https://tigstats.com/benchmarkers/0x8bc5ee3c32c3e7d53fcde11cd22b5bf855acebec){:target="_blank"}** statistics.
- At every benchmark, the pool adjusts to the most optimal pre-commit values, ensuring efficient and accurate mining results.

---

## Self-Deposit

The pool performs self-deposits using TIG staked by **Stellar** and **Nova** users.

- You can access the history of active self-deposits directly from your dashboard.
- Without these self-deposits, the pool would not be able to mine.
- For more details, refer to the **[TIG Cutoff Documentation](#)**, which explains the cutoff principle.

---

## Algorithm Selection

TIG Pool features its own algorithm selection mechanism that allows for quick and dynamic adjustments when new rounds start.

- This proprietary system automatically switches to the most effective algorithm, giving the pool a significant advantage in benchmarking.

---

## Idle Phase

For **Nova profiles**, there may be idle phases during which mining on the primary pool is paused (no rewards). However, this does not mean your machines stop working.

- During idle phases, your machines contribute to the pool's **strategic operations**, mining on a different address.
- The rewards generated on this address are allocated to the **moderation team**, which uses them for events like games and airdrops.
- The data for this address will be visible in the dashboard.

### Key Details:

- At least **5% of Nova accounts** will always be in idle mode to maintain a substantial reserve of power for background strategies.
- **Stellar and Titan profiles** are not affected by idle phases and experience uninterrupted mining.
- The percentage of Nova accounts in idle mode is dynamically adjusted based on the pool’s available power.

### Example:

If the pool reaches its cutoff limit due to self-deposits, additional computational power will not benefit mining. In this case, the percentage of Nova accounts in idle mode will increase to prevent rewards from being diluted for accounts that have staked TIG to mine.

---

## Titan Bonus Reward  

As explained in **[#Plans](#)**, Titan profile users benefit from a bonus reward directly linked to their **Titan investment**.

### Mechanism  

- The bonus is tied to the percentage of **Nova profiles** present in the pool.  
- A portion of the fees collected on Nova rewards is redistributed to Titan users.  
- **APY Information:**  
  - For the last round, the APY was **XX%**.  
  - The more Nova machines there are in the pool, the higher the APY for Titan users will be.  

This mechanism ensures that Titan investors receive significant benefits for their contributions to the pool's operations.  

---

## Upcoming Feature: Idle Percentage Gauge

To enhance transparency and user experience, we are developing a new feature for the dashboard:

- **Idle Percentage Gauge:** This gauge will display the current percentage of Nova accounts in idle mode, allowing miners to monitor pool activity in real-time.

Stay tuned for this upcoming enhancement!

---

By leveraging these innovative mechanisms, TIG Pool ensures an efficient, fair, and seamless mining experience for all its users.

Happy mining with TIG Pool! 🚀
