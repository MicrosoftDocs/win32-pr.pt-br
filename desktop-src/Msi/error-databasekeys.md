---
description: A propriedade DatabaseKeys somente leitura do objeto de erro retorna uma coleção de cadeias de caracteres que contém as chaves primárias da linha do banco de dados causando o erro. Há uma chave por entrada na coleção.
ms.assetid: 416a6cef-4c70-4c06-a8d2-801c9440e25a
title: Propriedade Error. DatabaseKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.DatabaseKeys
- IMsmError.get_DatabaseKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c0de387c0101e7b79e64486089abcbd49f5d60d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748778"
---
# <a name="errordatabasekeys-property"></a><span data-ttu-id="f1569-104">Propriedade Error. DatabaseKeys</span><span class="sxs-lookup"><span data-stu-id="f1569-104">Error.DatabaseKeys property</span></span>

<span data-ttu-id="f1569-105">A propriedade **DatabaseKeys** somente leitura do objeto de [**erro**](error-object.md) retorna uma coleção de cadeias de caracteres que contém as chaves primárias da linha do banco de dados causando o erro.</span><span class="sxs-lookup"><span data-stu-id="f1569-105">The read-only **DatabaseKeys** property of the [**Error**](error-object.md) object returns a string collection that contains the primary keys of the database row causing the error.</span></span> <span data-ttu-id="f1569-106">Há uma chave por entrada na coleção.</span><span class="sxs-lookup"><span data-stu-id="f1569-106">There is one key per entry in the collection.</span></span>

<span data-ttu-id="f1569-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f1569-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1569-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1569-108">Syntax</span></span>


```JScript
propVal = Error.DatabaseKeys
```



## <a name="property-value"></a><span data-ttu-id="f1569-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f1569-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f1569-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1569-110">Remarks</span></span>

<span data-ttu-id="f1569-111">O cliente é responsável por liberar a coleção de cadeias de caracteres quando ela não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="f1569-111">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="f1569-112">A coleção estará vazia se os valores não se aplicarem ao tipo do erro.</span><span class="sxs-lookup"><span data-stu-id="f1569-112">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="f1569-113">Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="f1569-113">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="f1569-114">C++</span><span class="sxs-lookup"><span data-stu-id="f1569-114">C++</span></span>

<span data-ttu-id="f1569-115">Consulte [**obter \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) a função DatabaseKeys.</span><span class="sxs-lookup"><span data-stu-id="f1569-115">See [**get\_DatabaseKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_databasekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1569-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1569-116">Requirements</span></span>



| <span data-ttu-id="f1569-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1569-117">Requirement</span></span> | <span data-ttu-id="f1569-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f1569-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1569-119">Versão</span><span class="sxs-lookup"><span data-stu-id="f1569-119">Version</span></span><br/> | <span data-ttu-id="f1569-120">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f1569-120">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="f1569-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1569-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f1569-122"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1569-122"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1569-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f1569-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f1569-124"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1569-124"><dt>Mergemod.dll</dt></span></span> </dl> |



 

