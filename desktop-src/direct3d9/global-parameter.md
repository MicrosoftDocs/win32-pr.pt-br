---
description: Cada efeito em conformidade com o DXSAS deve definir, no mínimo, um único parâmetro de efeito global com a semântica global.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Parâmetro global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105786317"
---
# <a name="global-parameter"></a>Parâmetro global

Cada efeito em conformidade com o DXSAS deve definir, no mínimo, um único parâmetro de efeito global com a semântica global. O parâmetro global também pode usar uma ou mais anotações opcionais. A sintaxe dela é a seguinte:


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



onde:

-   VariableName é um nome de variável de cadeia de caracteres de texto ASCII especificado pelo usuário.
-   SasGlobal é a palavra-chave semântica que identifica esse parâmetro como o parâmetro global DXSAS.
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

A única anotação necessária é SasVersion. Ela é declarada da seguinte maneira:


```
int3 SasVersion = { major, minor, revision };
```



onde:

-   principal indica a versão principal do DXSAS. As principais versões do DXSAS podem conter alterações de varredura no conjunto de semânticas e anotações definidas. A semântica e as anotações podem ser adicionadas e removidas e, em geral, a compatibilidade com versões anteriores não é garantida.
-   Minor indica a versão secundária SAS. As versões secundárias do DXSAS podem incluir a adição de novas semânticas ou anotações. Além disso, a semântica e as anotações podem ser marcadas como preteridas no padrão DXSAS. A semântica preterida e as anotações ainda devem ser suportadas por aplicativos host, mas podem emitir um diagnóstico de aviso quando essa semântica ou anotação é usada. Versões secundárias são compatíveis com versões anteriores.
-   revisão indica a revisão DXSAS. As revisões de DXSAS existem apenas como um meio de corrigir bugs, remover ambigüidade e refinar o padrão. As revisões para o padrão são compatíveis com versões anteriores.

A versão atual é a 1.0.0. Não há valor padrão para esta anotação.

## <a name="saseffectauthor"></a>SasEffectAuthor

Isso declara a pessoa que criou o efeito. Ela é declarada da seguinte maneira:


```
string SasEffectAuthor = "value";
```



em que value é uma cadeia de caracteres que identifica o autor do efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffectauthoringsoftware"></a>SasEffectAuthoringSoftware

Isso declara o software no qual o efeito foi criado. Ela é declarada da seguinte maneira:


```
string SasEffectAuthoringSoftware = "value";
```



em que value é uma cadeia de caracteres que identifica o efeito de criação de software. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffectcategory"></a>SasEffectCategory

Isso declara a categoria de efeito. Ela é declarada da seguinte maneira:


```
string SasEffectCategory = "value";
```



em que value é uma cadeia de caracteres que identifica a categoria de efeito. O padrão é uma cadeia de caracteres vazia. A categoria é expressa por meio de um valor do tipo caminho usando a barra como um delimitador. Os efeitos só podem pertencer a uma categoria, já que não há sintaxe para expressar a inclusão em vários caminhos em um único valor SasEffectCategory. O valor dessa anotação não é tratado como diferenciação de maiúsculas e minúsculas pelo aplicativo host.

## <a name="saseffectcompany"></a>SasEffectCompany

Isso declara a empresa que criou o efeito. Ela é declarada da seguinte maneira:


```
string SasEffectCompany = "value";
```



em que value é uma cadeia de caracteres que identifica o nome da empresa que possui o efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffectdescription"></a>SasEffectDescription

Isso descreve o efeito. Ela é declarada da seguinte maneira:


```
string SasEffectDescription = "value";
```



em que value é uma cadeia de caracteres que descreve o efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffecthelp"></a>SasEffectHelp

Essa é uma cadeia de caracteres de ajuda que pode ser exibida para o usuário sempre que a ajuda no efeito associado for solicitada. Ela é declarada da seguinte maneira:


```
string SasEffectHelp = "value";
```



em que value é uma cadeia de caracteres que pode ser exibida se o usuário solicitar ajuda. O padrão é uma cadeia de caracteres vazia.

## <a name="saseffectrevision"></a>SasEffectRevision

Essa anotação permite que as ferramentas e os usuários registrem o número de revisão do arquivo de efeito associado. Por exemplo, os usuários podiam inserir palavras-chave apropriadas no valor dessa anotação para invocar a substituição de palavra-chave em seu software de controle de revisão favorito. Ela é declarada da seguinte maneira:


```
string SasEffectRevision = "value";
```



em que value é uma cadeia de caracteres que identifica a revisão do efeito. O padrão é uma cadeia de caracteres vazia.

## <a name="examples"></a>Exemplos

Aqui está um exemplo que usa apenas a anotação única necessária:


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

 

 



