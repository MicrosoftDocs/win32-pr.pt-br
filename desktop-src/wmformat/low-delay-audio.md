---
title: Low-Delay áudio
description: Low-Delay áudio
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- SDK do Windows Media Format, áudio de baixo atraso
- SDK do Windows Media Format, suporte a áudio
- codecs, áudio de baixo atraso
- codecs, suporte a áudio
- áudio de atraso baixo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761141"
---
# <a name="low-delay-audio"></a>Low-Delay áudio

O áudio de baixo atraso é um modo de codificação que produz áudio compactado com uma configuração de janela de buffer menor que outros modos. Isso é útil para fluxos que precisam ser alternados rapidamente durante a reprodução. O cenário típico para esse recurso é uma apresentação transmitida que inclui a capacidade de alternar arbitrariamente o conteúdo, como alterar o canal de uma televisão.

Quando você usa um formato de áudio de baixo atraso, a latência para alternar conteúdo é drasticamente reduzida em comparação com outros formatos de áudio. A latência também é reduzida para transmissões ao vivo quando você usa formatos de atraso baixo.

Esse recurso tem suporte dos codecs Windows Media áudio 9,1 e Windows Media Audio 9,1 Professional. Os formatos de atraso baixo estão disponíveis apenas para codificação de taxa de bits constante (uma e duas passagens).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos do codec**](codec-features.md)
</dt> </dl>

 

 




