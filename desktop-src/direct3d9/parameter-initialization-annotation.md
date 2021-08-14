---
description: Use essa anotação para definir o conteúdo de um arquivo externo como o valor de inicialização de um parâmetro de efeito.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Anotação de inicialização de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d66d0cc18782d97a5a56c73ab12cd9222d33827930d60023fccf73cd2a8455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798649"
---
# <a name="parameter-initialization-annotation"></a>Anotação de inicialização de parâmetro

Use essa anotação para definir o conteúdo de um arquivo externo como o valor de inicialização de um parâmetro de efeito. Por exemplo:


```
string SasResourceAddress = "Value";
```



em que Value é uma cadeia de caracteres de texto ASCII que pode conter um caminho absoluto ou relativo. Um caminho relativo é relativo ao diretório que contém o arquivo de efeito.

Veja um exemplo:


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



O valor padrão é uma cadeia de caracteres vazia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de semântica e anotações padrão do DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



