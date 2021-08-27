---
title: TDM_SET_ELEMENT_TEXT mensagem (Commctrl.h)
description: TDM_SET_ELEMENT_TEXT mensagem – atualiza um elemento de texto em uma caixa de diálogo de tarefa.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT controles de Windows mensagem
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
ms.openlocfilehash: 7bb0f81867bcff4fd5f7d533c156c8af17d0f4a761b6f8560aa584a85c62b7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060766"
---
# <a name="tdm_set_element_text-message"></a>Mensagem de TEXTO \_ DO ELEMENTO SET \_ \_ DO TDM

Atualiza um elemento de texto em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

Indica o elemento a ser atualizado. (Para ver uma ilustração, consulte [About Task Dialogs](task-dialogs-overview.md).) Esse parâmetro deve ser um dos valores a seguir.



| Valor                                                                                                                                                                                           | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**CONTEÚDO \_ DA TDE**</dt> </dl>                                         | Conteúdo.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**INFORMAÇÕES \_ EXPANDIDAS DE \_ TDE**</dt> </dl> | Informações expandidas.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**RODAPÉ \_ DE TDE**</dt> </dl>                                            | Texto do rodapé.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**INSTRUÇÃO TDE \_ \_ MAIN**</dt> </dl>             | Instrução principal.<br/>     |



 

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

O novo texto a ser usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

O tamanho ou o layout da caixa de diálogo de tarefa pode mudar para acomodar o novo texto.

## <a name="examples"></a>Exemplos

O código de exemplo a seguir mostra como definir o texto do rodapé na caixa de diálogo de tarefa representada por *hwnd*.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TEXTO DO ELEMENTO UPDATE DO TDM \_ \_ \_**](tdm-update-element-text.md)
</dt> </dl>

 

 





