---
title: Mensagem de EM_GETIMECOMPMODE (RichEdit. h)
description: Recupera o modo do IME (editor de método de entrada) atual para um controle de edição rico.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- Controles de EM_GETIMECOMPMODE de mensagens do Windows
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
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455545"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é um dos valores a seguir.



| Código de retorno                                                                                     | Descrição                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**ICM não \_ aberto**</dt> </dl>     | O IME não está aberto.<br/>  |
| <dl> <dt>**LEVEL3 de ICM \_**</dt> </dl>      | Modo embutido verdadeiro.<br/> |
| <dl> <dt>**LEVEL2 de ICM \_**</dt> </dl>      | Nível 2.<br/>          |
| <dl> <dt>**ICM \_ LEVEL2 \_ 5**</dt> </dl>   | Nível 2,5<br/>         |
| <dl> <dt>**ICM \_ LEVEL2 \_ sui**</dt> </dl> | Interface do usuário especial.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





