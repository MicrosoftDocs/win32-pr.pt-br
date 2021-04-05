---
title: Mensagem de CB_LIMITTEXT (WinUser. h)
description: Limita o comprimento do texto que o usuário pode digitar no controle de edição de uma caixa de combinação.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- Controles de CB_LIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009355"
---
# <a name="cb_limittext-message"></a>\_Mensagem de LIMITTEXT CB

Limita o comprimento do texto que o usuário pode digitar no controle de edição de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número máximo de **TCHARs** que o usuário pode inserir, não incluindo o caractere nulo de terminação. Se esse parâmetro for zero, o tamanho do texto será limitado a 0x7FFFFFFE caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é sempre **verdadeiro**.

## <a name="remarks"></a>Comentários

Se a caixa de combinação não tiver o estilo [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , definir o limite de texto como maior que o tamanho do controle de edição não terá nenhum efeito.

A mensagem **CB \_ LIMITTEXT** limita apenas o texto que o usuário pode inserir. Ele não tem nenhum efeito em nenhum texto que já esteja no controle de edição quando a mensagem é enviada, nem afeta o comprimento do texto copiado para o controle de edição quando uma cadeia de caracteres na caixa de listagem é selecionada.

O limite padrão para o texto que um usuário pode inserir no controle de edição é 30.000 **TCHARs**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

 





