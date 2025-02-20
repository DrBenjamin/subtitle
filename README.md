# Subtitle

Subtitle converter for transforming from srt format to vtt format.

## Converting

The srt will be transformed to vtt with this method:

```python
    buffer_vtt = io.StringIO()
    buffer_vtt.write("WEBVTT\n\n")
    for line in srt_file:
        if line.strip().isdigit():
            continue
        if "-->" in line:
            line = line.replace(",", ".")
        buffer_vtt.write(line)
```

## Usage

To run the Converter, use thiese two commands:

```bash
python -m pip install -r requirements.txt
python -m streamlit run app.py
```
