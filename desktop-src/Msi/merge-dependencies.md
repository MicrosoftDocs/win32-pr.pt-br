---
description: A propriedade de dependências somente leitura do objeto de mesclagem retorna uma coleção de objetos de dependência que enumera um conjunto de dependências não atendidas para o banco de dados atual.
ms.assetid: d7081ffe-3d9e-486e-84b6-b45e92fff5f0
title: Propriedade Merge. Dependencies (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Dependencies
- IMsmMerge.get_Dependencies
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4c92d24ac2172b0d14de8e0609a407f2a0808494
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750608"
---
# <a name="mergedependencies-property"></a><span data-ttu-id="d84e2-103">Propriedade Merge. Dependencies</span><span class="sxs-lookup"><span data-stu-id="d84e2-103">Merge.Dependencies property</span></span>

<span data-ttu-id="d84e2-104">A propriedade de **dependências** somente leitura do objeto de [**mesclagem**](merge-object.md) retorna uma coleção de objetos de [**dependência**](dependency-object.md) que enumera um conjunto de dependências não atendidas para o banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="d84e2-104">The read-only **Dependencies** property of the [**Merge**](merge-object.md) object returns a collection of [**Dependency**](dependency-object.md) objects that enumerates a set of unsatisfied dependencies for the current database.</span></span>

<span data-ttu-id="d84e2-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d84e2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d84e2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d84e2-106">Syntax</span></span>


```JScript
propVal = Merge.Dependencies
```



## <a name="property-value"></a><span data-ttu-id="d84e2-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d84e2-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d84e2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d84e2-108">Remarks</span></span>

<span data-ttu-id="d84e2-109">Um módulo não precisa estar aberto para recuperar informações de dependência.</span><span class="sxs-lookup"><span data-stu-id="d84e2-109">A module does not need to be open to retrieve dependency information.</span></span>

### <a name="c"></a><span data-ttu-id="d84e2-110">C++</span><span class="sxs-lookup"><span data-stu-id="d84e2-110">C++</span></span>

<span data-ttu-id="d84e2-111">Consulte a função [**obter \_ dependências**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) .</span><span class="sxs-lookup"><span data-stu-id="d84e2-111">See [**get\_Dependencies**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_dependencies) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d84e2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d84e2-112">Requirements</span></span>



| <span data-ttu-id="d84e2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d84e2-113">Requirement</span></span> | <span data-ttu-id="d84e2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d84e2-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d84e2-115">Versão</span><span class="sxs-lookup"><span data-stu-id="d84e2-115">Version</span></span><br/> | <span data-ttu-id="d84e2-116">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d84e2-116">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="d84e2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d84e2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d84e2-118"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="d84e2-118"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="d84e2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d84e2-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="d84e2-120"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d84e2-120"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
