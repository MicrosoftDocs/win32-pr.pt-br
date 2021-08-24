---
title: Mensagem de CBEM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- controles de Windows de mensagem de CBEM_INSERTITEM
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d9627efef4796554dfdbe1d7263747cc6b1c32b2cc00d5619a7cb7953024cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699297"
---
# <a name="cbem_insertitem-message"></a>\_Mensagem CBEM INSERTITEM

Insere um novo item em um controle ComboBoxEx.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que contém informações sobre o item a ser inserido. Quando a mensagem é enviada, o membro **iItem** deve ser definido para indicar o índice de base zero no qual inserir o item. Para inserir um item no final da lista, defina o membro **iItem** como-1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice no qual o novo item foi inserido, se for bem-sucedido, ou-1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CBEM \_ INSERTITEMW** (Unicode) e **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 





