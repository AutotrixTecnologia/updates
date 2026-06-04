# AutoManager Agent Updates

Repositório público de distribuição do AutoManager Agent.

Este repositório é utilizado exclusivamente para publicar artefatos oficiais de atualização do AutoManager Agent, incluindo instaladores MSI, arquivos de verificação SHA256, manifests e notas de release.

## Objetivo

O objetivo deste repositório é servir como ponto público e estável para download das versões oficiais do AutoManager Agent utilizadas pelo mecanismo de atualização automática.

O código-fonte do agente não deve ser publicado neste repositório. Este repositório deve conter apenas artefatos de distribuição.

## Estrutura recomendada de releases

As versões devem ser publicadas usando GitHub Releases, seguindo o padrão de tag:

```text
v3.0.6
v3.0.7
v3.1.0
```

Cada release deve conter, no mínimo:

```text
AutoManagerAgent-<versao>.msi
AutoManagerAgent-<versao>.sha256.txt
```

Exemplo:

```text
AutoManagerAgent-3.0.6.msi
AutoManagerAgent-3.0.6.sha256.txt
```

## Validação SHA256

O arquivo `.sha256.txt` deve conter o hash SHA256 do instalador MSI correspondente.

Exemplo:

```text
6C42ED6DEBB60401A9DBA81D4E307E1ED056CF53BA7912C44B3DC90513891F2B  AutoManagerAgent-3.0.6.msi
```

O backend de atualização deve entregar ao agente o hash SHA256 real no campo `sha256`, não a URL do arquivo `.sha256.txt`.

## URL padrão de download

O padrão de URL dos instaladores publicados neste repositório é:

```text
https://github.com/AutotrixTecnologia/updates/releases/download/v<versao>/AutoManagerAgent-<versao>.msi
```

Exemplo:

```text
https://github.com/AutotrixTecnologia/updates/releases/download/v3.0.6/AutoManagerAgent-3.0.6.msi
```

## Aviso

Os arquivos publicados neste repositório são destinados exclusivamente à distribuição oficial do AutoManager Agent pela Autotrix Tecnologia.
