---
title: Mensagem de EM_INSERTIMAGE (RichEdit. h)
description: Substitui a seleção por um blob que exibe uma imagem.
ms.assetid: 147B298B-C4A9-455B-9736-A0B09D72902B
keywords:
- controles de Windows de mensagem de EM_INSERTIMAGE
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
ms.openlocfilehash: 7418a8fe4b7c627d211bce7bf2591ed684d82e42089fbe9bedeb2f76a6b9d3e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437886"
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

## <a name="return-value"></a>Valor retornado

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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_inserir em**](em-inserttable.md)
</dt> </dl>

 

 





