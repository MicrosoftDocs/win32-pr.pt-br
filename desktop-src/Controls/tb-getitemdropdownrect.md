---
title: Mensagem de TB_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtém o retângulo delimitador da janela suspensa para um item da barra de ferramentas com a \_ lista suspensa estilo BTNS.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- controles de Windows de mensagem de TB_GETITEMDROPDOWNRECT
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
ms.openlocfilehash: ecd2dfc8a48ff735bfb8bcc99bc0baf36555eee9d995c3f453a95ea2910948a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918696"
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

## <a name="return-value"></a>Valor retornado

Sempre retorna zero.

## <a name="remarks"></a>Comentários

O item deve ter o [**estilo \_ suspenso BTNS**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

