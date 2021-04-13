---
title: Mensagem de EM_STREAMIN (RichEdit. h)
description: Substitui o conteúdo de um controle de edição rico por um fluxo de dados fornecidos por um aplicativo definido \ 8211; Função de retorno de chamada EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- Controles de EM_STREAMIN de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455666"
---
# <a name="em_streamin-message"></a>Mensagem de fluxo em em \_

Substitui o conteúdo de um controle de edição rico por um fluxo de dados fornecidos por uma função de retorno de chamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o formato de dados e as opções de substituição. Esse valor deve ser um dos valores a seguir.



| Valor                                                                                                                                       | Significado         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**It \_ RTF**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**texto de it \_**</dt> </dl> | Texto<br/> |



 

Além disso, você pode especificar os sinalizadores a seguir.



| Valor                                                                                                                                                         | Significado                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**\_PLAINRTF SFF**</dt> </dl>    | Se especificado, somente palavras-chave comuns a todos os idiomas serão transmitidas em fluxo. Palavras-chave RTF específicas do idioma no fluxo são ignoradas. Se não for especificado, todas as palavras-chave serão transmitidas. Você pode combinar esse sinalizador com o sinalizador **it \_ RTF** .<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**seleção de SFF \_**</dt> </dl> | Se especificado, o fluxo de dados substituirá o conteúdo da seleção atual. Se não for especificado, o fluxo de dados substituirá todo o conteúdo do controle. Você pode combinar esse sinalizador com os sinalizadores de **\_ texto** de it ou **it \_ RTF** .<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**\_Unicode it**</dt> </dl>          | **Microsoft Rich Edit 2,0 e posterior:** Indica texto Unicode. Você pode combinar esse sinalizador com o sinalizador de **\_ texto it** . <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Na entrada, o membro **pfnCallback** dessa estrutura deve apontar para uma função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo. Na saída, o membro **dwError** poderá conter um código de erro diferente de zero se ocorrer um erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna o número de caracteres lidos.

## <a name="remarks"></a>Comentários

Quando você envia uma mensagem de **\_ fluxo** em em, o controle de edição rico faz chamadas repetidas para a função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada pelo membro **pfnCallback** da estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Cada vez que a função de retorno de chamada é chamada, ela preenche um buffer com dados para ler no controle. Isso continuará até que a função de retorno de chamada indique que a operação de entrada de fluxo foi concluída ou ocorrerá um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**em \_ fluxo contínuo**](em-streamout.md)
</dt> </dl>

 

 





