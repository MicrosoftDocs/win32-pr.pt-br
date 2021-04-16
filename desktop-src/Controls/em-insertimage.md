---
title: Mensagem de EM_INSERTIMAGE (RichEdit. h)
description: Substitui a seleção por um blob que exibe uma imagem.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- Controles de EM_INSERTIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_INSERTIMAGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9ff1e0fd355cf5dd8d43d211c44fda6417c638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454760"
---
# <a name="em_insertimage-message"></a>\_Mensagem em INSERTIMAGE

Substitui a seleção por um blob que exibe uma imagem.


```C++
#define EM_INSERTIMAGE       (WM_USER + 314)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ parâmetros de imagem RichEdit**](/windows/win32/api/richedit/ns-richedit-richedit_image_parameters) que contém o blob de imagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou um dos seguintes códigos de erro.



| Código de retorno                                                                                    | Descrição                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**E \_ FALHA**</dt> </dl>        | Não é possível inserir a imagem. <br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | O parâmetro *lParam* é nulo ou aponta para uma imagem inválida. |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente disponível.<br/>                  |



 

## <a name="remarks"></a>Comentários

Se a seleção for um ponto de inserção, o blob de imagem será inserido no ponto de inserção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_inserir em**](em-inserttable.md)
</dt> </dl>

 

 





