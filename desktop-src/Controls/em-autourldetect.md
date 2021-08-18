---
title: EM_AUTOURLDETECT mensagem (Richedit.h)
description: Habilita ou desabilita a detecção automática de hiperlinks por um controle de edição rico.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT controles Windows mensagem
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
ms.openlocfilehash: 0e7c53df29b1d106c537543983f1734aef7facaaca5d0965c3a2588f285a7391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049426"
---
# <a name="em_autourldetect-message"></a>Mensagem EM \_ AUTOURLDETECT

Habilita ou desabilita a detecção automática de hiperlinks por um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifique 0 para desabilitar a detecção automática de link ou um dos valores a seguir para habilitar vários tipos de detecção.



| Valor                                                                                                                                                                                       | Significado                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**AURL \_ DISABLEMIXEDLGC**</dt> </dl>          | **Windows 8:** desabilite o reconhecimento de nomes de domínio que contêm rótulos com caracteres pertencentes a mais de um dos seguintes scripts: latino, grego e cirílico. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**AURL \_ ENABLEDRIVELETERS**</dt> </dl> | **Windows 8:** reconhecer nomes de arquivo que têm uma especificação de unidade à frente, como c: \\ temp.<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**AURL \_ ENABLEEA**</dt> </dl>                               | Esse valor foi preterido; em **vez disso, use AURL \_ ENABLERLS.**<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**AURL \_ ENABLERLS**</dt> </dl>                   | Reconhecer URLs que contêm caracteres do Leste da Ásia. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**AURL \_ ENABLEEMAILADDR**</dt> </dl>          | **Windows 8:** reconhecer endereços de email.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**AURL \_ ENABLETELNO**</dt> </dl>                      | **Windows 8:** reconhecer números de telefone.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**AURL \_ ENABLEURL**</dt> </dl>                            | **Windows 8:** reconhecer URLs que incluem o caminho.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro determina os esquemas de URL reconhecidos se **a AURL \_ ENABLEURL** está ativa. Se *lParam* for NULL, a lista de nomes de esquema padrão será usada (consulte Comentários). Como alternativa, *lParam* pode apontar para uma cadeia de caracteres terminada em nulo que consiste em até 50 nomes de esquema terminados por dois-pontos que superam a lista de nomes de esquema padrão. Por exemplo, a cadeia de caracteres pode ser "news:http:ftp:telnet:". A sintaxe do nome do esquema é definida no [documento Uniform Resource Identifiers (URI): Sintaxe]( https://www.ietf.org/rfc/rfc2396.txt) genérica no site da IETF (Força-Tarefa de Engenharia da Internet). Especificamente, um nome de esquema pode conter até 13 caracteres (incluindo dois-pontos), deve começar com um alfabético ASCII e pode ser seguido por uma combinação de alfabéticos ASCII, dígitos e os três caracteres de pontuação: ".", "+" e "-". O tipo de cadeia de caracteres pode ser **char _ ou \* *_* WCHAR \***; o controle de edição rich detecta automaticamente o tipo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será zero.

Se a mensagem falhar, o valor de retorno será um valor não zero. Por exemplo, a mensagem pode falhar devido à memória insuficiente, a uma opção de detecção inválida ou a uma cadeia de caracteres de nome de esquema inválida.

Se *lParam contiver* mais de 50 nomes de esquema, a mensagem falhará com um valor de **retorno de E \_ INVALIDARG.**

## <a name="remarks"></a>Comentários

Se a detecção automática de URL estiver habilitada (ou seja, *o wParam* incluirá **a AURL \_ ENABLEURL),** o controle de edição rich verificará qualquer texto modificado para determinar se o texto corresponde ao formato de uma URL (ou mais geralmente no Windows 8 ou posteriormente em um Identificador de Recurso Internacional da IRI). Se *lParam* for NULL, o controle detectará URLs que começam com os seguintes nomes de esquema:

-   callto
-   file
-   FTP
-   gopher
-   http
-   HTTPS
-   mailto
-   notícias
-   HDInsight
-   Nntp
-   onenote
-   outlook
-   Prospero
-   tel
-   telnet
-   wais
-   webcal

Quando a detecção automática de link está habilitada, o controle de edição rich remove o efeito LINK do **CFE \_** do texto modificado que não tem um formato reconhecido pelo controle. Se seu aplicativo usar o efeito **LINK \_ do CFE** para marcar outros tipos de texto, não habilita a detecção automática de link. O controle de edição rich não verifica se existe um link detectado; essa responsabilidade pertence ao cliente.

Um controle de edição rich envia a notificação [ \_ EN LINK](en-link.md) quando recebe várias mensagens enquanto o ponteiro do mouse está sobre o texto que tem o efeito **\_ CFE LINK.** Para obter mais informações, [consulte Hiperlinks RichEdit Automáticos](/archive/blogs/murrays/automatic-richedit-hyperlinks) e [Hiperlinks de Nome Amigável RichEdit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Charformat2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[LINK DO EN \_](en-link.md)
</dt> </dl>

 

