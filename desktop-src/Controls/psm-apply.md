---
title: PSM_APPLY mensagem (Prsht.h)
description: Simula a seleção do botão Aplicar, indicando que uma ou mais páginas foram alteradas e as alterações precisam ser validadas e registradas.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY controles Windows mensagem
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
ms.openlocfilehash: f753eb2465ec835f467493bdbd83d10b8ba174b11c83abffcb91d20f8beba002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544156"
---
# <a name="psm_apply-message"></a>Mensagem APPLY do PSM \_

Simula a seleção do botão **Aplicar,** indicando que uma ou mais páginas foram alteradas e as alterações precisam ser validadas e registradas.

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

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se todas as páginas aplicarem as alterações com êxito, caso **contrário, FALSE.**

## <a name="remarks"></a>Comentários

A folha de propriedades envia o [código de notificação \_ KILLACTIVE PSN](psn-killactive.md) para a página atual. Se a página atual retornar **FALSE,** a folha de propriedades enviará o código de notificação [ \_ PSN APPLY](psn-apply.md) para todas as páginas ativas. Você pode enviar a mensagem APPLY do PSM \_ explicitamente ou usando a [**macro PropSheet \_ Apply.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply)

> [!Note]  
> Não há suporte para essa mensagem ao usar o estilo do assistente do Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





