---
title: Mensagem de EM_GETIMECOMPMODE (RichEdit. h)
description: Recupera o modo do IME (editor de método de entrada) atual para um controle de edição rico.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- controles de Windows de mensagem de EM_GETIMECOMPMODE
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53b9c0242872446c22034502d92af00ead7289fc68b4d5a66d79c3ef68be5eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019544"
---
# <a name="em_getimecompmode-message"></a>\_Mensagem em GETIMECOMPMODE

Recupera o modo do IME (editor de método de entrada) atual para um controle de edição rico.

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

## <a name="return-value"></a>Valor retornado

O valor de retorno é um dos valores a seguir.



| Código de retorno                                                                                     | Descrição                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**ICM \_ Não aberto**</dt> </dl>     | O IME não está aberto.<br/>  |
| <dl> <dt>**ICM \_ LEVEL3**</dt> </dl>      | Modo embutido verdadeiro.<br/> |
| <dl> <dt>**ICM \_ LEVEL2**</dt> </dl>      | Nível 2.<br/>          |
| <dl> <dt>**ICM \_ LEVEL2 \_ 5**</dt> </dl>   | Nível 2,5<br/>         |
| <dl> <dt>**ICM \_ LEVEL2 \_ sui**</dt> </dl> | Interface do usuário especial.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





