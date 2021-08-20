---
title: Mensagem de CBEM_GETITEM (commctrl. h)
description: Obtém informações de item para um determinado item ComboBoxEx.
ms.assetid: 2df07ae8-fa84-487c-a4a7-90244dfdb40e
keywords:
- controles de Windows de mensagem de CBEM_GETITEM
topic_type:
- apiref
api_name:
- CBEM_GETITEM
- CBEM_GETITEMA
- CBEM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcf4dadf72a9f1fab679599c01c8fd0c6ca3541f2f77a5e8c52a740828966034
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528056"
---
# <a name="cbem_getitem-message"></a>\_Mensagem CBEM GETITEM

Obtém informações de item para um determinado item ComboBoxEx.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) que recebe as informações do item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Quando a mensagem é enviada, os membros **iItem** e **Mask** da estrutura devem ser definidos para indicar o índice do item de destino e o tipo de informações a serem recuperadas. Outros membros são definidos conforme necessário. Por exemplo, para recuperar texto, você deve definir o \_ sinalizador de texto CBEIF em **Mask** e atribuir um valor a **cchTextMax**. Definir o membro **iItem** como-1 recuperará o item exibido no controle de edição.

Se o \_ sinalizador de texto CBEIF for definido no membro **Mask** da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) , o controle poderá alterar o membro **pszText** da estrutura para apontar para o novo texto em vez de preencher o buffer com o texto solicitado. Os aplicativos não devem pressupor que o texto sempre será colocado no buffer solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **CBEM \_ GETITEMW** (Unicode) e **CBEM \_ getitema** (ANSI)<br/>                 |



 

 





