---
description: As mensagens são definidas em um arquivo de texto de mensagem. O compilador de mensagem atribui números a cada mensagem e gera um arquivo de inclusão C/C++ que o aplicativo pode usar para acessar uma mensagem usando uma constante simbólica.
ms.assetid: 99fbb3d6-6fde-4162-b0b9-99a1cdf0b8f8
title: Arquivos de texto da mensagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e87547f44b0b556df4e3a2ffb67736b950321c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165448"
---
# <a name="message-text-files"></a>Arquivos de texto da mensagem

As mensagens são definidas em um arquivo de texto de mensagem. O compilador de mensagem atribui números a cada mensagem e gera um arquivo de inclusão C/C++ que o aplicativo pode usar para acessar uma mensagem usando uma constante simbólica.

A sintaxe geral para instruções em um arquivo de texto de mensagem é a seguinte:

*palavra-chave* = *valor* do

Os espaços em torno do sinal de igual são ignorados e o valor é delimitado por espaço em branco (incluindo quebras de linha) do próximo par de palavra-chave/valor. O caso é ignorado ao comparar com nomes de palavra-chave. A parte de *valor* pode ser uma constante numérica de inteiro usando a sintaxe c/c++, um nome de símbolo que segue as regras para identificadores C/c++, ou um nome de arquivo com 8 caracteres ou menos, sem pontos.

Para obter um exemplo de arquivo de mensagem, consulte [exemplo de arquivo de texto de mensagem](sample-message-text-file.md).

## <a name="comments"></a>Comentários

