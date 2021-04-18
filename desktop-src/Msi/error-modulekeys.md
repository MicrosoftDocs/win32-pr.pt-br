---
description: A propriedade ModuleKeys somente leitura do objeto de erro retorna um ponteiro para uma coleção de cadeias de caracteres que contém as chaves primárias da linha no módulo que está causando o erro, uma chave por entrada na coleção.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Propriedade Error. ModuleKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752044"
---
# <a name="errormodulekeys-property"></a><span data-ttu-id="a56f1-103">Propriedade Error. ModuleKeys</span><span class="sxs-lookup"><span data-stu-id="a56f1-103">Error.ModuleKeys property</span></span>

<span data-ttu-id="a56f1-104">A propriedade **ModuleKeys** somente leitura do objeto de [**erro**](error-object.md) retorna um ponteiro para uma coleção de cadeias de caracteres que contém as chaves primárias da linha no módulo que está causando o erro, uma chave por entrada na coleção.</span><span class="sxs-lookup"><span data-stu-id="a56f1-104">The read-only **ModuleKeys** property of the [**Error**](error-object.md) object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.</span></span>

<span data-ttu-id="a56f1-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a56f1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a56f1-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a56f1-106">Syntax</span></span>


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a><span data-ttu-id="a56f1-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a56f1-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a56f1-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a56f1-108">Remarks</span></span>

<span data-ttu-id="a56f1-109">O cliente é responsável por liberar a coleção de cadeias de caracteres quando ela não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="a56f1-109">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="a56f1-110">A coleção estará vazia se os valores não se aplicarem ao tipo do erro.</span><span class="sxs-lookup"><span data-stu-id="a56f1-110">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="a56f1-111">Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="a56f1-111">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="a56f1-112">C++</span><span class="sxs-lookup"><span data-stu-id="a56f1-112">C++</span></span>

<span data-ttu-id="a56f1-113">Consulte [**obter \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) a função ModuleKeys.</span><span class="sxs-lookup"><span data-stu-id="a56f1-113">See [**get\_ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a56f1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a56f1-114">Requirements</span></span>



| <span data-ttu-id="a56f1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a56f1-115">Requirement</span></span> | <span data-ttu-id="a56f1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a56f1-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a56f1-117">Versão</span><span class="sxs-lookup"><span data-stu-id="a56f1-117">Version</span></span><br/> | <span data-ttu-id="a56f1-118">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a56f1-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="a56f1-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a56f1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a56f1-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="a56f1-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="a56f1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a56f1-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a56f1-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a56f1-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

