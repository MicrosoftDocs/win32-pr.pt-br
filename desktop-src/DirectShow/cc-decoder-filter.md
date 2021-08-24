---
description: Filtro de decodificador de CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtro de decodificador de CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5feab764883754407030f2b4f72f794d049f5a394efb107ac149b10125da8d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757396"
---
# <a name="cc-decoder-filter"></a>Filtro de decodificador de CC

> [!IMPORTANT]
> este componente foi removido do Windows Vista e sistemas operacionais posteriores. ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.

 

O decodificador CC VBI é um filtro de classe de fluxo do modo kernel. Ele aparece em GraphEdit na categoria "codecs de VBI de streaming WDM". Ele aceita exemplos de onda fornecidos por um filtro de captura e entrega dados de legendas fechadas decodificados para a [linha 21 decodificador](line-21-decoder-filter.md) e/ou para aplicativos interessados.

Esse filtro tem dois pinos de entrada, VBI e HWCC. O PIN do VBI é usado para dados brutos do VBI e o PIN do HWCC é usado quando a decodificação de VBI é executada no hardware pelo filtro de captura. Quando os dados são recebidos no PIN do HWCC, o decodificador de CC opera no modo de "passagem" e envia os dados diretamente para o decodificador da linha 21 sem processá-los de forma alguma. Se o filtro de captura expõe um PIN HWCC, ele deve ser conectado diretamente ao PIN correspondente no decodificador CC. A categoria de PIN é a **\_ captura de vídeo \_ CC \_ do PINNAME**.

O decodificador CC tem até oito pinos de saída, cada um deles pode selecionar suas próprias linhas e subfluxos. O primeiro pino de saída é conectado ao decodificador de linha 21.

O filtro de decodificador de CC aparece na categoria de filtro "codecs de VBI de streaming WDM" (**am \_ KSCATEGORY \_ VBICODEC**).

Como esse é um filtro de modo kernel, os aplicativos não podem criá-lo diretamente usando **CoCreateInstance**. Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md). Para obter mais informações, consulte [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> <dt>

[Exibindo legendas ocultas](viewing-closed-captions.md)
</dt> </dl>

 

 



