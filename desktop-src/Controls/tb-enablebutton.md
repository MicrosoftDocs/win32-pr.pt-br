---
title: Mensagem de TB_ENABLEBUTTON (commctrl. h)
description: Habilita ou desabilita o botão especificado em uma barra de ferramentas.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- Controles de TB_ENABLEBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749306"
---
# <a name="tb_enablebutton-message"></a>TB de \_ mensagem ENABLEBUTTON

Habilita ou desabilita o botão especificado em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão a ser habilitado ou desabilitado.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que indica se o botão especificado deve ser habilitado ou desabilitado. Se for **true**, o botão será habilitado. Se for **false**, o botão será desabilitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Quando um botão é habilitado, ele pode ser pressionado e verificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

