  """
  This function sorts a list of numbers in ascending order using the bubble sort algorithm.

  Args:
    list_to_sort: A list of numbers to be sorted.

  Returns:
    A new list with the numbers sorted in ascending order.
  """
  # Create a copy of the list to avoid modifying the original
  sorted_list = list_to_sort.copy()
  n = len(sorted_list)

  # Iterate through the list n-1 times
  for i in range(n-1):
    # Flag to track if any swaps were made in a pass
    swapped = False
    # Iterate through the unsorted portion of the list
    for j in range(n-i-1):
      # Compare adjacent elements and swap if necessary
      if sorted_list[j] > sorted_list[j+1]:
        sorted_list[j], sorted_list[j+1] = sorted_list[j+1], sorted_list[j]
        swapped = True
    # If no swaps were made, the list is already sorted
    if not swapped:
      break

  # Return the sorted list
  return sorted_list

# Example usage
my_list = [1, 9, 5, 2, 1, 8, 6, 6, 3, 4, 10, 7]
sorted_list = sort_list(my_list)
print(sorted_list)  # Output: [1, 1, 2, 3, 4, 5, 6, 6, 7, 8, 9, 10]# Intra
[![Build Status](https://travis-ci.org/Jigsaw-Code/Intra.svg?branch=master)](https://travis-ci.org/Jigsaw-Code/Intra)

Intra is an experimental tool that allows you to test new DNS-over-HTTPS
services that encrypt domain name lookups and prevent manipulation by your
network. It currently supports services from Cloudflare and Google, and
additional options may be added over time.  You can get it from the
Google Play Store [here](https://play.google.com/store/apps/details?id=app.intra).

Features:
* Built-in support for public DNS services from Cloudflare and Google
* Visualization of server performance and application query behavior
* Geocoding of query results to compare against expected regional results

## Android build instructions

1. Clone this repo.
2. Open the `Android/` directory in Android Studio 3.2 or later.
3. Connect your phone
4. Click the green "play" triangle button.
