---
title: PSM_GETTABCONTROL mensagem (Prsht.h)
description: Recupera o alça para o controle de tabulação de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTabControl do PropSheet.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- PSM_GETTABCONTROL controles de Windows mensagem
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
ms.openlocfilehash: 5b0e26c9489dc839383552b407a16313c94e1fc3b070d93f1d59ddaf0310134d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169656"
---
# <a name="psm_gettabcontrol-message"></a>Mensagem GETTABCONTROL do PSM \_

Recupera o alça para o controle de tabulação de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ GetTabControl do PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol)

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

Retorna o alça para o controle de tabulação.

## <a name="remarks"></a>Comentários

> [!Note]  
> Não há suporte para essa mensagem ao usar o estilo do assistente do Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





