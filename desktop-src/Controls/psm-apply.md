---
title: Mensagem de PSM_APPLY (Prsht. h)
description: Simula a seleção do botão aplicar, indicando que uma ou mais páginas foram alteradas e que as alterações precisam ser validadas e registradas.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- Controles de PSM_APPLY de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824636"
---
# <a name="psm_apply-message"></a>Mensagem de aplicação de PSM \_

Simula a seleção do botão **aplicar** , indicando que uma ou mais páginas foram alteradas e que as alterações precisam ser validadas e registradas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se todas as páginas forem aplicadas com êxito às alterações ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A folha de propriedades envia o código de notificação [PSN \_ KILLACTIVE](psn-killactive.md) para a página atual. Se a página atual retornar **false**, a folha de propriedades enviará o código de notificação [PSN \_ aplicar](psn-apply.md) a todas as páginas ativas. Você pode enviar a mensagem de PSM \_ Apply explicitamente ou usando a macro [**PropSheet \_ Apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





