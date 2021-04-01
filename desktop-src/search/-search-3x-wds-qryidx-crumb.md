---
description: O argumento de trilha dá suporte a instruções de AQS (sintaxe de consulta avançada completa) e é especialmente útil como meio de controlar o escopo de uma pesquisa.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argumento de trilha (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f36764174e0eecaedee4a9c360bb9d7dabca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090094"
---
# <a name="crumb-argument-windows-search"></a>Argumento de trilha (pesquisa do Windows)

O `crumb` argumento oferece suporte a instruções AQS (sintaxe de consulta avançada completa) e é especialmente útil como meio de controlar o escopo de uma pesquisa. Além de AQS ements, o `crumb` argumento pode usar um parâmetro especial `location` no Windows Vista e `kind` `store` parâmetros no XP, conforme descrito posteriormente neste tópico.

Este tópico é organizado da seguinte maneira:

-   [Sintaxe de trilha](#crumb-syntax)
    -   [Exemplos gerais](#general-examples)
-   [Usando a trilha com o Vista (local)](#using-crumb-with-vista-location)
    -   [Exemplos do vista](#vista-examples)
    -   [Constantes para pastas comuns](#constants-for-common-folders)
-   [Usando a trilha com o Windows XP (tipo e loja)](#using-crumb-with-windows-xp-kind-and-store)
    -   [Exemplos do XP](#xp-examples)
-   [Tópicos relacionados](#related-topics)

 

## <a name="crumb-syntax"></a>Sintaxe de trilha

A sintaxe de trilha é a seguinte:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



A <column> parte é qualquer propriedade no sistema de propriedades e o <value> a parte é um valor válido para essa propriedade. A <label> parte é um alias opcional para a propriedade que é exibido como uma dica de interface do usuário.

### <a name="general-examples"></a>Exemplos gerais


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Usando a trilha com o Vista (local)

No parâmetro de trilha, o Windows Vista dá suporte ao AQS completo e também à `location` propriedade, que tem uma implementação especial disponível apenas no Windows Vista. Você pode usar uma cadeia de caracteres AQS ou a `location` propriedade dentro de um único parâmetro de trilha, mas não ambos. Se o parâmetro de trilha incluir AQS, todo o restante nesse parâmetro de trilha será ignorado.

A `location` propriedade permite que você especifique um caminho para pesquisar. O Windows Vista pode ignorar o indexador e atravessar o diretório diretamente se o local estiver fora do escopo de rastreamento do indexador. Consequentemente, essas pesquisas podem ser mais lentas do que as pesquisas que usam o indexador.

Quando você especifica uma `location` propriedade, dois parâmetros adicionais têm suporte e são opcionais:



| Parâmetro | Valores                  | Descrição                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inclusão | incluir, excluir        | Especifica se a consulta deve incluir ou excluir itens desse caminho. "Include" é o padrão. O Windows Vista não oferece suporte a exclusões sem inclusões. (Veja o exemplo) |
| recursão | recursivo, nonrecursive | Especifica se a pesquisa deve recurse todas as subpastas começando com o valor definido no local:<value>. "Recursivo" é o padrão.                             |



 

Para fazer o escopo de uma pesquisa usando o protocolo Search-MS:, você tem opções diferentes, dependendo do destino do escopo.

Pasta em um computador local:

-   Use AQS (trilha = pasta: <caminho codificado de URL>)
-   Usar o argumento de local (trilha = local: <caminho codificado de URL>)

Pasta em um computador/rede remota:

-   Usar o argumento de local (trilha = local: <caminho codificado de URL>)

Pasta acessada por meio de um manipulador de protocolo UNC conhecido:

-   Use AQS (trilha = armazenamento: <UNC protocol handler name> )
-   Usar o argumento de local (trilha = local: <caminho codificado de URL>)

### <a name="vista-examples"></a>Exemplos do vista


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



O primeiro exemplo executa uma pesquisa por "férias" começando no local shell://Personal (um atalho especial para a pasta meus documentos do usuário), incluindo essa pasta e todas as subpastas. Consulte a tabela abaixo.

O segundo exemplo executa uma pesquisa em C: \\ Pictures, mas não em c: \\ imagens \\ duplicatas.

O terceiro exemplo executa uma pesquisa em C: \\ Documents, limitada a arquivos com a propriedade Kind definida como pics.

### <a name="constants-for-common-folders"></a>Constantes para pastas comuns

O Windows Vista permite o uso de valores [KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) que fornecem uma maneira exclusiva independente do sistema de identificar pastas especiais usadas frequentemente por aplicativos, mas que podem não ter o mesmo nome ou local em um determinado sistema. Por exemplo, a pasta do sistema pode ser "C: \\ Windows" em um sistema e "c: \\ WinNT" em outro. Antes do Windows Vista, foram usadas [CSIDLs](/windows/desktop/shell/csidl) .

Use esses locais com esta sintaxe:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Usando a trilha com o Windows XP (tipo e loja)

Para o Windows Search no Windows XP (WDS 3. x), os termos de AQS "Kind" e "Store" têm uma implementação especial. Os valores de "Kind" são os mesmos [valores usados no WDS 2. x](../lwef/-search-2x-wds-perceivedtype.md). Os valores de "Store" incluem o seguinte:

-   MAPI
-   arquivo
-   outlookexpress
-   any

### <a name="xp-examples"></a>Exemplos do XP


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



O primeiro exemplo retorna emails do Microsoft Outlook Express de João com o rótulo personalizado "OE Mail". O segundo exemplo executa uma pesquisa para qualquer comunicação de João.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com argumentos de Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumentos do identificador de localidade](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argumento de sintaxe](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argumento de subconsulta](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
