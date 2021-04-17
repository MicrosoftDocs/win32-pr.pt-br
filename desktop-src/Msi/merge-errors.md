---
description: A propriedade de erros somente leitura do objeto de mesclagem retorna uma coleção de objetos de erro que é o conjunto atual de erros.
ms.assetid: 619f17cc-131a-4262-ad48-9ab1318142aa
title: Propriedade Merge. Errors (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Errors
- IMsmMerge.get_Errors
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9f07bdbba9fecf48001aed1fbcd42e02abb5c5c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750803"
---
# <a name="mergeerrors-property"></a><span data-ttu-id="dea6f-103">Propriedade Merge. Errors</span><span class="sxs-lookup"><span data-stu-id="dea6f-103">Merge.Errors property</span></span>

<span data-ttu-id="dea6f-104">A propriedade de **erros** somente leitura do objeto de [**mesclagem**](merge-object.md) retorna uma coleção de objetos de [**erro**](error-object.md) que é o conjunto atual de erros.</span><span class="sxs-lookup"><span data-stu-id="dea6f-104">The read-only **Errors** property of the [**Merge**](merge-object.md) object returns a collection of [**Error**](error-object.md) objects that is the current set of errors.</span></span>

<span data-ttu-id="dea6f-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="dea6f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea6f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dea6f-106">Syntax</span></span>


```JScript
propVal = Merge.Errors
```



## <a name="property-value"></a><span data-ttu-id="dea6f-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dea6f-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="dea6f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="dea6f-108">Remarks</span></span>

<span data-ttu-id="dea6f-109">A recuperação não é destrutiva.</span><span class="sxs-lookup"><span data-stu-id="dea6f-109">The retrieval is non-destructive.</span></span> <span data-ttu-id="dea6f-110">Várias instâncias da coleção de erros podem ser recuperadas chamando esse método repetidamente.</span><span class="sxs-lookup"><span data-stu-id="dea6f-110">Multiple instances of the error collection may be retrieved by repeatedly calling this method.</span></span>

### <a name="c"></a><span data-ttu-id="dea6f-111">C++</span><span class="sxs-lookup"><span data-stu-id="dea6f-111">C++</span></span>

<span data-ttu-id="dea6f-112">Consulte a função [**obter \_ erros**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) .</span><span class="sxs-lookup"><span data-stu-id="dea6f-112">See [**get\_Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) Function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dea6f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea6f-113">Requirements</span></span>



| <span data-ttu-id="dea6f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea6f-114">Requirement</span></span> | <span data-ttu-id="dea6f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dea6f-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dea6f-116">Versão</span><span class="sxs-lookup"><span data-stu-id="dea6f-116">Version</span></span><br/> | <span data-ttu-id="dea6f-117">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="dea6f-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="dea6f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dea6f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dea6f-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea6f-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="dea6f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dea6f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="dea6f-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dea6f-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
