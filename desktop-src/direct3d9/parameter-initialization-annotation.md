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
# <a name="parameter-initialization-annotation"></a><span data-ttu-id="4f9e9-103">Anotação de inicialização de parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f9e9-103">Parameter Initialization Annotation</span></span>

<span data-ttu-id="4f9e9-104">Use esta anotação para definir o conteúdo de um arquivo externo como o valor de inicialização para um parâmetro de efeito.</span><span class="sxs-lookup"><span data-stu-id="4f9e9-104">Use this annotation to define the contents of an external file as the initialization value for an effect parameter.</span></span> <span data-ttu-id="4f9e9-105">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4f9e9-105">For example:</span></span>


```
string SasResourceAddress = "Value";
```



<span data-ttu-id="4f9e9-106">em que value é uma cadeia de caracteres de texto ASCII que pode conter um caminho absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="4f9e9-106">where Value is an ASCII text string that may contain an absolute or relative path.</span></span> <span data-ttu-id="4f9e9-107">Um caminho relativo é relativo ao diretório que contém o arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="4f9e9-107">A relative path is relative to the directory that contains the effect file.</span></span>

<span data-ttu-id="4f9e9-108">Veja um exemplo:</span><span class="sxs-lookup"><span data-stu-id="4f9e9-108">Here is an example:</span></span>


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



<span data-ttu-id="4f9e9-109">O valor padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="4f9e9-109">The default value is an empty string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f9e9-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f9e9-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f9e9-111">Referência de semântica e anotações padrão do DirectX</span><span class="sxs-lookup"><span data-stu-id="4f9e9-111">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



