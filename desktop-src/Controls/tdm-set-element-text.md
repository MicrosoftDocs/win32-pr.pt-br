---
title: Mensagem de TDM_SET_ELEMENT_TEXT (commctrl. h)
description: Mensagem de TDM_SET_ELEMENT_TEXT-atualiza um elemento de texto em uma caixa de diálogo de tarefa.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- Controles de TDM_SET_ELEMENT_TEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0c8830a6d8a1057ab283a9e096434a6184151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104024"
---
# <a name="tdm_set_element_text-message"></a>\_Mensagem de \_ texto do elemento do conjunto TDM \_

Atualiza um elemento de texto em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Indica o elemento a ser atualizado. (Para obter uma ilustração, consulte [sobre caixas de diálogo de tarefas](task-dialogs-overview.md).) Esse parâmetro deve ser um dos valores a seguir.



| Valor                                                                                                                                                                                           | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**conteúdo do TDE \_**</dt> </dl>                                         | Conteúdo.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**\_informações expandidas do TDE \_**</dt> </dl> | Informações expandidas.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**rodapé do TDE \_**</dt> </dl>                                            | Texto do rodapé.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_instrução principal do TDE \_**</dt> </dl>             | Instrução principal.<br/>     |



 

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

O novo texto a ser usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

O tamanho ou o layout da caixa de diálogo de tarefa pode ser alterado para acomodar o novo texto.

## <a name="examples"></a>Exemplos

O código de exemplo a seguir mostra como definir o texto de rodapé na caixa de diálogo de tarefa representada por *HWND*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_texto do \_ elemento de atualização TDM \_**](tdm-update-element-text.md)
</dt> </dl>

 

 





