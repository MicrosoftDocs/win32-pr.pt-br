---
title: Mensagem de EM_AUTOURLDETECT (RichEdit. h)
description: Habilita ou desabilita a detecção automática de hiperlinks por um controle de edição rico.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- Controles de EM_AUTOURLDETECT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918711"
---
# <a name="em_autourldetect-message"></a>\_Mensagem em AUTOURLDETECT

Habilita ou desabilita a detecção automática de hiperlinks por um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifique 0 para desabilitar a detecção automática de link ou um dos valores a seguir para habilitar vários tipos de detecção.



| Valor                                                                                                                                                                                       | Significado                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**AURL \_ DISABLEMIXEDLGC**</dt> </dl>          | **Windows 8**: desabilite o reconhecimento de nomes de domínio que contêm rótulos com caracteres que pertencem a mais de um dos seguintes scripts: latim, grego e cirílico. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**AURL \_ ENABLEDRIVELETTERS**</dt> </dl> | **Windows 8**: reconhecer nomes de arquivos que têm uma especificação de unidade principal, como c: \\ Temp.<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**AURL \_ ENABLEEA**</dt> </dl>                               | Esse valor é preterido; em vez disso, use **AURL \_ ENABLEEAURLS** .<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**AURL \_ ENABLEEAURLS**</dt> </dl>                   | Reconhecer URLs que contêm caracteres do leste asiático. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**AURL \_ ENABLEEMAILADDR**</dt> </dl>          | **Windows 8**: reconhecer endereços de email.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**AURL \_ ENABLETELNO**</dt> </dl>                      | **Windows 8**: reconhecer números de telefone.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**AURL \_ ENABLEURL**</dt> </dl>                            | **Windows 8**: reconhecer URLs que incluem o caminho.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro determinará os esquemas de URL reconhecidos se **AURL \_ ENABLEURL** estiver ativo. Se *lParam* for NULL, a lista de nome de esquema padrão será usada (consulte comentários). Como alternativa, *lParam* pode apontar para uma cadeia de caracteres terminada em nulo que consiste em até 50 de nomes de esquema terminados por dois-pontos que substituem a lista de nome de esquema padrão. Por exemplo, a cadeia de caracteres poderia ser "News: http: ftp: Telnet:". A sintaxe do nome do esquema é definida no [Uniform Resource Identifiers (URI): documento de sintaxe genérica]( https://www.ietf.org/rfc/rfc2396.txt) no site da IETF (Internet Engineering Task Force). Especificamente, um nome de esquema pode conter até 13 caracteres (incluindo os dois-pontos), deve começar com um alfabeto ASCII e pode ser seguido por uma mistura de alfabetos ASCII, dígitos e os três caracteres de Pontuação: ".", "+" e "-". O tipo de cadeia de caracteres pode ser **Char \** _ ou _*WCHAR \**_; o controle de edição rico detecta automaticamente o tipo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, o valor de retorno será zero.

Se a mensagem falhar, o valor de retorno será um valor diferente de zero. Por exemplo, a mensagem pode falhar devido a memória insuficiente, uma opção de detecção inválida ou uma cadeia de caracteres de nome de esquema inválida.

Se _lParam * contiver mais de 50 nomes de esquema, a mensagem falhará com um valor de retorno de **E \_ INVALIDARG**.

## <a name="remarks"></a>Comentários

Se a detecção automática de URL estiver habilitada (ou seja, *wParam* incluir **AURL \_ ENABLEURL**), o controle de edição rico examinará qualquer texto modificado para determinar se o texto corresponde ao formato de uma URL (ou mais geralmente no Windows 8 ou posterior um identificador de recurso internacional IRI). Se *lParam* for NULL, o controle detectará URLs que começam com os seguintes nomes de esquema:

-   callto
-   arquivo
-   FTP
-   gopher
-   http
-   HTTPS
-   mailto
-   notícias
-   HDInsight
-   NNTP
-   onenote
-   outlook
-   prospero
-   tel
-   telnet
-   wais
-   webcal

Quando a detecção automática de link está habilitada, o controle de edição rico remove o efeito de **\_ link CFE** do texto modificado que não tem um formato reconhecido pelo controle. Se seu aplicativo usar o efeito de **\_ link CFE** para marcar outros tipos de texto, não habilite a detecção automática de link. O controle de edição rico não verifica se existe um link detectado; essa responsabilidade pertence ao cliente.

Um controle de edição rico envia a notificação de [ \_ link en](en-link.md) quando recebe várias mensagens enquanto o ponteiro do mouse está sobre o texto que tem o efeito de **\_ link CFE** . Para obter mais informações, consulte hiperlinks [automáticos de RichEdit](/archive/blogs/murrays/automatic-richedit-hyperlinks) e [hiperlinks de nome amigável do RichEdit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[\_link para](en-link.md)
</dt> </dl>

 

