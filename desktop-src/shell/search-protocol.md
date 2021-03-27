---
description: 'A pesquisa: protocolo de aplicativo é uma convenção extensível para chamar o aplicativo de pesquisa de desktop no Windows Vista com Service Pack 1 (SP1) e versões posteriores.'
title: Usando o protocolo de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 91a1ec25-f6ab-4377-8478-20bc51a1d5df
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: a9223a2a30cab85f8e1b0dac0d0df2dc4fe8f80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989070"
---
# <a name="using-the-search-protocol"></a>Usando o protocolo de pesquisa

A **pesquisa:** [protocolo de aplicativo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) é uma convenção extensível para chamar o aplicativo de pesquisa de desktop no Windows Vista com Service Pack 1 (SP1) e versões posteriores. O protocolo foi criado no Windows Vista com SP1 (para obter informações, consulte a visão geral do artigo da base [de dados de conhecimento do Windows Vista Desktop Search Changes no Windows Vista Service Pack 1](https://support.microsoft.com/kb/941946)) para fornecer ao Windows uma maneira de determinar e chamar o aplicativo de pesquisa de desktop padrão.

A sintaxe de protocolo fornece vários parâmetros úteis para executar pesquisas de área de trabalho comuns, como termos de pesquisa inseridos pelo usuário ou o local em que a pesquisa foi iniciada. Quando os usuários pesquisam de um dos dois pontos de entrada de pesquisa disponíveis (o menu **Iniciar** ou o Windows Explorer), o sistema operacional usa o protocolo de pesquisa para iniciar o aplicativo de pesquisa de área de trabalho padrão. Ele faz isso adicionando os termos de pesquisa inseridos pelo usuário à sintaxe do protocolo de pesquisa padrão e passando essas informações para o aplicativo registrado como o aplicativo de pesquisa padrão.

Se nenhum outro aplicativo de pesquisa de desktop estiver instalado, uma pesquisa inserida nesses pontos de entrada iniciará o Windows Search Explorer. No entanto, desenvolvedores de terceiros podem criar, instalar e registrar seus aplicativos para lidar com o protocolo de pesquisa e para ser o aplicativo de pesquisa padrão. Esses aplicativos precisam dar suporte à sintaxe de protocolo de pesquisa e se registrarem com o recurso de [programas padrão](default-programs.md) para garantir uma experiência tranqüila com o Windows.

Se você desenvolver um aplicativo que se destina a usar ou a criar um aplicativo de pesquisa de área de trabalho específico, não deverá depender exclusivamente do protocolo **Search:** . Como muitos aplicativos podiam ter a **pesquisa:** protocolo, não há nenhuma garantia de que seu aplicativo de pesquisa de área de trabalho de destino o terá em um determinado momento. Em vez disso, você deve usar um protocolo de pesquisa particular definido por esse aplicativo de pesquisa de área de trabalho de destino. Isso significa que os aplicativos de pesquisa de desktops destinados a ser uma plataforma para aplicativos de terceiros devem dar suporte tanto ao protocolo **Search:** quanto ao seu próprio protocolo de pesquisa proprietário.

> [!Note]  
> A **pesquisa:** protocolo não substitui a pesquisa proprietária [-MS:](../search/-search-3x-wds-qryidx-searchms.md) Protocol. Os aplicativos ainda podem usar o protocolo **Search-MS:** para iniciar o Gerenciador de pesquisa de janelas ou para consultar silenciosamente o indexador do Windows Search.

 

Este tópico aborda o seguinte:

-   [Sintaxe](#syntax)
-   [Uso do Windows Vista com SP1 da pesquisa: protocolo](#windows-vista-with-sp1-use-of-the-search-protocol)
-   [Exemplos](#examples)
-   [Registrando o aplicativo que manipula o protocolo](#registering-the-application-that-handles-the-protocol)
    -   [Entradas do registro](#registry-entries)
-   [Tópicos relacionados](#related-topics)

## <a name="syntax"></a>Syntax

O protocolo de pesquisa usa a seguinte sintaxe padrão codificada por URL:


```C++
search:parameter=value[&parameter=value]&
```



A sintaxe começa identificando o próprio protocolo (**Search:**). Os pares de parâmetro/valor são argumentos passados para o mecanismo de pesquisa, conforme descrito na tabela a seguir, que mostra todos os parâmetros possíveis para a sintaxe do protocolo de pesquisa.



| Parâmetro                                              | Valor                                                         | Descrição                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consulta                                                  | Texto codificado por URL                                              | O texto da consulta inserido pelo usuário.                                                                                                                                                                                                                                                            |
| [InputLocale](search-protocol-localeidentifiers.md)   | Qualquer LCID (identificador de código de idioma) válido                     | O LCID que identifica o idioma de entrada para a consulta.                                                                                                                                                                                                                                     |
| [keywordlocale](search-protocol-localeidentifiers.md) | Qualquer LCID válido                                                | O LCID que identifica o idioma da versão internacional do indexador. O padrão é 1033 (en-US).                                                                                                                                                                                |
| [estrutural](search-protocol-crumb.md)                     | Instrução AQS                                                 | Esse argumento restringe o escopo que está sendo pesquisado. No Windows Vista, o protocolo de pesquisa dá suporte a AQS completas, bem como a uma implementação especial para um `location` argumento. No Windows XP, o protocolo de pesquisa também dá suporte a AQS completas, exceto para uma implementação especial do `kind` e do `store` . |
| [sintaxe](search-protocol-syntaxargument.md)           | NQS, AQS (não diferencia maiúsculas de minúsculas)                                 | A sintaxe de consulta a ser usada para pesquisar o índice: sintaxe de consulta natural ou sintaxe de consulta avançada (AQS). AQS é o padrão e sempre é presumido, analisado e suportado.                                                                                                                        |
| [stackedby](search-protocol-stackedby.md)             | Qualquer propriedade válida do sistema de propriedades                   | Uma propriedade que especifica a coluna pela qual os resultados são empilhados.                                                                                                                                                                                                                                      |
| [subquery](search-protocol-subquery.md)               | Um caminho totalmente especificado para um arquivo de pesquisa salvo ( \* . Search-MS) | Os resultados da subconsulta são usados como a origem da consulta. Ou seja, os termos de consulta são pesquisados em relação aos resultados da subconsulta.                                                                                                                                               |
| displayname                                            | Cadeia de caracteres codificada em URL                                            | O nome da pesquisa atual.                                                                                                                                                                                                                                                                |



 

## <a name="windows-vista-with-sp1-use-of-the-search-protocol"></a>Uso do Windows Vista com SP1 da pesquisa: protocolo

O Windows Vista com SP1 tem vários pontos de entrada dos quais ele chama o protocolo **Search:** . Esses pontos de entrada são descritos abaixo, bem como a sintaxe comum associada a cada um.



| Ponto de entrada de protocolo de pesquisa | Localização         | Consulta chamada                                                         |
|-----------------------------|------------------|----------------------------------------------------------------------|
| **Pesquisar em qualquer lugar**       | Menu **Iniciar**   | pesquisa: consulta =<*termo de pesquisa*>                                   |
| **Pesquisar em qualquer lugar**       | Windows Explorer | pesquisa: consulta =<*termo de pesquisa*>&trilha = local: <*local*> |
| Tecla de logotipo do Windows +F          | Qualquer lugar         | procurando                                                              |
| Ctrl+F                      | Windows Explorer | pesquisa: consulta =<*termo de pesquisa*>&trilha = local: <*local*> |
| F3                          | Menu **Iniciar**   | procurando                                                              |
| F3                          | Windows Explorer | pesquisa: consulta =<*termo de pesquisa*>&trilha = local: <*local*> |



 

Os pontos de entrada do protocolo de pesquisa do Windows Vista com SP1 não tiram proveito de todos os parâmetros possíveis no protocolo de pesquisa. Os aplicativos que se preocupam apenas com a manipulação de chamadas de protocolo de pesquisa do Windows Vista com SP1 podem usar a tabela a seguir como um guia para o mínimo que precisam ser implementados.



| Parâmetro                                              | Usado pelo Windows? | Como o Windows Vista com SP1 o utiliza ao chamar a pesquisa:                                                                                                                                                                                                                     |
|--------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Consulta                                                  | Yes              | O texto da consulta inserido pelo usuário.                                                                                                                                                                                                                                         |
| [estrutural](search-protocol-crumb.md)                     | Yes              | a [trilha](search-protocol-crumb.md) usa o `location` argumento para especificar de onde veio a consulta.                                                                                                                                                                       |
| [subquery](search-protocol-subquery.md)               | Yes              | Os resultados do argumento de [subconsulta](search-protocol-subquery.md) são usados como o escopo de itens a serem pesquisados. Normalmente, isso seria usado se um usuário estivesse usando um arquivo. Search-MS para pesquisar e, em seguida, chamado de aplicativo de pesquisa de desktop padrão de dentro dessa pesquisa. |
| [InputLocale](search-protocol-localeidentifiers.md)   | No               | Não usado no momento.                                                                                                                                                                                                                                                         |
| [keywordlocale](search-protocol-localeidentifiers.md) | No               | Não usado no momento.                                                                                                                                                                                                                                                         |
| [sintaxe](search-protocol-syntaxargument.md)           | No               | Não usado no momento.                                                                                                                                                                                                                                                         |
| [stackedby](search-protocol-stackedby.md)             | No               | Não usado no momento.                                                                                                                                                                                                                                                         |
| displayname                                            | No               | Não usado no momento.                                                                                                                                                                                                                                                         |



 

## <a name="examples"></a>Exemplos

Se um usuário digitar "Microsoft" no menu **Iniciar** e clicar em **Pesquisar em todos os lugares**, a chamada de protocolo de pesquisa resultante será feita:


```C++
search:query=microsoft&
```



Se um usuário digitar "Seattle" no Windows Explorer em C: \\ MyFolder e clicar em **Pesquisar em todos os lugares**, a chamada a seguir será feita, usando caracteres de escape para ': ' e ' \\ ':


```C++
search:query=seattle&crumb=location:C%3A%5CMyFolder
```



## <a name="registering-the-application-that-handles-the-protocol"></a>Registrando o aplicativo que manipula o protocolo

Como vários aplicativos podem disputar o protocolo de pesquisa, você deve registrar seu aplicativo com o recurso de [programas padrão](default-programs.md) durante a instalação para permitir que o usuário configure o padrão com mais facilidade. Além dos procedimentos de instalação normalmente praticado no Windows XP, um aplicativo baseado no Windows Vista deve se registrar com o recurso de programas padrão para que o aplicativo e os usuários possam configurar os padrões de forma direta.

Depois de instalar os arquivos binários necessários no computador do usuário, a rotina de instalação deve concluir estas tarefas gerais:

1.  Escreva ProgIDs para **o \_ \_ computador local hKey**, conforme descrito abaixo. Observe que os aplicativos devem criar ProgIDs específicos do aplicativo para o protocolo de pesquisa.
2.  Solicitar Associação de protocolo de pesquisa no nível da máquina.
3.  Registre o aplicativo com [programas padrão](default-programs.md), conforme explicado em [registrando um aplicativo para uso com programas padrão](default-programs.md), como um Contender para o protocolo de pesquisa.

### <a name="registry-entries"></a>Entradas do Registro

Veja a seguir exemplos das entradas de Registro necessárias para um aplicativo de pesquisa de área de trabalho fictício, pesquisa da contoso.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            URL Protocol = ""
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            DefaultIcon
               (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe,-7
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         contoso-search
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Contoso\Search\contososearch.exe %1
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Contoso Search = "Software\\Contoso\\Search\\Capabilities"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               ApplicationName = "Contoso Search Test App"
               ApplicationDescription = "Contoso search is a great new desktop search application"
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         Search
            Capabilities
               UrlAssociations
                  search = "contoso-search"
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de consulta avançada](../search/-search-3x-advancedquerysyntax.md)
</dt> <dt>

[Programas padrão](default-programs.md)
</dt> </dl>

 

 
