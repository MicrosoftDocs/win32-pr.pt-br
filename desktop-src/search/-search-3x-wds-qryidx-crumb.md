---
description: Entenda como usar o argumento DEAD NO Windows Search como um meio de controlar o escopo de uma pesquisa.
ms.assetid: b0b974ae-0573-45e4-888e-07138604b62e
title: Argumento DEM (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ec64fdcf9b15e0b7c87ea2ff0b122e22a8f8917bbacb9d9c3c3da274123f607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463238"
---
# <a name="crumb-argument-windows-search"></a>Argumento DEM (Windows Search)

O argumento dá suporte a instruções completas de `crumb` AQS (Advanced Query Syntax) e é especialmente útil como um meio de controlar o escopo de uma pesquisa. Além dos parâmetros do AQS, o argumento pode usar um parâmetro especial no Windows Vista e e nos parâmetros no XP, conforme descrito `crumb` `location` `kind` `store` posteriormente neste tópico.

Este tópico é organizado da seguinte forma:

-   [Sintaxe de sintaxe de sintaxe de sintaxe](#crumb-syntax)
    -   [Exemplos gerais](#general-examples)
-   [Usando o mofando com o Vista (localização)](#using-crumb-with-vista-location)
    -   [Exemplos do Vista](#vista-examples)
    -   [Constantes para pastas comuns](#constants-for-common-folders)
-   [Usando o desa Windows XP (tipo e armazenamento)](#using-crumb-with-windows-xp-kind-and-store)
    -   [Exemplos do XP](#xp-examples)
-   [Tópicos relacionados](#related-topics)

 

## <a name="crumb-syntax"></a>Sintaxe de sintaxe de sintaxe de sintaxe

A sintaxe de sintaxe de sintaxe é a seguinte:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



A <column> parte é qualquer propriedade no sistema de propriedades e o <value> parte é um valor válido para essa propriedade. A <label> parte é um alias opcional para a propriedade que é exibida como uma dica de interface do usuário.

### <a name="general-examples"></a>Exemplos gerais


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



 

## <a name="using-crumb-with-vista-location"></a>Usando o mofando com o Vista (localização)

No parâmetro de sistema, Windows Vista dá suporte ao AQS completo e também à propriedade , que tem uma implementação especial disponível somente no `location` Windows Vista. Você pode usar uma cadeia de caracteres do AQS ou a propriedade dentro de um único parâmetro `location` de controle, mas não ambos. Se o parâmetro de desatrelação incluir o AQS, todo o resto nesse parâmetro de desatrelação será ignorado.

A `location` propriedade permite que você especifique um caminho a ser pesquisado. Windows O Vista poderá ignorar o Indexador e percorrer o diretório diretamente se o local estiver fora do escopo de rastreamento do Indexador. Consequentemente, essas pesquisas podem ser mais lentas do que as pesquisas que usam o Indexador.

Quando você especifica uma `location` propriedade, há suporte para dois parâmetros adicionais e opcionais:



| Parâmetro | Valores                  | Descrição                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inclusão | incluir, excluir        | Especifica se a consulta deve incluir ou excluir itens desse caminho. "Incluir" é o padrão. Windows O Vista não dá suporte a exclusões sem inclusões. (Veja o exemplo) |
| recursão | recursivo, não recursivo | Especifica se a pesquisa deve recursar todas as subpastas começando com o valor definido no local:<value>. "Recursivo" é o padrão.                             |



 

Para escopo de uma pesquisa usando o protocolo search-ms:, você tem opções diferentes, dependendo do destino do escopo.

Pasta em um computador local:

-   Usar o AQS (folder=folder:<caminho codificado por URL>)
-   Use o argumento location (encode=location:<caminho codificado por URL>)

Pasta em um computador/rede remoto:

-   Use o argumento location (encode=location:<caminho codificado por URL>)

Pasta acessada por meio de um manipulador de protocolo UNC conhecido:

-   Usar o AQS (agora= store: <UNC protocol handler name> )
-   Use o argumento location (encode=location:<caminho codificado por URL>)

### <a name="vista-examples"></a>Exemplos do Vista


```
search-ms:query=vacation&crumb=location:shell%3aPersonal,include,recursive&

search-ms:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 

search-ms:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



O primeiro exemplo executa uma pesquisa de "férias" começando no local shell://Personal (um atalho especial para a pasta Meus Documentos do usuário), incluindo essa pasta e todas as subpastas. Consulte a tabela abaixo.

O segundo exemplo executa uma pesquisa em C: \\ Imagens, mas não em C: \\ \\ Duplicatas de Imagens.

O terceiro exemplo executa uma pesquisa em C: Documentos, limitado a arquivos com a \\ propriedade kind definida como imagens.

### <a name="constants-for-common-folders"></a>Constantes para pastas comuns

Windows O Vista permite o uso de [valores KNOWNFOLDERID](/previous-versions//bb762584(v=vs.85)) que fornecem uma maneira exclusiva independente do sistema para identificar pastas especiais usadas com frequência por aplicativos, mas que podem não ter o mesmo nome ou local em qualquer sistema específico. Por exemplo, a pasta do sistema pode ser "C: Windows" em um \\ sistema e "C: \\ Winnt" em outro. Antes de Windows Vista, [CSIDLs eram usadas.](/windows/desktop/shell/csidl)

Use estes locais com esta sintaxe:


```
crumb=location:shell%3a<LocationName>&
```



 

## <a name="using-crumb-with-windows-xp-kind-and-store"></a>Usando o desa Windows XP (tipo e armazenamento)

Para Windows Pesquisar no Windows XP (WDS 3.x), os termos do AQS "kind" e "store" têm uma implementação especial. Os valores "kind" são os [mesmos valores usados no WDS 2.x.](../lwef/-search-2x-wds-perceivedtype.md) Os valores de "store" incluem o seguinte:

-   Mapi
-   file
-   outlookexpress
-   any

### <a name="xp-examples"></a>Exemplos do XP


```
search-ms:query=from:john&crumb=store:outlookexpress,OE%20Mail&
search-ms:query=from:john&crumb=kind:communications&
```



O primeiro exemplo retorna emails do Microsoft Outlook Express de John com o rótulo personalizado " OE Mail". O segundo exemplo executa uma pesquisa para qualquer comunicação de João.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com Parameter-Value argumentos](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argumentos do identificador de localidade](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Argumento SYNTAX](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argumento STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argumento SUBQUERY](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 
