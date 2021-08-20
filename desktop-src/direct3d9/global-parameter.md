---
description: Cada efeito em conformidade com DXSAS deve definir, no mínimo, um único parâmetro de efeito global com a semântica global.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Parâmetro global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4dc0a1337505cec30960ca12fa91ed692b9de9434e702c3fb03829e89ab46d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094767"
---
# <a name="global-parameter"></a>Parâmetro global

Cada efeito em conformidade com DXSAS deve definir, no mínimo, um único parâmetro de efeito global com a semântica global. O parâmetro global também pode usar uma ou mais anotações opcionais. A sintaxe dela é a seguinte:


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



em que:

-   VariableName é um nome de variável de cadeia de caracteres de texto ASCII especificado pelo usuário.
-   SasGlobal é a palavra-chave semântica que identifica esse parâmetro como o parâmetro DXSAS global.
-   SasVersion é a única anotação necessária.
-   OptionalAnnotations pode incluir o seguinte:
    -   [SasEffectAuthor](#saseffectauthor)
    -   [SasEffectAuthoringSoftware](#saseffectauthoringsoftware)
    -   [SasEffectCategory](#saseffectcategory)
    -   [SasEffectCompany](#saseffectcompany)
    -   [SasEffectDescription](#saseffectdescription)
    -   [SasEffectHelp](#saseffecthelp)
    -   [SasEffectRevision](#saseffectrevision)

## <a name="sasversion"></a>SasVersion

A única anotação necessária é SasVersion. Ele é declarado desta forma:


```
int3 SasVersion = { major, minor, revision };
```



em que:

-   principal indica a versão principal do DXSAS. As principais versões do DXSAS podem conter alterações de limpeza no conjunto de semânticas e anotações definidas. A semântica e as anotações podem ser adicionadas e removidas e, em geral, a compatibilidade com versões anteriores não é garantida.
-   secundária indica a versão secundária da SAS. As versões secundárias do DXSAS podem incluir a adição de novas semânticas ou anotações. Além disso, a semântica e as anotações podem ser marcadas como preterida no padrão DXSAS. A semântica e as anotações preterida ainda devem ser suportadas por aplicativos host, mas podem emitir um diagnóstico de aviso quando essa semântica ou anotação é usada. As versões secundárias são compatíveis com versões anteriores.
-   revision indica a revisão DXSAS. As revisões de DXSAS existem apenas como um meio de corrigir bugs, remover ambiguidade e refinar o padrão. As revisões para o padrão são compatíveis com versões anteriores.

A versão atual é 1.0.0. Não há nenhum valor padrão para essa anotação.

## <a name="saseffectauthor"></a>SasEffectAuthor

Isso declara a pessoa que criou o efeito. Ele é declarado desta forma:


```
string SasEffectAuthor = "value";
```



em que value é uma cadeia de caracteres que identifica o autor do efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffectauthoringsoftware"></a>SasEffectAuthoringSoftware

Isso declara o software em que o efeito foi autor. Ele é declarado desta forma:


```
string SasEffectAuthoringSoftware = "value";
```



em que value é uma cadeia de caracteres que identifica o software de autor do efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffectcategory"></a>SasEffectCategory

Isso declara a categoria de efeito. Ele é declarado desta forma:


```
string SasEffectCategory = "value";
```



em que value é uma cadeia de caracteres que identifica a categoria de efeito. O padrão é uma cadeia de caracteres vazia. A categoria é expressa por meio de um valor de caminho usando a barra como um delimiter. Os efeitos só podem pertencer a uma categoria, pois não há sintaxe para expressar a inclusão em vários caminhos dentro de um único valor SasEffectCategory. O valor dessa anotação não é tratado como sensível a minúsculas pelo aplicativo host.

## <a name="saseffectcompany"></a>SasEffectCompany

Isso declara a empresa que criou o efeito. Ele é declarado desta forma:


```
string SasEffectCompany = "value";
```



em que value é uma cadeia de caracteres que identifica o nome da empresa que possui o efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffectdescription"></a>SasEffectDescription

Isso descreve o efeito. Ele é declarado desta forma:


```
string SasEffectDescription = "value";
```



em que value é uma cadeia de caracteres que descreve o efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffecthelp"></a>SasEffectHelp

Essa é uma cadeia de caracteres de ajuda que pode ser exibida ao usuário sempre que a ajuda sobre o efeito associado é solicitada. Ele é declarado desta forma:


```
string SasEffectHelp = "value";
```



em que value é uma cadeia de caracteres que pode ser exibida se o usuário solicitar ajuda. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffectrevision"></a>SasEffectRevision

Essa anotação permite que ferramentas e usuários gravem o número de revisão do arquivo de efeito associado. Por exemplo, os usuários podem inserir palavras-chave apropriadas no valor dessa anotação para invocar a substituição de palavra-chave em seu software de controle de revisão favorito. Ele é declarado desta forma:


```
string SasEffectRevision = "value";
```



em que value é uma cadeia de caracteres que identifica a revisão de efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="examples"></a>Exemplos

Aqui está um exemplo que usa apenas a anotação única e necessária:


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



Aqui está um exemplo que usa a anotação necessária e várias anotações opcionais:


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de semântica e anotações padrão do DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



