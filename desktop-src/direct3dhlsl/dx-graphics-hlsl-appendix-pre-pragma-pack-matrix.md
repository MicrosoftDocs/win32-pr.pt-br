---
title: pack_matrix diretiva pragma
description: Diretiva pragma que especifica o alinhamento de empacotamento para matrizes.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix HLSL de diretiva pragma
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006543"
---
# <a name="pack_matrix-pragma-directive"></a><span data-ttu-id="34100-104">Diretiva de pragma de matriz de pacote \_</span><span class="sxs-lookup"><span data-stu-id="34100-104">pack\_matrix pragma Directive</span></span>

<span data-ttu-id="34100-105">Diretiva pragma que especifica o alinhamento de empacotamento para matrizes.</span><span class="sxs-lookup"><span data-stu-id="34100-105">Pragma directive that specifies packing alignment for matrices.</span></span>



| <span data-ttu-id="34100-106">\#\_matriz de pragma Pack ( *alinhamento* )</span><span class="sxs-lookup"><span data-stu-id="34100-106">\#pragma pack\_matrix( *alignment* )</span></span> |
|--------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="34100-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34100-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34100-108">Item</span><span class="sxs-lookup"><span data-stu-id="34100-108">Item</span></span></th>
<th><span data-ttu-id="34100-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="34100-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34100-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>sintonia</em></span><span class="sxs-lookup"><span data-stu-id="34100-110"><span id="alignment"></span><span id="ALIGNMENT"></span><em>alignment</em></span></span><br/></td>
<td><span data-ttu-id="34100-111">Alinhamento a ser definido para matrizes.</span><span class="sxs-lookup"><span data-stu-id="34100-111">Alignment to set for matrices.</span></span> <span data-ttu-id="34100-112">Esse parâmetro pode usar um dos valores listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="34100-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="34100-113">Valor</span><span class="sxs-lookup"><span data-stu-id="34100-113">Value</span></span></th>
<th><span data-ttu-id="34100-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="34100-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34100-115">column_major</span><span class="sxs-lookup"><span data-stu-id="34100-115">column_major</span></span></td>
<td><span data-ttu-id="34100-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="34100-116">Default.</span></span> <span data-ttu-id="34100-117">Define o alinhamento da embalagem de matriz para a coluna principal.</span><span class="sxs-lookup"><span data-stu-id="34100-117">Sets the matrix packing alignment to column major.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34100-118">row_major</span><span class="sxs-lookup"><span data-stu-id="34100-118">row_major</span></span></td>
<td><span data-ttu-id="34100-119">Define o alinhamento da embalagem de matriz para a linha principal.</span><span class="sxs-lookup"><span data-stu-id="34100-119">Sets the matrix packing alignment to row major.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="34100-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34100-120">Examples</span></span>

<span data-ttu-id="34100-121">O exemplo a seguir define o alinhamento da embalagem de matriz para a linha principal.</span><span class="sxs-lookup"><span data-stu-id="34100-121">The following example sets the matrix packing alignment to row major.</span></span>


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a><span data-ttu-id="34100-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="34100-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34100-123">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34100-123">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="34100-124">\#Diretiva pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="34100-124">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





