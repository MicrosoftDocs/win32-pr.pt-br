---
title: Método StringCollection. getAttributeCountByType
description: O método getAttributeCountByType recupera o número de atributos associados ao índice do item StringCollection especificado, ao nome do atributo e ao idioma.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- método getAttributeCountByType Windows Media Player
- método getAttributeCountByType Windows Media Player, classe StringCollection
- Classe StringCollection Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811949"
---
# <a name="stringcollectiongetattributecountbytype-method"></a><span data-ttu-id="ed32a-106">Método StringCollection. getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="ed32a-106">StringCollection.getAttributeCountByType method</span></span>

<span data-ttu-id="ed32a-107">O método **getAttributeCountByType** recupera o número de atributos associados ao índice do item **StringCollection** especificado, ao nome do atributo e ao idioma.</span><span class="sxs-lookup"><span data-stu-id="ed32a-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified **StringCollection** item index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed32a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed32a-108">Syntax</span></span>


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="ed32a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed32a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed32a-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ed32a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed32a-111">**Número** (**longo**) especificando o índice de base zero do item **StringCollection** do qual obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="ed32a-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ed32a-112">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ed32a-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed32a-113">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="ed32a-113">**String** containing the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ed32a-114">*idioma* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ed32a-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed32a-115">**Cadeia de caracteres** que contém o idioma.</span><span class="sxs-lookup"><span data-stu-id="ed32a-115">**String** containing the language.</span></span> <span data-ttu-id="ed32a-116">Se o valor for definido como nulo ou a cadeia de caracteres vazia (""), a cadeia de caracteres de localidade atual será usada.</span><span class="sxs-lookup"><span data-stu-id="ed32a-116">If the value is set to null or the empty string (""), the current locale string is used.</span></span> <span data-ttu-id="ed32a-117">Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="ed32a-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed32a-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed32a-118">Return value</span></span>

<span data-ttu-id="ed32a-119">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="ed32a-119">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ed32a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed32a-120">Remarks</span></span>

<span data-ttu-id="ed32a-121">Esse método é usado para determinar o número de atributos correspondentes a um determinado nome de atributo para um determinado item **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="ed32a-121">This method is used to determine the number of attributes corresponding to a particular attribute name for a particular **StringCollection** item.</span></span> <span data-ttu-id="ed32a-122">Os números de índice podem então ser passados para o quarto parâmetro do método **StringCollection. getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="ed32a-122">Index numbers can then be passed to the fourth parameter of the **StringCollection.getItemInfoByType** method.</span></span>

<span data-ttu-id="ed32a-123">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ed32a-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ed32a-124">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ed32a-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed32a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed32a-125">Requirements</span></span>



| <span data-ttu-id="ed32a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed32a-126">Requirement</span></span> | <span data-ttu-id="ed32a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ed32a-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed32a-128">Versão</span><span class="sxs-lookup"><span data-stu-id="ed32a-128">Version</span></span><br/> | <span data-ttu-id="ed32a-129">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ed32a-129">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="ed32a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ed32a-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="ed32a-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed32a-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed32a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed32a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed32a-133">**Objeto StringCollection**</span><span class="sxs-lookup"><span data-stu-id="ed32a-133">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





