---
description: As \_ constantes LINECALLFEATURE2 listam os recursos complementares disponíveis para conferência, transferência e chamadas de estacionamento.
ms.assetid: 67a3b587-dd5b-4ccf-ab69-2137604706b8
title: Constantes de LINECALLFEATURE2_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977e71f722fba34da6b2ecbd6a3e914c34a0aae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767744"
---
# <a name="linecallfeature2_-constants"></a>\_Constantes LINECALLFEATURE2

As **constantes \_ LINECALLFEATURE2** listam os recursos complementares disponíveis para conferência, transferência e chamadas de estacionamento.

<dl> <dt>

<span id="LINECALLFEATURE2_COMPLCALLBACK"></span><span id="linecallfeature2_complcallback"></span>**LINECALLFEATURE2 \_ COMPLCALLBACK**
</dt> <dd> <dl> <dt>



Se esse bit estiver ativado, o recurso de "retorno de chamada" poderá ser invocado usando a \_ opção de retorno de chamada LINECOMPLMODE com [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). O LINECALLFEATURE \_ COMPLETECALL bit também estará ativado no membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLCAMPON"></span><span id="linecallfeature2_complcampon"></span>**LINECALLFEATURE2 \_ COMPLCAMPON**
</dt> <dd> <dl> <dt>



Se esse bit for on, o recurso "Camp on" poderá ser invocado usando a \_ opção LINECOMPLMODE Camp com [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). O LINECALLFEATURE \_ COMPLETECALL bit também estará ativado no membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLINTRUDE"></span><span id="linecallfeature2_complintrude"></span>**LINECALLFEATURE2 \_ COMPLINTRUDE**
</dt> <dd> <dl> <dt>



Se esse bit for on, o recurso "intrusão" poderá ser invocado usando a \_ opção LINECOMPLMODE intruso com [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). O LINECALLFEATURE \_ COMPLETECALL bit também estará ativado no membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_COMPLMESSAGE"></span><span id="linecallfeature2_complmessage"></span>**LINECALLFEATURE2 \_ COMPLMESSAGE**
</dt> <dd> <dl> <dt>



Se esse bit estiver ativado, o recurso "deixar mensagem" poderá ser invocado usando a \_ opção de mensagem LINECOMPLMODE com [**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall). O LINECALLFEATURE \_ COMPLETECALL bit também estará ativado no membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_NOHOLDCONFERENCE"></span><span id="linecallfeature2_noholdconference"></span>**LINECALLFEATURE2 \_ NOHOLDCONFERENCE**
</dt> <dd> <dl> <dt>



Se esse bit estiver ativado, uma "nenhuma conferência de retenção" poderá ser criada usando a \_ opção LINECALLPARAMFLAGS NOHOLDCONFERENCE com [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference). O LINECALLFEATURE \_ SETUPCONF bit também estará ativado no membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_ONESTEPTRANSFER"></span><span id="linecallfeature2_onesteptransfer"></span>**LINECALLFEATURE2 \_ ONESTEPTRANSFER**
</dt> <dd> <dl> <dt>



Se esse bit estiver ativado, a "transferência de uma etapa" poderá ser criada usando a \_ opção LINECALLPARAMFLAGS ONESTEPTRANSFER com [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer). O LINECALLFEATURE \_ SETUPTRANSFER bit também estará ativado no membro **dwCallFeatures** .

> [!Note]  
> Se nenhum dos bits "COMPr" for especificado no membro **dwCallFeatures2** em [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , mas LINECALLFEATURE \_ COMPLETECALL for especificado, será possível que qualquer um deles funcione, mas o provedor de serviços não especificou que.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERCONF"></span><span id="linecallfeature2_transferconf"></span>**LINECALLFEATURE2 \_ TRANSFERCONF**
</dt> <dd> <dl> <dt>



Se esse bit for on, a função [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) poderá ser usada para resolver a transferência como uma conferência de três vias. O LINECALLFEATURE \_ COMPLETETRANSF bit também estará ativado no membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_TRANSFERNORM"></span><span id="linecallfeature2_transfernorm"></span>**LINECALLFEATURE2 \_ TRANSFERNORM**
</dt> <dd> <dl> <dt>



Se esse bit for on, a função [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) poderá ser usada para resolver a transferência como uma transferência normal. O LINECALLFEATURE \_ COMPLETETRANSF bit também estará ativado no membro **dwCallFeatures** .

> [!Note]  
> Se nem TRANSFERNORM nem TRANSFERCONF forem especificados no membro **dwCallFeatures2** em [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , mas LINECALLFEATURE \_ COMPLETETRANSF for especificado, será possível que ele funcione, mas o provedor de serviços não especificou que.

 


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKDIRECT"></span><span id="linecallfeature2_parkdirect"></span>**LINECALLFEATURE2 \_ PARKDIRECT**
</dt> <dd> <dl> <dt>



Se esse bit estiver ativado, o recurso "Parque direcionado" poderá ser invocado usando a \_ opção direcionada LINEPARKMODE com [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). O \_ bit LINECALLFEATURE Park também estará ativado no membro **dwCallFeatures** .


</dt> </dl> </dd> <dt>

<span id="LINECALLFEATURE2_PARKNONDIRECT"></span><span id="linecallfeature2_parknondirect"></span>**LINECALLFEATURE2 \_ PARKNONDIRECT**
</dt> <dd> <dl> <dt>



Se esse bit estiver ativado, o recurso "Parque não direcionado" poderá ser invocado usando a \_ opção não direcionada LINEPARKMODE com [**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark). O \_ bit LINECALLFEATURE Park também estará ativado no membro **dwCallFeatures** .

> [!Note]  
> Se nem PARKDIRECT nem PARKNONDIRECT forem especificados no membro **dwCallFeatures2** em [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) , mas \_ o parque LINECALLFEATURE for especificado, será possível que ele funcione, mas o provedor de serviços não especificou que.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**lineCompleteCall**](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)
</dt> <dt>

[**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[**linePark**](/windows/desktop/api/Tapi/nf-tapi-linepark)
</dt> <dt>

[**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)
</dt> <dt>

[**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> </dl>

 

 




