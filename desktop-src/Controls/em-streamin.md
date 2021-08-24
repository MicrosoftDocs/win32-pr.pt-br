---
title: EM_STREAMIN mensagem (Richedit.h)
description: Substitui o conteúdo de um controle de edição rico por um fluxo de dados fornecidos por um aplicativo definido como \ 8211; Função de retorno de chamada EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN controles de Windows mensagem
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
ms.openlocfilehash: 597d6483ef02f0c9f6f4e4459cd6780b91e04c39160c8057e88fc537fde3b173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576336"
---
# <a name="em_streamin-message"></a>Mensagem EM \_ STREAMIN

Substitui o conteúdo de um controle de edição avançada por um fluxo de dados fornecidos por uma função de retorno de chamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica as opções de substituição e formato de dados. Esse valor deve ser um dos valores a seguir.



| Valor                                                                                                                                       | Significado         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF \_ TEXT**</dt> </dl> | Texto<br/> |



 

Além disso, você pode especificar os sinalizadores a seguir.



| Valor                                                                                                                                                         | Significado                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>    | Se especificado, somente palavras-chave comuns a todos os idiomas serão transmitidas. Palavras-chave RTF específicas de linguagem no fluxo são ignoradas. Se não for especificado, todas as palavras-chave serão transmitidas. Você pode combinar esse sinalizador com o **sinalizador \_ RTF SF.**<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SELEÇÃO \_ DE SFF**</dt> </dl> | Se especificado, o fluxo de dados substituirá o conteúdo da seleção atual. Se não for especificado, o fluxo de dados substituirá todo o conteúdo do controle. Você pode combinar esse sinalizador com os **sinalizadores SF \_ TEXT** ou **SF \_ RTF.**<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>          | **Microsoft Rich Edit 2.0 e posterior:** Indica o texto Unicode. Você pode combinar esse sinalizador com o **sinalizador SF \_ TEXT.** <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Na entrada, o **membro pfnCallback** dessa estrutura deve apontar para uma [*função EditStreamCallback definida pelo*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) aplicativo. Na saída, o **membro dwError** poderá conter um código de erro que não seja zero se ocorrer um erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna o número de caracteres lidos.

## <a name="remarks"></a>Comentários

Quando você envia uma **mensagem EM \_ STREAMIN,** o controle de edição avançada faz chamadas repetidas para a função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada pelo **membro pfnCallback** da estrutura [**EDITSTREAM.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Sempre que a função de retorno de chamada é chamada, ela preenche um buffer com dados para ler no controle. Isso continuará até que a função de retorno de chamada indique que a operação de stream-in foi concluída ou ocorre um erro.

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

[**EM \_ STREAMOUT**](em-streamout.md)
</dt> </dl>

 

 





