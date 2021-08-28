---
title: CB_LIMITTEXT mensagem (Winuser.h)
description: Limita o comprimento do texto que o usuário pode digitar no controle de edição de uma caixa de combinação.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT controles de Windows mensagem
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
ms.openlocfilehash: 3e94cdb1bedfb1c0aa3efb401649524782183ced7728304951596c9383efaa0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089076"
---
# <a name="cb_limittext-message"></a>Mensagem CB \_ LIMITTEXT

Limita o comprimento do texto que o usuário pode digitar no controle de edição de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número máximo de **TCHARs** que o usuário pode inserir, não incluindo o caractere nulo de terminação. Se esse parâmetro for zero, o comprimento do texto será limitado a 0x7FFFFFFE caracteres.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é sempre **TRUE.**

## <a name="remarks"></a>Comentários

Se a caixa de combinação não tiver o estilo [**CBS \_ AUTOHSCROLL,**](combo-box-styles.md) definir o limite de texto como maior que o tamanho do controle de edição não terá nenhum efeito.

A **mensagem CB \_ LIMITTEXT** limita apenas o texto que o usuário pode inserir. Ele não tem nenhum efeito sobre qualquer texto que já está no controle de edição quando a mensagem é enviada, nem afeta o comprimento do texto copiado para o controle de edição quando uma cadeia de caracteres na caixa de listagem é selecionada.

O limite padrão para o texto que um usuário pode inserir no controle de edição é de 30.000 **TCHARs.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

 





