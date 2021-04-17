---
title: Mensagem de CBEM_INSERTITEM (commctrl. h)
description: Insere um novo item em um controle ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- Controles de CBEM_INSERTITEM de mensagens do Windows
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
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754811"
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

## <a name="return-value"></a>Retornar valor

Retorna o índice no qual o novo item foi inserido, se for bem-sucedido, ou-1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CBEM \_ INSERTITEMW** (Unicode) e **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 





