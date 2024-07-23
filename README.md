## Hi there 👋

```go
package main

import (
	"fmt"
)

func devAdvice(project string, mood string) string {
	funEmojis := map[string]string{
		"enthusiastic": "🚀",
		"neutral":      "🛠️",
		"stuck":        "😓",
	}

	professionalAdvice := map[string]string{
		"enthusiastic": "Keep pushing forward and experimenting!",
		"neutral":      "Maintain focus and work steadily towards your goals.",
		"stuck":        "Take a break, review your approach, and seek help if needed.",
	}

	if _, moods := funEmojis[mood]; !moods {
		return "Invalid mood! Please choose between 'enthusiastic', 'neutral', or 'stuck'."
	}

	return fmt.Sprintf("Current project: %s %s. Advice: %s", project, funEmojis[mood], professionalAdvice[mood])
}

func main() {
	message := devAdvice("Build a new feature", "stuck")
	fmt.Println(message)
}
```
