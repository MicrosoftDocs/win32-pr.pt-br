---
title: Fluxos de áudio
description: Fluxos de áudio
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Lojas online do Windows Media Player, fluxos de áudio
- lojas online, fluxos de áudio
- Digite 1 lojas online, fluxos de áudio
- Armazenamentos online do Windows Media Player, fluxos de servidores de música
- lojas online, fluxos de servidores de música
- Digite 1 lojas online, fluxos de servidores de música
- Lojas online do Windows Media Player, fluxos do servidor de música
- lojas online, fluxos de servidor de música
- tipos 1 lojas online, fluxos de servidor de música
- fluxos de áudio
- fluxos do servidor de música
- fluxos de servidores de música
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007137"
---
# <a name="audio-streams"></a>Fluxos de áudio

As lojas online podem fornecer música como um fluxo de um servidor de música. Isso é útil para fornecer exemplos, itens promocionais especiais ou para permitir que os usuários de assinatura desfrutem de música sem precisar baixar o conteúdo. É comum não armazenar a URL do fluxo como parte do catálogo de música, mas sim para resolver a URL logo antes da reprodução com base na ID da faixa. Para habilitar isso, o Windows Media Player chama [IWMPContentPartner:: GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) e fornece o tipo de streaming (como um valor de enumeração [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) ) e a ID do fluxo. O plug-in retorna a URL para o fluxo por meio do parâmetro *pbstrURL* .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o tipo 1 lojas online**](about-type-1-online-stores.md)
</dt> </dl>

 

 




