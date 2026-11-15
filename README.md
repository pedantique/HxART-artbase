# HxART Artbase

This public repository is the versioned update feed for HxART. It contains no
application source code and no original working files.

The app checks `catalog.json` at launch, retains the last verified catalogue
offline and promotes an update only after every referenced asset passes its
SHA-256 check.

## Artwork protection

Artwork packages will be published as AES-256-GCM encrypted `.hxartpack`
objects rather than ordinary JPEG or PNG files. The initial Hannah collection
uses a key shipped inside the signed app. This prevents casual GitHub browsing,
hot-linking and ordinary image downloads, but it is not DRM: any picture an app
can display can ultimately be recovered by a determined person.

Future muse packs can use separate keys derived from long unlock codes. Entering
a code in HxART will store the derived key in the Apple Keychain and make that
muse's encrypted catalogue entries available. Codes should be high entropy;
short PINs are vulnerable to offline guessing because the encrypted packages
are public.

All artworks and metadata are copyright their respective owners. No licence is
granted to copy, redistribute or reuse them.

