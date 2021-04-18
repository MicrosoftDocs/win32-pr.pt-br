---
description: Encoder-Specific entradas do registro
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific entradas do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788777"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific entradas do registro


Além das entradas listadas acima para o codificador, você também deve registrar o codificador na categoria de codificadores do Windows Imaging Component (WIC) para que o mecanismo de descoberta possa encontrá-lo. Faça isso fazendo as seguintes entradas do registro. O primeiro GUID nas entradas a seguir é o identificador de categoria (CATID) para WICBitmapEncoders.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Registrando um formato de contêiner com gravadores de metadados

Se você criar um novo formato de contêiner para o codec, também deverá criar entradas de registro para dar suporte a gravadores de metadados para os blocos de metadados em suas imagens. As entradas a seguir precisam ser criadas no identificador de classe (CLSID) do gravador de metadados para cada formato de metadados com suporte em seu formato de contêiner. Se o seu codec usa um contêiner TIFF (Tagged Image File Format), essas informações já estão no registro e você não precisa criar essas entradas.

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

Se você usar um formato de contêiner TIFF ou estilo JPEG, deverá registrar uma associação entre o contêiner e esse formato de contêiner. Para obter mais informações, consulte a introdução em [integração com a Galeria de fotos do Windows e o Windows Explorer](-wic-integrationregentries.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Entradas gerais do registro](-wic-generalregentries.md)
</dt> <dt>

[Entradas de registro específicas do codificador](-wic-decoderregentries.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



