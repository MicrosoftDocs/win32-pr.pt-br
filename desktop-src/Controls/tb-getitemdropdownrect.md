---
title: Mensagem de TB_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtém o retângulo delimitador da janela suspensa para um item da barra de ferramentas com a \_ lista suspensa estilo BTNS.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- Controles de TB_GETITEMDROPDOWNRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008991"
---
# <a name="tb_getitemdropdownrect-message"></a>TB de \_ mensagem GETITEMDROPDOWNRECT

Obtém o retângulo delimitador da janela suspensa para um item da barra de ferramentas com a [**\_ lista suspensa estilo BTNS**](toolbar-control-and-button-styles.md).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O índice de base zero do item de controle Toolbar para o qual o retângulo delimitador será recuperado.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>Um ponteiro para uma estrutura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> para receber as informações do retângulo delimitador. O remetente da mensagem é responsável por alocar essa estrutura. As coordenadas retornadas na estrutura **Rect** são expressas como coordenadas do cliente.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sempre retorna zero.

## <a name="remarks"></a>Comentários

O item deve ter o [**estilo \_ suspenso BTNS**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

