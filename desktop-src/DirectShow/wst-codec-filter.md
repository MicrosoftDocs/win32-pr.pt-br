---
description: Filtro codec do WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro codec do WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e729e13500317711076f6cdbd39c9a6ab25bea77e8d378e12f917f2e20e4a561
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083446"
---
# <a name="wst-codec-filter"></a>Filtro codec do WST

> [!IMPORTANT]
> Esse componente foi removido do Windows Vista e sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

A partir Windows Vista, esse filtro é substituído pelo filtro VBICodec, que está documentado na documentação da Microsoft TV Technologies.

O WST (World Standard Teletext) é o padrão europeu para transmissão de dados usando a VBI em sinais de tv análogo pal. Os serviços de legenda e dados são fornecidos usando esse padrão. O Codec do WST é um filtro de modo kernel que recebe exemplos brutos de VBI e, opcionalmente, exemplos de Teletext decodificados do Filtro de Captura por meio do filtro [Conversor Tee/Sink-to-Sink.](tee-sink-to-sink-converter.md) Esse codec decodifica e/ou duplica os dados teletextos decodificados e corrigidos por erro de encaminhamento para o filtro [de decodificador WST.](wst-decoder-filter.md) O Codec do WST corresponde ao filtro do Decodificador CC para transmissões NTSC. O Decodificador WST corresponde ao [Decodificador de Linha 21](line-21-decoder-filter.md) para NTSC; esses filtros criam os bitmaps que são enviados para o Mixer sobreposição ou para o Renderador de Combinação de Vídeo.

Esse filtro tem dois pinos de entrada, VBI e HWCC. O pin da VBI é usado para dados brutos da VBI e o pin HWCC é usado quando a decodificação da VBI é executada em hardware pelo filtro de captura. Quando os dados são recebidos no pin HWCC, o Codec do WST opera no modo de "passagem" e envia os dados diretamente para o Decodificador WST sem processá-los de nenhuma maneira. Se o filtro de captura expõe um pino HWCC, ele deve ser conectado diretamente ao pino correspondente no Codec do WST.

O filtro Codec do WST aparece na categoria de filtro "Codecs de VBI de Streaming do WDM" (**AM \_ KSCATEGORY \_ VMCDEC**).

Como esse é um filtro de modo kernel, os aplicativos não podem criar diretamente usando **CoCreateInstance**. Em vez disso, use [o Enumerador de Dispositivo do Sistema](system-device-enumerator.md). Para obter mais informações, consulte [Criando Kernel-Mode filtros](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Exibindo o World Standard Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



