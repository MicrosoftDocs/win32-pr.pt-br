---
title: Mensagem de EM_LINESCROLL (WinUser. h)
description: Rola o texto em um controle de edição de várias linhas.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- Controles de EM_LINESCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009563"
---
# <a name="em_linescroll-message"></a>\_Mensagem em LINESCROLL

Rola o texto em um controle de edição de várias linhas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Controles de edição:** O número de caracteres a rolar horizontalmente.

**Controles de edição avançados:** Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

O número de linhas a rolar verticalmente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem for enviada para um controle de edição de várias linhas, o valor de retorno será **true**.

Se a mensagem for enviada para um controle de edição de linha única, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

O controle não rola verticalmente além da última linha de texto no controle de edição. Se a linha atual mais o número de linhas especificado pelo parâmetro *lParam* exceder o número total de linhas no controle de edição, o valor será ajustado de forma que a última linha do controle de edição seja rolada para a parte superior da janela de controle de edição.

**Controles de edição:** A mensagem em **\_ LINESCROLL** rola o texto vertical ou horizontalmente em um controle de edição de várias linhas. A mensagem em **\_ LINESCROLL** pode ser usada para rolar horizontalmente além do último caractere de qualquer linha.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. A mensagem em **\_ LINESCROLL** rola o texto verticalmente em um controle de edição de várias linhas. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

 





