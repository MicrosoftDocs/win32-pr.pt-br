---
title: Mensagem de EM_SETPAGEROTATE (RichEdit. h)
description: Define o layout de texto para um controle de edição rico.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- Controles de EM_SETPAGEROTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918348"
---
# <a name="em_setpagerotate-message"></a>\_Mensagem em SETPAGEROTATE

\[**Em \_ O SETPAGEROTATE** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Define o layout de texto para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de layout do texto. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                       | Significado                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <dt>**EPR \_ 0**</dt> </dl>       | O texto flui da esquerda para a direita e de cima para baixo.<br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <dt>**EPR \_ 90**</dt> </dl>    | O texto flui de baixo para cima e da esquerda para a direita.<br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <dt>**EPR \_ 180**</dt> </dl> | O texto flui da direita para a esquerda e de baixo para cima.<br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <dt>**EPR \_ 270**</dt> </dl> | O texto flui de cima para baixo e da direita para a esquerda.<br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <dt>**EPR \_ se**</dt> </dl>    | **Windows 8:** O texto flui de cima para baixo e da esquerda para a direita (layout de texto mongol).<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Valor de retorno é o novo valor de layout de texto.

## <a name="remarks"></a>Comentários

Esta mensagem define o layout de texto para todo o documento. No entanto, o conteúdo inserido não é girado e deve ser girado separadamente pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETPAGEROTATE**](em-getpagerotate.md)
</dt> </dl>

 

 





