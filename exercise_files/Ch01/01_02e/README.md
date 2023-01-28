# Add TypeScript to an existing solution

## Add the TypeScript compiler dependency
- `npm install typescript --save-dev`

## Run the TypeScript compiler
- `npx tsc`

## Configure the TypeScript compiler settings

- `outDir` where to put generated files
- `target` target JS version (`esnext` is the highest version supported by installed TypeScript version)
- `noEmit` toggle emitting files (false means don't emit anything just run the compiler to check types)
- `include` the path where files exist to be compiled

```bash
cat << EOF > tsconfig.json
{
    "compilerOptions": {
        "outDir": "build",
        "target": "esnext",
        "noEmit": true
    },
    "include": ["src/**/*"]
}
EOF
```
