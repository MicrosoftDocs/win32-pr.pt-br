---
title: Mensagem de EM_STREAMOUT (RichEdit. h)
description: Faz com que um controle de edição rico passe seu conteúdo para uma função de retorno de chamada EditStreamCallback do aplicativo \ 8211; definida. A função de retorno de chamada pode gravar o fluxo de dados em um arquivo ou em qualquer outro local escolhido por ele.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- Controles de EM_STREAMOUT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918490"
---
# <a name="em_streamout-message"></a>Mensagem em fluxo em em \_

Faz com que um controle de edição rico passe seu conteúdo para uma função de retorno de chamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo. A função de retorno de chamada pode gravar o fluxo de dados em um arquivo ou em qualquer outro local escolhido por ele.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o formato de dados e as opções de substituição.

Esse valor deve ser um dos valores a seguir.



| Valor                                                                                                                                                      | Significado                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**It \_ RTF**</dt> </dl>                   | RTF.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**\_RTFNOOBJS**</dt> </dl> | RTF com espaços no lugar de objetos COM.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**texto de it \_**</dt> </dl>                | Texto com espaços no lugar de objetos COM.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**em \_ texto**</dt> </dl>    | Texto com uma representação de texto de objetos COM.<br/> |



 

A opção **it \_ RTFNOOBJS** é útil se um aplicativo armazena objetos com em si, pois a representação RTF de objetos com não é muito compacta. A palavra de controle, \\ objattph, seguida por um espaço denota a posição do objeto.

Além disso, você pode especificar os sinalizadores a seguir.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**\_PLAINRTF SFF**</dt> </dl>       | Se especificado, o controle de edição rico transmite apenas as palavras-chave comuns a todos os idiomas, ignorando palavras-chave específicas de idioma. Se não for especificado, o controle rich edit transmitirá todas as palavras-chave. Você pode combinar esse sinalizador com o sinalizador **it \_ RTF** ou **it \_ RTFNOOBJS** .<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**seleção de SFF \_**</dt> </dl>    | Se especificado, o controle rich edit transmitirá apenas o conteúdo da seleção atual. Se não for especificado, o controle transmitirá todo o conteúdo. Você pode combinar esse sinalizador com qualquer um dos valores de formato de dados.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**\_Unicode it**</dt> </dl>             | **Microsoft Rich Edit 2,0 e posterior:** Indica texto Unicode. Você pode combinar esse sinalizador com o sinalizador de **\_ texto it** .<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**It \_ USECODEPAGE**</dt> </dl> | **Edição avançada 3,0 e posterior:** Gera UTF-8 RTF, bem como texto usando outras páginas de código. A página de código é definida na palavra alta do *wParam*. Por exemplo, para UTF-8 RTF, defina *wParam* como (CP \_ UTF8 << 16) \| it \_ USECODEPAGE \| it \_ RTF.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Na entrada, o membro **pfnCallback** dessa estrutura deve apontar para uma função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo. Na saída, o membro **dwError** poderá conter um código de erro diferente de zero se ocorrer um erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna o número de caracteres gravados no fluxo de dados.

## <a name="remarks"></a>Comentários

Quando você envia uma mensagem em **\_ StreamOut** , o controle de edição rico faz chamadas repetidas para a função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada pelo membro **pfnCallback** da estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) . Cada vez que ele chama a função de retorno de chamada, o controle passa um buffer contendo uma parte do conteúdo do controle. Esse processo continua até que o controle tenha passado todo o seu conteúdo para a função de retorno de chamada ou até que ocorra um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**fluxo de em \_**](em-streamin.md)
</dt> </dl>

 

 





