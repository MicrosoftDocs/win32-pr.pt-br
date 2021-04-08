---
title: Mensagem de EM_GETPASSWORDCHAR (WinUser. h)
description: Obtém o caractere de senha que um controle de edição exibe quando o usuário digita o texto. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- Controles de EM_GETPASSWORDCHAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824689"
---
# <a name="em_getpasswordchar-message"></a>\_Mensagem em GETpasswordchar

Obtém o caractere de senha que um controle de edição exibe quando o usuário digita o texto. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

O valor de retorno especifica o caractere a ser exibido no lugar de quaisquer caracteres digitados pelo usuário. Se o valor de retorno for **nulo**, não haverá nenhum caractere de senha e o controle exibirá os caracteres digitados pelo usuário.

## <a name="remarks"></a>Comentários

Se um controle de edição for criado com o estilo de [**\_ senha es**](edit-control-styles.md) , o caractere de senha padrão será definido como um asterisco ( \* ). Se um controle de edição for criado sem o estilo de **\_ senha es** , não haverá nenhum caractere de senha. Para alterar o caractere da senha, envie a mensagem em [**\_ SetPasswordChar**](em-setpasswordchar.md) .

**Controles de edição:** Os controles de edição de várias linhas não dão suporte ao estilo de senha ou às mensagens.

**Edição avançada:** Com suporte no Microsoft rich edit 2,0 e posterior. Os controles de linha única e de edição de várias linhas dão suporte ao estilo e às mensagens da senha. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETpasswordchar**](em-setpasswordchar.md)
</dt> </dl>

 

 





