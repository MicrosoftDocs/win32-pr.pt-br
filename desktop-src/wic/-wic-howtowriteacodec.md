---
description: Esta seção de tópicos fornece aos desenvolvedores orientações sobre como implementar codecs de formato de arquivo de imagem que funcionarão dentro da estrutura do Windows Imaging Component (WIC).
ms.assetid: 58f03dc2-cc31-4d76-b75a-f332da1f900f
title: Como escrever um codec de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee694d9a857781e97a31cb37f5ef18c518dae964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828605"
---
# <a name="how-to-write-a-wic-enabled-codec"></a>Como escrever um codec de WIC-Enabled

Esta seção de tópicos fornece aos desenvolvedores orientações sobre como implementar codecs de formato de arquivo de imagem que funcionarão dentro da estrutura do Windows Imaging Component (WIC).

<dl>

[Introdução](-wic-howtowriteacodec-intro.md)  
[Como funciona o Windows Imaging Component (WIC)](-wic-howwicworks.md)  
<dl>

[Descoberta e arbitragem](-wic-howwicworks.md)  
[Decodificação](-wic-howwicworks.md)  
[Codificação](-wic-howwicworks.md)  
[O tempo de vida de um codec](-wic-howwicworks.md)  
[Como habilitar um codec por WIC](-wic-howwicworks.md)  
[Suporte a multi-threaded apartment no WIC](-wic-howwicworks.md)  
</dl> </dd> <a href="-wic-implementingwicdecoder.md">Implementando um decodificador de WIC-Enabled</a><dl>

[Interfaces do decodificador](-wic-decoderinterfaces.md)<dl>

[IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)  
[IWICBitmapSource](-wic-imp-iwicbitmapsource.md)  
[IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)  
[IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)  
[IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)  
[IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)  
</dl> </dd> </dl> </dd> <a href="-wic-implementingwicencoder.md">Implementando um codificador de WIC-Enabled</a>  
<dl>

[Interfaces do codificador](-wic-encoderinterfaces.md)  
<dl>

[IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md)  
[IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)  
[IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md)  
[IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Instalação e registro de codec</a>  
<dl>

[Registrando um codec](-wic-codecinstallandreg.md)  
<dl>

[Entradas gerais de registro](-wic-generalregentries.md)  
[Entradas de registro específicas do codificador](-wic-encoderregentries.md)  
<dl>

[Registrando um formato de contêiner com gravadores de metadados](-wic-encoderregentries.md)  
</dl> </dd> <a href="-wic-decoderregentries.md">Entradas de registro específicas do codificador</a>  
<dl>

[Registrando um novo formato de contêiner com leitores de metadados](-wic-decoderregentries.md)  
</dl> </dd> <a href="-wic-integrationregentries.md">Integração com o Windows Vista galeria e o Explorer</a>  
<dl>

[Armazenamento de propriedades do Windows](-wic-integrationregentries.md)  
[Galeria de fotos do Windows Vista](-wic-integrationregentries.md)  
[Cache de miniaturas do Windows Vista](-wic-integrationregentries.md)  
</dl> </dd> </dl> </dd> <a href="-wic-codecinstallandreg.md">Atualizando o cache de miniaturas ao instalar um codec que</a> [torna o codec de WIC-Enabled disponível para os usuários](-wic-codecinstallandreg.md) </dl> </dd> <a href="-wic-howtowriteacodec-conclusion.md">concluir</a>  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Introdução (como escrever um CODEC de WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



