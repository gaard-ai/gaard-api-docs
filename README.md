# Gaard API documentation

- API server: [https://vision.gaard.ai](https://vision.gaard.ai)
- API documentation website [https://gaard.ai/docs](https://gaard.ai/docs)

## Work with API

To work with API you need `API_KEY`. Please contact us contact@gaard.ai to have access.

## Use scripts

Classification API is asynchronous. The general flow is to send video to classification and receive the result by calling `/result` endpoint or using webhook

Clone repository

```bash
git clone git@github.com:gaard-ai/gaard-api-docs.git
cd gaard-api-docs
```

Add `API_KEY` to environment variables

```bash
export API_KEY="YOUR API KEY"
```

### Post video

Usage

```bash
bin/post-video [video_path] [metadata_path]
```

Examples

```bash
bin/post-video
bin/post-video bin/video.mov
bin/post-video bin/video.mov
bin/post-video bin/video.mov bin/metadata.json
```

### Get results

Usage

```bash
bin/get-result classify_id
```

Example

```bash
bin/get-result 69c5488f6444fe27532566af
```

### Get Annotated video

Usage

```bash
bin/get-annotated-video classify_id
```

Example

```bash
bin/get-annotated-video 69c5488f6444fe27532566af
```

The output will be saved to `out.mp4`.

## Licenses

An example `bin/video.mov` is a part of [The VIRAT Video Dataset](https://viratdata.org/)