Linhas de comentário são permitidas no arquivo de texto da mensagem. Um ponto e vírgula (;) inicia um comentário que termina no final da linha. Siga o ponto-e-vírgula com um indicador de comentário de linha única C/C++ (//) para que o arquivo de cabeçalho gerado pelo compilador de mensagem seja compilado em seu aplicativo.

``` syntax
;// This is a single-line comment.
```

Para um comentário de bloco, comece cada linha com um ponto e vírgula e coloque um indicador de comentário de bloco aberto C/C++ (/ \* ) após o ponto e vírgula na primeira linha e o indicador de comentário de bloco de fechamento ( \* /) após o ponto e vírgula na última linha.

``` syntax
;/* This is a block comment.
;   It spans multiple lines.
;*/
```

## <a name="header-section"></a>Seção de cabeçalho

O arquivo de texto da mensagem contém um cabeçalho que define os nomes e os identificadores de idioma para uso pelas definições de mensagem no corpo do arquivo. O cabeçalho contém zero ou mais das instruções a seguir.



| Sintaxe de instrução                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageIdTypedef =*tipo*                    | Tipo a ser usado na definição de mensagem da seguinte maneira: \# definir *nome* ((*tipo*) 0x *nnnnnnnn*)<br/> O tipo deve ser grande o suficiente para acomodar o código de mensagem inteiro, como um **DWORD**. O tipo também pode ser um tipo definido no código-fonte do aplicativo. O valor padrão para *Type* é Empty, portanto, nenhuma conversão de tipo é usada. <br/> Essa instrução pode ser especificada no cabeçalho e, sempre que necessário, na seção de definição de mensagem.<br/>                                                                                                                  |
| Gravidadenames = (número do *nome* =  \[ :*nome* \] ) | Conjunto de nomes que são permitidos para a severidade em uma definição de mensagem. Associado a cada nome de severidade há um número que, quando deslocado para a esquerda por 30 bits, dá ao padrão de bit um valor lógico ou com os valores de ID da mensagem e de instalação para formar o código da mensagem. Qualquer valor de severidade que não caiba em 2 bits é um erro. Os códigos de severidade também podem receber nomes simbólicos. O valor padrão é definido da seguinte maneira: Severidadenames = (êxito = 0x0 informativo = 0x1 aviso = 0x2 erro = 0x3)<br/>                                                                      |
| Facilitname = (número do *nome* =  \[ :*nome* \] ) | Conjunto de nomes que são permitidos para os valores de recurso em uma definição de mensagem. Associado a cada nome de recurso é um número que, quando deslocado para a esquerda por 16 bits, dá ao padrão de bit um valor lógico ou com os valores de severidade e ID da mensagem para formar o código da mensagem. Qualquer valor de recurso que não caiba em 12 bits é um erro. Isso permite códigos de instalações de 4096; os primeiros 256 códigos são reservados para uso do sistema. Os códigos de recurso também podem receber nomes simbólicos. O valor padrão é definido da seguinte maneira: refacilitname = (System = 0x0FF Application = 0xFFF)<br/> |
| Idiomas = (número do *nome* = :*nome de arquivo*) | Conjunto de nomes que são permitidos para os valores de idioma em uma definição de mensagem. O número é usado como o identificador de idioma na tabela de recursos. O arquivo especificado contém as mensagens para esse idioma. Normalmente, é um arquivo. bin gerado pelo compilador de mensagem.<br/> Um valor de exemplo é: Languagenames = (Inglês = 0x409: MSG00409)<br/> Para obter uma lista de identificadores de idioma, consulte <https://go.microsoft.com/fwlink/p/?linkid=190280> .<br/>                                                                                                                    |
| OutputBase =*número*                        | A base de saída das constantes de mensagem que o compilador de mensagem grava no arquivo de cabeçalho. Se estiver presente, esse valor substituirá a opção-d. Esse número pode ser 10 (Decimal) ou 16 (hexadecimal).                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="message-definitions"></a>Definições de mensagem

Um arquivo de texto de mensagem contém zero ou mais definições de mensagem após a seção de cabeçalho. A tabela a seguir descreve as instruções de definição de mensagem. A instrução MessageId marca o início da definição da mensagem. As instruções Severity e Facility são opcionais.



| Sintaxe de instrução                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageId = \[  \| + *número* de número\] | Identificador da mensagem. Essa instrução é necessária, embora o valor seja opcional. Se nenhum valor for especificado, o valor usado será o valor anterior para a instalação, mais um. Se o valor for especificado com um sinal de adição, o valor usado será o valor anterior para a instalação, mais o número após o sinal de adição. Qualquer valor especificado deve caber em 16 bits. Para obter mais detalhes sobre como o valor da mensagem é formado por gravidade, instalação e ID da mensagem, consulte o diagrama em Winerror. h. Esse arquivo de cabeçalho define códigos de erro para o sistema.<br/> |
| Severidade =*nome*                   | Um dos valores especificados por Severitynames no cabeçalho. Essa instrução é opcional. Se nenhum valor for especificado, o valor usado será o valor especificado pela última vez para uma definição de mensagem. O padrão para a primeira definição de mensagem é `Severity=Success`<br/>                                                                                                                                                                                                                                                                                               |
| Instalação =*nome*                   | Um dos valores especificados por recursos no cabeçalho. Essa instrução é opcional. Se nenhum valor for especificado, o valor usado será o valor especificado pela última vez para uma definição de mensagem. O padrão para a primeira definição de mensagem é `Facility=Application`<br/>                                                                                                                                                                                                                                                                                           |
| Simbóliconame =*nome*               | Associa uma constante simbólica C/C++ ao código da mensagem. Ele é usado na definição da mensagem da seguinte maneira: \# definir *nome* ((*tipo*) 0x *nnnnnnnn*)<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| OutputBase = {*Number*}             | A base de saída das constantes de mensagem que o compilador de mensagem grava no arquivo de cabeçalho. Se estiver presente, esse valor substituirá a opção-d. Esse número pode ser 10 (Decimal) ou 16 (hexadecimal).                                                                                                                                                                                                                                                                                                                                                                 |
| Idioma =*nome*                   | Um dos valores especificados por Languagenames no cabeçalho. Essa instrução é opcional. Se nenhum valor for especificado, o valor usado será o valor especificado pela última vez para uma definição de mensagem. O padrão para a primeira definição de mensagem é o seguinte: `Language=English`<br/>                                                                                                                                                                                                                                                                                   |
| *texto da mensagem*                    | Texto da mensagem. Ele é incluído no arquivo binário da mensagem. Ele também está incluído no arquivo de cabeçalho no bloco de comentário que precede diretamente a definição de mensagem.                                                                                                                                                                                                                                                                                                                                                                                        |
| .                                 | O texto da mensagem é encerrado por uma nova linha que contém um único período no início da linha.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

Se a definição de mensagem incluir o texto da mensagem para mais de um idioma, cada idioma exigirá sua própria instrução de linguagem, texto de mensagem e encerrando a nova linha com um ponto. Por exemplo:

``` syntax
MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.
```

Você pode especificar as sequências de escape a seguir para formatar o texto da mensagem para uso pelo Visualizador de eventos ou seu aplicativo. O caractere de sinal de porcentagem (%) Inicia todas as sequências de escape. Qualquer outro caractere após um sinal de porcentagem é exibido sem o sinal de porcentagem.

<dl> <dt>

<span id="_n__format_specifier__"></span><span id="_N__FORMAT_SPECIFIER__"></span>%*n* \[ ! *\_ especificador de formato*!\]
</dt> <dd>

Descreve uma inserção. Cada Insert é uma entrada na matriz Arguments na função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . O valor de *n* pode ser um número entre 1 e 99. O especificador de formato é opcional. Se nenhum valor for especificado, o padrão será! s!. Para obter informações sobre o especificador de formato, consulte [**wsprintf**](/windows/win32/api/winuser/nf-winuser-wsprintfa).

O especificador de formato pode \* ser usado para a precisão ou a largura. Quando especificado, eles consomem inserções numeradas *n*+ 1 e *n*+ 2.

</dd> <dt>

<span id="_0"></span>%0
</dt> <dd>

Encerra uma linha de texto de mensagem sem um caractere de nova linha à direita. Isso pode ser usado para criar uma linha longa ou encerrar uma mensagem de prompt sem um caractere de nova linha à direita.

</dd> <dt>

<span id="_."></span>%.
</dt> <dd>

Gera um único período. Isso pode ser usado para exibir um ponto no início de uma linha, o que, de outra forma, encerraria o texto da mensagem.

</dd> <dt>

<span id="__"></span>%!
</dt> <dd>

Gera um ponto de exclamação único. Isso pode ser usado para especificar um ponto de exclamação imediatamente após uma inserção.

</dd> <dt>

<span id="__"></span>%%
</dt> <dd>

Gera um único sinal de porcentagem.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>% n
</dt> <dd>

Gera uma quebra de linha rígida quando ocorre no final de uma linha. Isso pode ser usado com [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) para garantir que a mensagem se ajuste a uma determinada largura.

</dd> <dt>

<span id="_b"></span><span id="_B"></span>% b
</dt> <dd>

Gera um caractere de espaço. Isso pode ser usado para garantir um número apropriado de espaços à direita em uma linha.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>% r
</dt> <dd>

Gera um retorno de carro rígido sem um caractere de nova linha à direita.

</dd> </dl>

 

