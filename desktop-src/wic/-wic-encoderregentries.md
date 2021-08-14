---
description: Encoder-Specific entradas do Registro
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific entradas do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d5d91d917be3940bcece4bed7c224e0f281dbb1cade5d0dc2c25872f89af93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711225"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific entradas do Registro


Além das entradas listadas acima para o codificador, você também deve registrar seu codificador na categoria de codificadores WIC (Windows Imaging Component) para que o mecanismo de descoberta possa encontrá-lo. Faça isso fazendo as seguintes entradas do Registro. O primeiro GUID nas entradas a seguir é o CATID (identificador de categoria) para WICBitmapEncoders.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Registrando um formato de contêiner com autores de metadados

Se você criar um novo formato de contêiner para seu codec, também deverá criar entradas do Registro para dar suporte a autores de metadados para os blocos de metadados em suas imagens. As entradas a seguir precisam ser criadas sob o CLSID (identificador de classe) do autor de metadados para cada formato de metadados com suporte no formato de contêiner. Se o codec usar um contêiner TIFF (Formato de Arquivo de Imagem Marcada), essas informações já estão no Registro e você não precisa criar essas entradas.

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

Se você usar um formato de contêiner no estilo TIFF ou JPEG, deverá registrar uma associação entre o contêiner e esse formato de contêiner. Para obter mais informações, consulte a introdução em [Integração com Windows Galeria de Fotos e Windows Explorer](-wic-integrationregentries.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Entradas gerais do Registro](-wic-generalregentries.md)
</dt> <dt>

[Entradas do Registro específicas do codificador](-wic-decoderregentries.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



