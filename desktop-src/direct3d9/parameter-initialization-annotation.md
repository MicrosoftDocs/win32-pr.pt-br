---
description: Use esta anotação para definir o conteúdo de um arquivo externo como o valor de inicialização para um parâmetro de efeito.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Anotação de inicialização de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163717"
---
# <a name="parameter-initialization-annotation"></a>Anotação de inicialização de parâmetro

Use esta anotação para definir o conteúdo de um arquivo externo como o valor de inicialização para um parâmetro de efeito. Por exemplo:


```
string SasResourceAddress = "Value";
```



em que value é uma cadeia de caracteres de texto ASCII que pode conter um caminho absoluto ou relativo. Um caminho relativo é relativo ao diretório que contém o arquivo de efeito.

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

 

 



