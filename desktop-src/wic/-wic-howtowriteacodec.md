---
description: Esta seção de tópicos fornece aos desenvolvedores diretrizes sobre como implementar codecs de formato de arquivo de imagem que funcionarão dentro da estrutura WIC (Windows Imaging Component).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Como escrever um WIC-Enabled Codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e54339191626aefa8d6fb6cb53c88c9d2098d3e898e0805b796535323a9f98d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668123"
---
# <a name="how-to-write-a-wic-enabled-codec"></a>Como escrever um WIC-Enabled Codec

Esta seção de tópicos fornece aos desenvolvedores diretrizes sobre como implementar codecs de formato de arquivo de imagem que funcionarão dentro da estrutura WIC (Windows Imaging Component).

<dl>

[Introdução](-wic-howtowriteacodec-intro.md)  
[Como funciona o WIC (Windows de imagens)](-wic-howwicworks.md)  
<dl>

[Descoberta e mediação](-wic-howwicworks.md)  
[Decodificação](-wic-howwicworks.md)  
[Codificação](-wic-howwicworks.md)  
[O tempo de vida de um codec](-wic-howwicworks.md)  
[Como habilitar um Codec para WIC](-wic-howwicworks.md)  
[Suporte a apartments multi-threaded no WIC](-wic-howwicworks.md)  
</dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementando um WIC-Enabled decodificador</a><dl>

[Interfaces do decodificador](-wic-decoderinterfaces.md)<dl>

[Iwicbitmapdecoder](-wic-imp-iwicbitmapdecoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[Iwicbitmapsource](-wic-imp-iwicbitmapsource.md)  
[Iwicbitmapframedecode](-wic-imp-iwicbitmapframedecode.md)  
[Iwicmetadatablockreader](-wic-imp-iwicmetadatablockreader.md)  
[IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)  
[IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)  
</dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementando um codificador WIC-Enabled aplicativo</a>  
<dl>

[Interfaces do codificador](-wic-encoderinterfaces.md)  
<dl>

[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[Iwicbitmapframeencode](-wic-imp-iwicbitmapframeencode.md)  
[IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Instalação e registro do Codec</a>  
<dl>

[Registrando um Codec](-wic-codecinstallandreg.md)  
<dl>

[Entradas de Registro Geral](-wic-generalregentries.md)  
[Entradas do Registro específicas do codificador](-wic-encoderregentries.md)  
<dl>

[Registrando um formato de contêiner com autores de metadados](-wic-encoderregentries.md)  
</dl> </dd> <a href="-wic-decoderregentries.md">Entradas do Registro específicas do codificador</a>  
<dl>

[Registrando um novo formato de contêiner com leitores de metadados](-wic-decoderregentries.md)  
</dl> </dd> <a href="-wic-integrationregentries.md">Integração com Windows Vista PhotoGallery e Explorer</a>  
<dl>

[Windows Repositório de Propriedades](-wic-integrationregentries.md)  
[Windows Vista Galeria de Fotos](-wic-integrationregentries.md)  
[Windows Vista Thumbnail Cache](-wic-integrationregentries.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Atualizando o cache em miniatura ao instalar um codec</a> disponibilizando seu [WIC-Enabled codec para os](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">usuários</a>  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Introdução (Como escrever uma WIC-Enabled CODEC)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



