---
title: Método StringCollection. getItemInfo
description: O método getItemInfo recupera a cadeia de caracteres correspondente ao índice e nome do item StringCollection especificado.
ms.assetid: a031b91e-9d3b-47ac-bc5b-c111d5e3bc12
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, classe StringCollection
- Classe StringCollection Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- StringCollection.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c9552dcebbc7d565ebc797c62ac3bc00ee109fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812233"
---
# <a name="stringcollectiongetiteminfo-method"></a><span data-ttu-id="3e335-106">Método StringCollection. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="3e335-106">StringCollection.getItemInfo method</span></span>

<span data-ttu-id="3e335-107">O método **getItemInfo** recupera a cadeia de caracteres correspondente ao índice e nome do item **StringCollection** especificado.</span><span class="sxs-lookup"><span data-stu-id="3e335-107">The **getItemInfo** method retrieves the string corresponding to the specified **StringCollection** item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e335-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e335-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.getItemInfo(
  index,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="3e335-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e335-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e335-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3e335-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e335-111">**Número** (**longo**) especificando o índice de base zero do item **StringCollection** do qual obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="3e335-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="3e335-112">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3e335-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e335-113">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="3e335-113">**String** containing the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e335-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e335-114">Return value</span></span>

<span data-ttu-id="3e335-115">Esse método retorna uma **cadeia de caracteres** que representa o valor do atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="3e335-115">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="3e335-116">Para atributos cujo valor subjacente é **booliano**, ele retorna a cadeia de caracteres "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="3e335-116">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="3e335-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e335-117">Remarks</span></span>

<span data-ttu-id="3e335-118">Para recuperar atributos com vários valores e atributos com valores complexos, use o método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="3e335-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="3e335-119">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3e335-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3e335-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3e335-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e335-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e335-121">Requirements</span></span>



| <span data-ttu-id="3e335-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e335-122">Requirement</span></span> | <span data-ttu-id="3e335-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3e335-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e335-124">Versão</span><span class="sxs-lookup"><span data-stu-id="3e335-124">Version</span></span><br/> | <span data-ttu-id="3e335-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="3e335-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="3e335-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3e335-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="3e335-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e335-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e335-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e335-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e335-129">**StringCollection. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="3e335-129">**StringCollection.getItemInfoByType**</span></span>](stringcollection-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="3e335-130">**Objeto StringCollection**</span><span class="sxs-lookup"><span data-stu-id="3e335-130">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





