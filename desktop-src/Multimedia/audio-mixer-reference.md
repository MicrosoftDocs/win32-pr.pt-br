---
title: Referência de Mixer áudio
description: Referência de Mixer áudio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- áudio multimídia, mixers de áudio
- áudio, mixers de áudio
- áudio multimídia, referência de mixer
- audio, referência de mixer
- mixers de áudio, referência
- mixers, referência
- referência para mixers de áudio, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1602a9ac0631a3e81430285c8cd862215a437c72b03b41d87fad6cefa7e41827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786216"
---
# <a name="audio-mixer-reference"></a>Referência de Mixer áudio

Esta seção descreve as funções, estruturas e mensagens associadas a mixers de áudio. Esses elementos são agrupados da seguinte forma.

## <a name="querying-devices"></a>Consultando dispositivos

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**Mixergetnumdevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Abertura e fechamento

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**Mixeropen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>Recuperando identificadores Mixer dados

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Recuperando controles de linha

-   [**Mixercontrol**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**Mixergetlinecontrols**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**Mixerlinecontrols**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Alterando atributos de controle

-   [**Mixercontroldetails**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS \_ BOOLEAN**](/previous-versions//dd757295(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ ASSINADO**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ UNSIGNED**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**Mixersetcontroldetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Recuperando informações de linha

-   [**Mixergetlineinfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**Mixerline**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**ALTERAÇÃO \_ DE CONTROLE DO MM \_ \_ MIXM**](mm-mixm-control-change.md)
-   [**ALTERAÇÃO DE LINHA DO MM \_ \_ \_ MIXM**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Enviando User-Defined mensagens

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Mixer áudio](audio-mixer-reference.md)
</dt> </dl>

 

 