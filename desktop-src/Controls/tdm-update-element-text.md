---
title: Mensagem de TDM_UPDATE_ELEMENT_TEXT (commctrl. h)
description: Mensagem de TDM_UPDATE_ELEMENT_TEXT-atualiza um elemento de texto em uma caixa de diálogo de tarefa.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- controles de Windows de mensagem de TDM_UPDATE_ELEMENT_TEXT
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5abf6eb91b3eadfea71d0c9a4b5386e44db100c3a548998d5113636ff7f8cc29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166909"
---
# <a name="tdm_update_element_text-message"></a>\_Mensagem de \_ texto do elemento de atualização TDM \_

Atualiza um elemento de texto em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Indica o elemento a ser atualizado. (Para obter uma ilustração dos elementos, consulte [sobre caixas de diálogo de tarefas](task-dialogs-overview.md).) Esse parâmetro deve ser um dos seguintes valores:



| Valor                                                                                                                                                                                           | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**conteúdo do TDE \_**</dt> </dl>                                         | Conteúdo.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**\_informações expandidas do TDE \_**</dt> </dl> | Informações expandidas.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**rodapé do TDE \_**</dt> </dl>                                            | Texto do rodapé.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**\_instrução principal do TDE \_**</dt> </dl>             | Instrução principal.<br/>     |



 

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode que contém o novo texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Para evitar o recorte, o novo texto não deve ser maior do que o texto existente. Definir o texto para uma cadeia de caracteres mais curta não faz com que a caixa de diálogo seja redimensionada.

Se o membro **pszExpandedInformation** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usada para criar a caixa de diálogo de tarefa fosse **nulo** e você enviar uma mensagem de texto de **elemento de \_ atualização \_ \_ TDM** com \_ informações expandidas do TDE \_ , nada acontecerá.

O acima também se aplica ao rodapé rodapé e TDE \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_texto do \_ elemento do conjunto de TDM \_**](tdm-set-element-text.md)
</dt> </dl>

 

 





