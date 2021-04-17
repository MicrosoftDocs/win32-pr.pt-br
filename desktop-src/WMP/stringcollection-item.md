---
title: Método StringCollection. Item
description: O método item recupera a cadeia de caracteres no índice especificado.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe StringCollection
- Classe StringCollection Windows Media Player, método item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780335"
---
# <a name="stringcollectionitem-method"></a><span data-ttu-id="2c6b7-106">Método StringCollection. Item</span><span class="sxs-lookup"><span data-stu-id="2c6b7-106">StringCollection.item method</span></span>

<span data-ttu-id="2c6b7-107">O método **Item** recupera a cadeia de caracteres no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2c6b7-107">The **item** method retrieves the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c6b7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c6b7-108">Syntax</span></span>


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="2c6b7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c6b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c6b7-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2c6b7-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c6b7-111">**Número** (**longo**) que contém o índice.</span><span class="sxs-lookup"><span data-stu-id="2c6b7-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c6b7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c6b7-112">Return value</span></span>

<span data-ttu-id="2c6b7-113">Esse método retorna uma **cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="2c6b7-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c6b7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c6b7-114">Remarks</span></span>

<span data-ttu-id="2c6b7-115">O objeto **StringCollection** é usado para recuperar o conjunto de valores disponíveis para um atributo.</span><span class="sxs-lookup"><span data-stu-id="2c6b7-115">The **StringCollection** object is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="2c6b7-116">Por exemplo, a *mediacollection*. o método **getAttributeStringCollection** pode ser usado para recuperar um objeto **StringCollection** que representa todos os valores do atributo gênero dentro do tipo de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="2c6b7-116">For example, the *MediaCollection*.**getAttributeStringCollection** method can be used to retrieve a **StringCollection** object representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="2c6b7-117">A propriedade **Item** pode então ser usada para iterar por todos os valores possíveis para o atributo gênero.</span><span class="sxs-lookup"><span data-stu-id="2c6b7-117">The **item** property can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="2c6b7-118">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2c6b7-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2c6b7-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2c6b7-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c6b7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c6b7-120">Requirements</span></span>



| <span data-ttu-id="2c6b7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c6b7-121">Requirement</span></span> | <span data-ttu-id="2c6b7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2c6b7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6b7-123">Versão</span><span class="sxs-lookup"><span data-stu-id="2c6b7-123">Version</span></span><br/> | <span data-ttu-id="2c6b7-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2c6b7-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2c6b7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2c6b7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c6b7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c6b7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c6b7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c6b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c6b7-128">**Mediacollection. getAttributeStringCollection**</span><span class="sxs-lookup"><span data-stu-id="2c6b7-128">**MediaCollection.getAttributeStringCollection**</span></span>](mediacollection-getattributestringcollection.md)
</dt> <dt>

[<span data-ttu-id="2c6b7-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2c6b7-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2c6b7-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2c6b7-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2c6b7-131">**Objeto StringCollection**</span><span class="sxs-lookup"><span data-stu-id="2c6b7-131">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





