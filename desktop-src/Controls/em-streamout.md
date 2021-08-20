---
title: EM_STREAMOUT mensagem (Richedit.h)
description: Faz com que um controle de edição avançada passe seu conteúdo para um aplicativo \ 8211;função de retorno de chamada EditStreamCallback definida. A função de retorno de chamada pode gravar o fluxo de dados em um arquivo ou em qualquer outro local escolhido.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT controles de Windows mensagem
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
ms.openlocfilehash: 63236083c1964d29cb915e4bfc51303b30b730e01f76f2b186cc200d1dcfce6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019464"
---
# <a name="em_streamout-message"></a>Mensagem EM \_ STREAMOUT

Faz com que um controle de edição avançada passe seu conteúdo para uma função de retorno de [*chamada EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo. A função de retorno de chamada pode gravar o fluxo de dados em um arquivo ou em qualquer outro local escolhido.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica as opções de substituição e formato de dados.

Esse valor deve ser um dos valores a seguir.



| Valor                                                                                                                                                      | Significado                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>                   | Rtf.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**SF \_ RTFNOOBJS**</dt> </dl> | RTF com espaços no lugar de objetos COM.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF \_ TEXT**</dt> </dl>                | Texto com espaços no lugar de objetos COM.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF \_ TEXTIZED**</dt> </dl>    | Texto com uma representação de texto de objetos COM.<br/> |



 

A **opção SF \_ RTFNOOBJS** será útil se um aplicativo armazenar objetos COM em si, pois a representação RTF de objetos COM não é muito compacta. A palavra de \\ controle, objattph, seguida por um espaço indica a posição do objeto.

Além disso, você pode especificar os sinalizadores a seguir.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>       | Se especificado, o controle de edição avançada transmitirá apenas as palavras-chave comuns a todos os idiomas, ignorando palavras-chave específicas do idioma. Se não for especificado, o controle de edição avançada transmitirá todas as palavras-chave. Você pode combinar esse sinalizador com o **sinalizador \_ RTF ou** **SF \_ RTFNOOBJS SF.**<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SELEÇÃO \_ DE SFF**</dt> </dl>    | Se especificado, o controle de edição rich transmite apenas o conteúdo da seleção atual. Se não for especificado, o controle transmitirá todo o conteúdo. Você pode combinar esse sinalizador com qualquer um dos valores de formato de dados.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>             | **Microsoft Rich Edit 2.0 e posterior:** Indica o texto Unicode. Você pode combinar esse sinalizador com o **sinalizador SF \_ TEXT.**<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**SF \_ USECODEPAGE**</dt> </dl> | **Rich Edit 3.0 e posterior:** Gera rTF UTF-8, bem como texto usando outras páginas de código. A página de código é definida na palavra alta *de wParam*. Por exemplo, para UTF-8 RTF, de definir *wParam* como (CP \_ UTF8 << 16) \| SF \_ USECODEPAGE \| SF \_ RTF.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Na entrada, o **membro pfnCallback** dessa estrutura deve apontar para uma [*função EditStreamCallback definida pelo*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) aplicativo. Na saída, o **membro dwError** poderá conter um código de erro que não seja zero se ocorrer um erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna o número de caracteres gravados no fluxo de dados.

## <a name="remarks"></a>Comentários

Quando você envia uma **mensagem EM \_ STREAMOUT,** o controle de edição avançada faz chamadas repetidas para a função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada pelo **membro pfnCallback** da estrutura [**EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Sempre que ele chama a função de retorno de chamada, o controle passa um buffer que contém uma parte do conteúdo do controle. Esse processo continua até que o controle tenha passado todo o conteúdo para a função de retorno de chamada ou até que ocorra um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*Editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





