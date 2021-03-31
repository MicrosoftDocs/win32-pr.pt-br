---
title: Referência do mixer de áudio
description: Referência do mixer de áudio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- áudio de multimídia, mixers de áudio
- áudio, mixers de áudio
- áudio de multimídia, referência de mixer
- áudio, referência de mixer
- mixers de áudio, referência
- mixers, referência
- referência para mixers de áudio, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104162240"
---
# <a name="audio-mixer-reference"></a>Referência do mixer de áudio

Esta seção descreve as funções, as estruturas e as mensagens associadas aos mixers de áudio. Esses elementos são agrupados da seguinte maneira.

## <a name="querying-devices"></a>Consultando dispositivos

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Abrindo e fechando

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>Recuperando identificadores do mixer

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Recuperando controles de linha

-   [**MIXERCONTROL**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Alterando atributos de controle

-   [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS \_ booliano**](/previous-versions//dd757295(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ assinado**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ não assinado**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Recuperando informações de linha

-   [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**MIXER**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**\_alteração de \_ controle de MIXM mm \_**](mm-mixm-control-change.md)
-   [**\_alteração de \_ linha \_ MIXM mm**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Enviando mensagens de User-Defined

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do mixer de áudio](audio-mixer-reference.md)
</dt> </dl>

 

 