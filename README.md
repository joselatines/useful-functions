# useful-functions
A repository to save useful functions that I created or found on internet or for personal projects

# Typescript
## Encrypt strings
```
import bcrypt from "bcrypt";

export const encrypt = async (query: string, salt = 10): Promise<string> => {
	const hashedPassword = await bcrypt.hash(query, salt);

	return hashedPassword;
};

export const compareEncrypted = async (
	queryEncrypted: string,
	query: string
): Promise<boolean> => {
	const isEqual = await bcrypt.compare(query, queryEncrypted);

	return isEqual;
};
 
```
