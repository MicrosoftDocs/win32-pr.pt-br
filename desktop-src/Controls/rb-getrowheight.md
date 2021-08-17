---
title: Mensagem de RB_GETROWHEIGHT (commctrl. h)
description: Recupera a altura de uma linha especificada em um controle rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- controles de Windows de mensagem de RB_GETROWHEIGHT
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ac650fb50f1b6594964ec0bf10d23a8c8b6b75ff82e14af44bb63e2c9cf8af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409410"
---
# <a name="rb_getrowheight-message"></a>\_Mensagem RB GETalturadalinha

Recupera a altura de uma linha especificada em um controle rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero de uma banda. A altura da linha que contém a faixa especificada será recuperada.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **uint** que representa a altura da linha, em pixels.

## <a name="remarks"></a>Comentários

Para recuperar o número de linhas em um controle rebar, use a mensagem [**RB \_ GetRowCount**](rb-getrowcount.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





