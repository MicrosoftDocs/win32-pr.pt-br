---
title: Mensagem de PSM_GETTABCONTROL (Prsht. h)
description: Recupera o identificador para o controle guia de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTabControl PropSheet.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- Controles de PSM_GETTABCONTROL de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499624"
---
# <a name="psm_gettabcontrol-message"></a>Mensagem do PSM \_ GETtabcontrol

Recupera o identificador para o controle guia de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTabControl PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .

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

Retorna o identificador para o controle de guia.

## <a name="remarks"></a>Comentários

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





