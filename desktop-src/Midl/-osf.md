---
title: comutador/OSF
description: A opção/OSF força a compatibilidade estrita com o uso DCE.
ms.assetid: d94228fa-24af-43d7-9596-cf3a14690e0b
keywords:
- MIDL do comutador/OSF
topic_type:
- apiref
api_name:
- /osf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb887997642b0d0ff81314d6cf81dc148e57547727a09b1fe646f04d0391f967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014114"
---
# <a name="osf-switch"></a>comutador/OSF

A opção **/OSF** força a compatibilidade estrita com o uso DCE.

``` syntax
midl /osf
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Use essa opção se seu aplicativo exigir compatibilidade estrita com o uso DCE para fins de portabilidade.

No modo **/OSF** , o pacote RPCSS é habilitado automaticamente quando você usa ponteiros completos, os argumentos exigem alocação de memória ou quando você usa o atributo [**habilitar \_ alocação**](enable-allocate.md) . Isso significa que você não precisa fornecer as funções de [**\_ \_ alocação**](/windows/desktop/Rpc/the-midl-user-allocate-function) de usuário de MIDL e de [**\_ \_ usuário MIDL**](/windows/desktop/Rpc/the-midl-user-free-function) em seu aplicativo cliente e servidor.

Os seguintes recursos estendidos da Microsoft não estão disponíveis quando você compila com a opção **/OSF** :

-   Os declaradores abstratos (parâmetros sem nome) no arquivo IDL.
-   Definições de interface para objetos COM.
-   Nomes de interface com mais de 17 caracteres.
-   Atributos somente MIDL, como [**\_ marshaling de conexão**](wire-marshal.md), [**\_ marshaling do usuário**](user-marshal.md)e as extensões de typelib (ODL).
-   Usando palavras-chave ACF em um arquivo IDL (a opção MIDL **/app \_ config** ).
-   Funções de retorno de chamada estática no cliente.
-   O atributo [**Async**](async.md) .
-   [**\_ aspas de CPP**](cpp-quote.md) e **\# \_ eco de MIDL de pragma**.
-   [**WCHAR \_ t**](wchar-t.md) largo-tipos de caractere, constantes e cadeias de caracteres.
-   inicialização de [**Enumeração**](enum.md) (enumeradores esparsos).
-   especificação de tamanho somente [**out**](out-idl.md).
-   Tamanhos mistos-ponteiros e matrizes dimensionais.
-   Expressões usadas para especificadores de tamanho e discriminador.
-   Parâmetros de identificador explícitos em qualquer posição na lista de argumentos. No modo **/OSF** , o compilador MIDL procura um identificador de ligação explícito como o primeiro parâmetro. Quando o primeiro parâmetro não é um identificador de associação e um ou mais identificadores de contexto são especificados, o identificador de contexto mais à esquerda é usado como o identificador de associação. Quando o primeiro parâmetro não é um identificador e não há identificadores de contexto, o procedimento usa a associação implícita usando o [**\_ identificador implícito**](implicit-handle.md) do atributo de ACF ou o [**\_ identificador automático**](auto-handle.md).
-   Herança de tipo de atributo de ponteiro. USO o DCE não permite ponteiros sem atributo. Portanto, no modo **/OSF** , cada arquivo IDL deve definir atributos para seus ponteiros. Se qualquer ponteiro não tiver um atributo explícito, o arquivo IDL deverá ter uma especificação de [**ponteiro \_ padrão**](pointer-default.md) para definir o tipo de ponteiro.
-   Várias interfaces em um arquivo IDL.
-   Definições fora do bloco de interface.
-   Qualificadores de tipo, como **far** e **stdcall**.
-   Omitindo atributos direcionais.

As seguintes extensões de linguagem C/C++ não estão disponíveis quando você compila com a opção **/OSF** :

-   Campos de bits em estruturas e uniões.
-   Comentários de linha única delimitados por dois caracteres de barra (//).
-   Declarações externas.
-   Procedimentos com reticências na lista de parâmetros.
-   Digite [**int**](int.md).
-   Digite **void \** _ (exceto com o atributo [_ *contexto \_ Handle* *](context-handle.md) ).
-   Os qualificadores de tipo, incluindo o formulário com o prefixo de conformidade com ANSI, contêm dois caracteres de sublinhado: **\_ \_ cdecl**, **cdecl**, [**const**](const.md), **const**, **\_ \_ Exportar**, **Exportar**, **\_ \_ longe**, **longe**, **\_ \_ LOADDS**, **LOADDS**, **\_ \_ próximo**, **próximo**, **\_ \_ Pascal**, **Pascal**, **\_ \_ stdcall**, **stdcall**, **\_ \_ volátil** e **volátil**.
-   Qualquer \# aviso [**pragma**](pragma.md) ou comentário **\# pragma** .
-   Serialização de tipo.
-   O tipo de dados [**\_ \_ int3264**](--int3264.md) .
-   A opção [**/Protocol**](-protocol.md) e a sintaxe de transferência ndr64.

## <a name="examples"></a>Exemplos

**MIDL/OSF filename. idl**

**MIDL/OSF/app \_ config filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**configuração do/App \_**](-app-config.md)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[Pacote de gerenciamento de memória de RPCSS](/windows/desktop/Rpc/rpcss-memory-management-package)
</dt> </dl>

 

 