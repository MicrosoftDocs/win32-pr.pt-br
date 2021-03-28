---
title: Tipo de vetor (HLSL)
description: Um vetor contém entre um e quatro componentes escalares; cada componente de um vetor deve ser do mesmo tipo.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Tipo de vetor HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "104989128"
---
# <a name="vector-type"></a><span data-ttu-id="6cd2f-104">Tipo de vetor</span><span class="sxs-lookup"><span data-stu-id="6cd2f-104">Vector Type</span></span>

<span data-ttu-id="6cd2f-105">Um vetor contém entre um e quatro componentes escalares; cada componente de um vetor deve ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="6cd2f-105">A vector contains between one and four scalar components; every component of a vector must be of the same type.</span></span>



|                     |
|---------------------|
| <span data-ttu-id="6cd2f-106">**Nome do TypeNumber**</span><span class="sxs-lookup"><span data-stu-id="6cd2f-106">**TypeNumber Name**</span></span> |



 


```
TypeComponents Name
```



## <a name="components"></a><span data-ttu-id="6cd2f-107">Componentes</span><span class="sxs-lookup"><span data-stu-id="6cd2f-107">Components</span></span>



| <span data-ttu-id="6cd2f-108">Item</span><span class="sxs-lookup"><span data-stu-id="6cd2f-108">Item</span></span>                                                                                                                             | <span data-ttu-id="6cd2f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cd2f-109">Description</span></span>                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd2f-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="6cd2f-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="6cd2f-111">Um único nome que contém duas partes.</span><span class="sxs-lookup"><span data-stu-id="6cd2f-111">A single name that contains two parts.</span></span> <span data-ttu-id="6cd2f-112">A primeira parte é um dos tipos [escalares](dx-graphics-hlsl-data-types.md) .</span><span class="sxs-lookup"><span data-stu-id="6cd2f-112">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="6cd2f-113">A segunda parte é o número de componentes, que deve estar entre 1 e 4, inclusive.</span><span class="sxs-lookup"><span data-stu-id="6cd2f-113">The second part is the number of components, which must be between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="6cd2f-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**</span><span class="sxs-lookup"><span data-stu-id="6cd2f-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="6cd2f-115">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável.</span><span class="sxs-lookup"><span data-stu-id="6cd2f-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                |



 

## <a name="examples"></a><span data-ttu-id="6cd2f-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6cd2f-116">Examples</span></span>

<span data-ttu-id="6cd2f-117">Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="6cd2f-117">Here are some examples:</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



<span data-ttu-id="6cd2f-118">Um vetor pode ser declarado usando essa sintaxe também:</span><span class="sxs-lookup"><span data-stu-id="6cd2f-118">A vector can be declared using this syntax also:</span></span>


```
vector <Type, Number> VariableName
```



<span data-ttu-id="6cd2f-119">Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="6cd2f-119">Here are some examples:</span></span>


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a><span data-ttu-id="6cd2f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cd2f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd2f-121">Tipos de dados (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6cd2f-121">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





