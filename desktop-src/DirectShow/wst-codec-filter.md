---
description: Filtro de codec de WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtro de codec de WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297608"
---
# <a name="wst-codec-filter"></a>Filtro de codec de WST

> [!IMPORTANT]
> Este componente foi removido do Windows Vista e de sistemas operacionais posteriores. Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

A partir do Windows Vista, esse filtro é substituído pelo filtro VBICodec, que está documentado na documentação das tecnologias de TV da Microsoft.

O teletexto padrão mundial (WST) é o padrão europeu para transmissão de dados usando VBI em sinais de televisão analógicas da PAL. Tanto a legenda quanto os serviços de dados são fornecidos usando esse padrão. O codec de WST é um filtro de modo kernel que recebe exemplos VBI brutos e, opcionalmente, exemplos de telecódigo de telecodificação do filtro de captura por meio do filtro de [conversor de alto e Sink para coletor](tee-sink-to-sink-converter.md) . Esse codec decodifica e/ou duplica os dados de telecodificação e de encaminhamento de erros corrigidos para o filtro de [decodificador de WST](wst-decoder-filter.md) . O codec de WST corresponde ao filtro de decodificador de CC para transmissões NTSC. O decodificador de WST corresponde ao [decodificador de linha 21](line-21-decoder-filter.md) para NTSC; esses filtros criam os bitmaps que são enviados para o mixer de sobreposição ou o processador de mixagem de vídeo.

Esse filtro tem dois pinos de entrada, VBI e HWCC. O PIN do VBI é usado para dados brutos do VBI e o PIN do HWCC é usado quando a decodificação de VBI é executada no hardware pelo filtro de captura. Quando os dados são recebidos no PIN do HWCC, o codec de WST opera no modo de "passagem" e envia os dados diretamente para o decodificador de WST sem processá-los de forma alguma. Se o filtro de captura expõe um PIN HWCC, ele deve ser conectado diretamente ao PIN correspondente no codec de WST.

O filtro de codec de WST aparece na categoria de filtro "codecs VBI de streaming WDM" (**am \_ KSCATEGORY \_ VBICODEC**).

Como esse é um filtro de modo kernel, os aplicativos não podem criá-lo diretamente usando **CoCreateInstance**. Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md). Para obter mais informações, consulte [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> <dt>

[Exibindo teletexto do mundo Standard](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



