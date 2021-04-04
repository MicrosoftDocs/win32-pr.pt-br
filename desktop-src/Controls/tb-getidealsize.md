---
title: Mensagem de TB_GETIDEALSIZE (commctrl. h)
description: Obtém o tamanho ideal da barra de ferramentas.
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- Controles de TB_GETIDEALSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008994"
---
# <a name="tb_getidealsize-message"></a>TB de \_ mensagem GETIDEALSIZE

Obtém o tamanho ideal da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Um **bool** que indica se a altura ou a largura ideal da barra de ferramentas é recuperada. Use **true** para recuperar a altura ideal, **false** para recuperar a largura ideal.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) que recebe a altura ou largura na qual todos os botões seriam exibidos. Se *wParam* for **true**, somente o membro **CY** (Height) será válido. Se *wParam* for **false**, somente o membro **CX** (Width) será válido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

