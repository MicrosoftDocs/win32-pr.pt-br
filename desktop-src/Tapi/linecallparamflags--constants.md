---
description: As \_ constantes LINECALLPARAMFLAGS descrevem vários sinalizadores de status sobre uma chamada.
ms.assetid: f323ec9f-5bab-4b5d-93ef-8a552ee0d591
title: Constantes de LINECALLPARAMFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e70fe2721e6fce0ac509b50290b1ec3788f3c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781041"
---
# <a name="linecallparamflags_-constants"></a>\_Constantes LINECALLPARAMFLAGS

As **constantes \_ LINECALLPARAMFLAGS** descrevem vários sinalizadores de status sobre uma chamada.

<dl> <dt>

<span id="LINECALLPARAMFLAGS_BLOCKID"></span><span id="linecallparamflags_blockid"></span>**LINECALLPARAMFLAGS \_ blockid**
</dt> <dd> <dl> <dt>



A identidade do originador deve ser ocultada (bloquear ID do chamador).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_DESTOFFHOOK"></span><span id="linecallparamflags_destoffhook"></span>**LINECALLPARAMFLAGS \_ DESTOFFHOOK**
</dt> <dd> <dl> <dt>



O telefone da parte chamada deve ser feito automaticamente offhook.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_IDLE"></span><span id="linecallparamflags_idle"></span>**LINECALLPARAMFLAGS \_ ocioso**
</dt> <dd> <dl> <dt>



A chamada deve ser originada em uma aparência de chamada ociosa e não se associar a uma chamada em andamento. Ao usar a função [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) , se o \_ valor ocioso de LINECALLPARAMFLAGS não for definido e houver uma chamada existente na linha, a função será interrompida na chamada existente, se necessário, para fazer a nova chamada. Se não houver nenhuma chamada existente, a função fará a nova chamada como especificado.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_NOHOLDCONFERENCE"></span><span id="linecallparamflags_noholdconference"></span>**LINECALLPARAMFLAGS \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Esse bit é usado somente em conjunto com [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference) e [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference). O endereço a ser conferência com a chamada atual é especificado no membro **targetAddress** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). A chamada de consulta não desenha fisicamente o tom de discagem do comutador, mas irá progredir por meio de vários Estados de estabelecimento de chamada (por exemplo, discagem, continuação). Quando a chamada de consulta atinge o estado conectado, a conferência é automaticamente estabelecida; a chamada original, que permanecia no estado conectado, entra no estado de conferência; a chamada de consulta entra no estado de conferência; o hConfCall entra no estado conectado. Se a chamada de consulta falhar (entra no estado desconectado seguido por ociosidade), o hConfCall também entrará no estado ocioso e a chamada original (que pode ter sido uma conferência existente, no caso de **linePrepareAddToConference**) permanecerá no estado conectado. A parte original (ou partes) nunca percebe que a chamada tem ficado em espera. Esse recurso é frequentemente usado para adicionar um supervisor a uma chamada do agente ad quando necessário para monitorar as interações com um chamador irate.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ONESTEPTRANSFER"></span><span id="linecallparamflags_onesteptransfer"></span>**LINECALLPARAMFLAGS \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Esse bit é usado somente em conjunto com [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). Ele combina a operação de **lineSetupTransfer** seguida por [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) na chamada de consulta em uma única etapa. O endereço a ser discado é especificado no membro **targetAddress** em [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams). A chamada original é colocada no estado *onHoldPendingTransfer* , assim como se **lineSetupTransfer** fosse chamado normalmente, e a chamada de consulta é estabelecida normalmente. O aplicativo ainda deve chamar [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) para efetivar a transferência. Esse recurso é geralmente usado ao invocar uma transferência de um servidor por meio de um link de controle de chamada de terceiros, pois esses links geralmente não dão suporte ao processo normal de duas etapas.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_ORIGOFFHOOK"></span><span id="linecallparamflags_origoffhook"></span>**LINECALLPARAMFLAGS \_ ORIGOFFHOOK**
</dt> <dd> <dl> <dt>



O telefone do originador deve ser feito automaticamente offhook.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_PREDICTIVEDIAL"></span><span id="linecallparamflags_predictivedial"></span>**LINECALLPARAMFLAGS \_ PREDICTIVEDIAL**
</dt> <dd> <dl> <dt>



Esse bit é usado somente quando se faz uma chamada em um endereço com capacidade de discagem preditiva (LINEADDRCAPFLAGS \_ PREDICTIVEDIALER está on no membro **DwAddrCapFlags** no [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)). O bit deve estar ativado para habilitar o andamento da chamada avançada e/ou os recursos de monitoramento do dispositivo de mídia do dispositivo. Se esse bit não estiver ativado, a chamada será colocada sem um progresso de chamada avançado ou monitoramento de tipo de mídia, e nenhuma transferência automática será iniciada com base no estado da chamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARAMFLAGS_SECURE"></span><span id="linecallparamflags_secure"></span>**LINECALLPARAMFLAGS \_ seguro**
</dt> <dd> <dl> <dt>



A chamada deve ser configurada como segura.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




