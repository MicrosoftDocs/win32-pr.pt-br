---
title: Mensagem de TB_CHECKBUTTON (commctrl. h)
description: Verifica ou desmarca um determinado botão em uma barra de ferramentas.
ms.assetid: e67734a9-851c-41ab-8ad7-15d434f58e5a
keywords:
- controles de Windows de mensagem de TB_CHECKBUTTON
topic_type:
- apiref
api_name:
- TB_CHECKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec35b6a333e0663acc8c94dec22c2b8f4138cb6024b1f7919fd0ec73cdb0eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919126"
---
# <a name="tb_checkbutton-message"></a>TB de \_ mensagem CHECKBUTTON

Verifica ou desmarca um determinado botão em uma barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de comando do botão a ser verificado.

</dd> <dt>

*lParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que indica se deve marcar ou desmarcar o botão especificado. Se for **true**, a verificação será adicionada. Se for **false**, a verificação será removida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Quando um botão é marcado, ele é exibido no estado pressionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

