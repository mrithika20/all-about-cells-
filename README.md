# CELL SEEDING CALCULATOR
Input: live cells from counter (side A & side B)
side_A_live = float(input("Enter live cell value from side A: "))
side_B_live = float(input("Enter live cell value from side B: "))

#finding the average
avg_live = (side_A_live + side_B_live) / 2

print("\n--- Cell Counting Result ---")
print(f"Average live value: {avg_live:.2f}")

#Seeding input/s
num_wells = int(input("\nEnter number of wells: "))
cells_per_well = float(input("Enter target cells per well: "))
final_volume_per_well = float(input("Enter final volume per well (mL): "))

#Calculation
cells_required = num_wells * cells_per_well
volume_needed_ml = cells_required / avg_live
total_final_volume = num_wells * final_volume_per_well
media_needed_ml = total_final_volume - volume_needed_ml

#Output
print("\nFinal Seeding Calculation: ")
print(f"Average live value: {avg_live:.2f}")
print(f"Total cells required: {cells_required:,.0f} cells")
print(f"Cell suspension needed: {volume_needed_ml:.3f} mL ({volume_needed_ml*1000:.1f} µL)")
print(f"Fresh media needed: {media_needed_ml:.3f} mL")
print(f"Total final volume: {total_final_volume:.3f} mL")
