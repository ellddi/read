#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main()
{
    const int towns = 6;
    const int candidates = 5;
    int votes[towns][candidates];

    srand(time(0));

    for (int i = 0; i < towns; i++)
    {
        for (int j = 0; j < candidates; j++)
        {
            votes[i][j] = rand() % (10 * 22 + 50);
        }
    }

    cout << "Voting results:" << endl;
    cout << "\tCandidate 1\tCandidate 2\tCandidate 3\tCandidate 4\tCandidate 5" << endl;
    for (int i = 0; i < towns; i++)
    {
        cout << "Town " << i + 1 << "\t";
        for (int j = 0; j < candidates; j++)
        {
            cout << votes[i][j] << "\t\t";
        }
        cout << endl;
    }

    for (int t : {1, 4})
    {
        int maxVotes = votes[t][0], minVotes = votes[t][0];
        int maxCan = 0, minCan = 0;
        for (int j = 1; j < candidates; j++)
        {
            if (votes[t][j] > maxVotes)
            {
                maxVotes = votes[t][j];
                maxCan = j;
            }
            if (votes[t][j] < minVotes)
            {
                minVotes = votes[t][j];
                minCan = j;
            }
        }
        cout << "In Town " << t + 1 << ", Candidate " << maxCan + 1 << " has the most votes (" << maxVotes << "), and Candidate " << minCan + 1 << " has the least votes (" << minVotes << ")." << endl;
    }
    return 0;
}
