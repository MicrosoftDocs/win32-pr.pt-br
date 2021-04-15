---
title: Mensagem de EM_GETLINECOUNT (WinUser. h)
description: Obtém o número de linhas em um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Controles de EM_GETLINECOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454764"
---
# <a name="em_getlinecount-message-winuserh"></a>Mensagem de EM_GETLINECOUNT (WinUser. h)

Obtém o número de linhas em um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um número inteiro que especifica o número total de linhas de texto no controle de edição de várias linhas ou no controle de edição com formato. Se o controle não tiver texto, o valor de retorno será 1. O valor de retorno nunca será menor que 1.

## <a name="remarks"></a>Comentários

A mensagem em **\_ GETLINECOUNT** recupera o número total de linhas de texto, não apenas o número de linhas que estão visíveis no momento.

Se o recurso WordWrap estiver habilitado, o número de linhas poderá ser alterado quando as dimensões da janela de edição forem alteradas.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETline**](em-getline.md)
</dt> <dt>

[**em \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**Editar \_ GetLineCount**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





