---
title: Mensagem de PSM_UNCHANGED (Prsht. h)
description: Informa uma folha de propriedades que as informações em uma página foram revertidas para o estado salvo anteriormente. Você pode enviar essa mensagem explicitamente ou usando a \_ macro inalterada PropSheet.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- Controles de PSM_UNCHANGED de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163617"
---
# <a name="psm_unchanged-message"></a>Mensagem de PSM \_ INalterada

Informa uma folha de propriedades que as informações em uma página foram revertidas para o estado salvo anteriormente. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ inalterada PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador para a página que foi revertida para o estado salvo anteriormente.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A folha de propriedades desabilita o botão **aplicar** se nenhuma outra página tiver registrado alterações com a folha de propriedades.

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





