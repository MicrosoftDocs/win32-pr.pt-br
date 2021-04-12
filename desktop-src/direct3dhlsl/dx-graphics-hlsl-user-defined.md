---
title: Tipo definido pelo usuário
description: Use a sintaxe a seguir para declarar um tipo definido pelo usuário.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363796"
---
# <a name="user-defined-type"></a><span data-ttu-id="6b140-103">Tipo definido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="6b140-103">User-Defined Type</span></span>

<span data-ttu-id="6b140-104">Use a sintaxe a seguir para declarar um tipo definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6b140-104">Use the following syntax to declare a user-defined type.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="6b140-105">**\[ \] \[ índice \] de nome de tipo de constante** de typedef;</span><span class="sxs-lookup"><span data-stu-id="6b140-105">typedef **\[const\] Type Name\[Index\]**;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="6b140-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b140-106">Parameters</span></span>



| <span data-ttu-id="6b140-107">Item</span><span class="sxs-lookup"><span data-stu-id="6b140-107">Item</span></span>                                                                                         | <span data-ttu-id="6b140-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b140-108">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b140-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span><span class="sxs-lookup"><span data-stu-id="6b140-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span></span><br/>                 | <span data-ttu-id="6b140-110">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6b140-110">Optional.</span></span> <span data-ttu-id="6b140-111">Essa palavra-chave marca explicitamente o tipo como uma constante.</span><span class="sxs-lookup"><span data-stu-id="6b140-111">This keyword explicitly marks the type as a constant.</span></span><br/>             |
| <span data-ttu-id="6b140-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Escreva**</span><span class="sxs-lookup"><span data-stu-id="6b140-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="6b140-113">Identifica o tipo de dados; deve ser um dos tipos de dados intrínsecos HLSL.</span><span class="sxs-lookup"><span data-stu-id="6b140-113">Identifies the data type; must be one of the HLSL intrinsic data types.</span></span><br/>     |
| <span data-ttu-id="6b140-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="6b140-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="6b140-115">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="6b140-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="6b140-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**</span><span class="sxs-lookup"><span data-stu-id="6b140-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**</span></span><br/> | <span data-ttu-id="6b140-117">Tamanho de matriz opcional.</span><span class="sxs-lookup"><span data-stu-id="6b140-117">Optional array size.</span></span> <span data-ttu-id="6b140-118">Deve ser um inteiro sem sinal entre 1 e 4, inclusive.</span><span class="sxs-lookup"><span data-stu-id="6b140-118">Must be an unsigned integer between 1 and 4 inclusive.</span></span><br/> |



 

<span data-ttu-id="6b140-119">Além dos tipos de dados intrínsecos internos, o HLSL dá suporte a tipos definidos pelo usuário ou personalizados que seguem essa sintaxe:</span><span class="sxs-lookup"><span data-stu-id="6b140-119">In addition to the built-in intrinsic data types, HLSL supports user-defined or custom types which follow this syntax:</span></span>

## <a name="remarks"></a><span data-ttu-id="6b140-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b140-120">Remarks</span></span>

<span data-ttu-id="6b140-121">Os tipos definidos pelo usuário não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6b140-121">User-defined types are not case-sensitive.</span></span> <span data-ttu-id="6b140-122">Para sua conveniência, os tipos a seguir são definidos automaticamente em escopo superglobal.</span><span class="sxs-lookup"><span data-stu-id="6b140-122">For convenience, the following types are automatically defined at super-global scope.</span></span>


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



<span data-ttu-id="6b140-123">O sinal de sustenido ( \# ) representa um dígito inteiro entre 1 e 4.</span><span class="sxs-lookup"><span data-stu-id="6b140-123">The pound sign (\#) represents an integer digit between 1 and 4.</span></span>

<span data-ttu-id="6b140-124">Para compatibilidade com os efeitos do DirectX 8, os seguintes tipos são definidos automaticamente em escopo superglobal:</span><span class="sxs-lookup"><span data-stu-id="6b140-124">For compatibility with DirectX 8 effects, the following types are automatically defined at super-global scope:</span></span>


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a><span data-ttu-id="6b140-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b140-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b140-126">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6b140-126">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





