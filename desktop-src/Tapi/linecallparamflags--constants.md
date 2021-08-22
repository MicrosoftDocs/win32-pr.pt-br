---
description: As constantes LINECALLPARAMFLAGS \_ descrevem vários sinalizadores de status sobre uma chamada.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: LINECALLPARAMFLAGS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fb33f662357b2e7e4d6b71b90e70aac1d8698a286de9da7f5e6a5b684712dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118863860"
---
# <a name="linecallparamflags_-constants"></a>Constantes LINECALLPARAMFLAGS \_

As **constantes LINECALLPARAMFLAGS \_** descrevem vários sinalizadores de status sobre uma chamada.

<dl> <dt>

<span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ BLOCKID**
</dt> <dd> <dl> <dt>



A identidade do originador deve ser ocultada (ID do chamador de bloco).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



O telefone da parte chamada deve ser retirado automaticamente.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ OCIOSO**
</dt> <dd> <dl> <dt>



A chamada deve ser originada em uma aparência de chamada ociosa e não ingressar em uma chamada em andamento. Ao usar a função [**lineMakeCall,**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) se o valor IDLE LINECALLPARAMFLAGS não estiver definido e houver uma chamada existente na linha, a função será interrompeda na chamada existente, se necessário, para fazer \_ a nova chamada. Se não houver nenhuma chamada existente, a função fará a nova chamada conforme especificado.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Esse bit é usado apenas em conjunto com [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) e [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference). O endereço a ser conferênciado com a chamada atual é especificado **no membro TargetAddress** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). A chamada de consulta não desenha fisicamente o tom de discagem da opção, mas progride por vários estados de estabelecimento de chamada (por exemplo, discagem, continuação). Quando a chamada de consultoria atinge o estado conectado, a conferência é estabelecida automaticamente; a chamada original, que permanecera no estado conectado, entra no estado conferênciado; a chamada de consultoria entra no estado conferência; o hConfCall entra no estado conectado. Se a chamada de consulta falhar (entra no estado desconectado seguido por ocioso), hConfCall também entra no estado ocioso e a chamada original (que pode ter sido uma conferência existente, no caso de **linePrepareAddToConference**) permanece no estado conectado. A parte original (ou partes) nunca percebe que a chamada foi reter. Esse recurso geralmente é usado para adicionar um supervisor a uma chamada de agente ACD quando necessário para monitorar interações com um chamador de taxa de iterações.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Esse bit é usado apenas em conjunto com [**lineSetupTransfer.**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer) Ele combina a operação de **lineSetupTransfer** seguida por [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) na chamada de consulta em uma única etapa. O endereço a ser discado é especificado no **membro TargetAddress** em [**LINECALLPARAMS.**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) A chamada original é colocada no estado *onholdpendingtransfer,* assim como se **lineSetupTransfer** fosse chamada normalmente e a chamada de consulta fosse estabelecida normalmente. O aplicativo ainda deve chamar [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para efetuar a transferência. Esse recurso geralmente é usado ao invocar uma transferência de um servidor por um link de controle de chamada de terceiros, pois esses links geralmente não são suportados pelo processo normal de duas etapas.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



O telefone do originador deve ser retirado automaticamente.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**
</dt> <dd> <dl> <dt>



Esse bit é usado somente ao fazer uma chamada em um endereço com a funcionalidade de discagem preditiva (LINEADDRCAPFLAGS PREDICTIVEDIALER está em no membro \_ **dwAddrCapFlags** [**em LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)). O bit deve estar ativado para habilitar o progresso da chamada aprimorado e/ou recursos de monitoramento de dispositivo de mídia do dispositivo. Se esse bit não estiver, a chamada será feita sem o progresso da chamada ou o monitoramento de tipo de mídia aprimorado e nenhuma transferência automática será iniciada com base no estado da chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ SECURE**
</dt> <dd> <dl> <dt>



A chamada deve ser configurada como segura.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Nenhuma extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**Linecallparams**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**Linecompletetransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**Linedial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**Linemakecall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**Lineprepareaddtoconference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**Linesetupconference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**Linesetuptransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




