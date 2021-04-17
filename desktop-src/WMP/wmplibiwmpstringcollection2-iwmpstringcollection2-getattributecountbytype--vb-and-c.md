---
title: Método IWMPStringCollection2 getAttributeCountByType
description: O método getAttributeCountByType retorna o número de atributos associados ao índice de coleção de cadeia de caracteres especificado, ao nome do atributo e ao idioma.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- método getAttributeCountByType Windows Media Player
- método getAttributeCountByType Windows Media Player, interface IWMPStringCollection2
- Interface IWMPStringCollection2 Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bb60fdd843fb3f45b6e4e3aff444a8a915fa0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780246"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a><span data-ttu-id="107e5-106">Método IWMPStringCollection2:: getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="107e5-106">IWMPStringCollection2::getAttributeCountByType method</span></span>

<span data-ttu-id="107e5-107">O método **getAttributeCountByType** retorna o número de atributos associados ao índice de coleção de cadeia de caracteres especificado, ao nome do atributo e ao idioma.</span><span class="sxs-lookup"><span data-stu-id="107e5-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified string collection index, attribute name, and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="107e5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="107e5-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="107e5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="107e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="107e5-110">*lCollectionIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="107e5-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="107e5-111">O **System. Int32** que especifica o índice de base zero do item de coleção de cadeia de caracteres a partir do qual obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="107e5-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="107e5-112">*bstrtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="107e5-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="107e5-113">O **System. String** que é o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="107e5-113">The **System.String** that is the name of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="107e5-114">*bstrLanguage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="107e5-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="107e5-115">O **System. String** que é o nome do idioma.</span><span class="sxs-lookup"><span data-stu-id="107e5-115">The **System.String** that is the name of the language.</span></span> <span data-ttu-id="107e5-116">Se o valor for definido como NULL ou para uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada.</span><span class="sxs-lookup"><span data-stu-id="107e5-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="107e5-117">Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="107e5-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="107e5-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="107e5-118">Return value</span></span>

<span data-ttu-id="107e5-119">O **System. Int32** que é a contagem.</span><span class="sxs-lookup"><span data-stu-id="107e5-119">The **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="107e5-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="107e5-120">Remarks</span></span>

<span data-ttu-id="107e5-121">Esse método é usado para descobrir o número de atributos correspondentes a um determinado nome de atributo para um determinado item **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="107e5-121">This method is used to discover the number of attributes corresponding to a particular attribute name for a given **StringCollection** item.</span></span> <span data-ttu-id="107e5-122">Os números de índice podem então ser passados para o quarto parâmetro do método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="107e5-122">Index numbers can then be passed to the fourth parameter of the **getItemInfoByType** method.</span></span>

<span data-ttu-id="107e5-123">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="107e5-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="107e5-124">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="107e5-124">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="107e5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="107e5-125">Requirements</span></span>



| <span data-ttu-id="107e5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="107e5-126">Requirement</span></span> | <span data-ttu-id="107e5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="107e5-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="107e5-128">Versão</span><span class="sxs-lookup"><span data-stu-id="107e5-128">Version</span></span><br/>   | <span data-ttu-id="107e5-129">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="107e5-129">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="107e5-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="107e5-130">Namespace</span></span><br/> | <span data-ttu-id="107e5-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="107e5-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="107e5-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="107e5-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="107e5-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="107e5-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="107e5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="107e5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107e5-135">**Interface IWMPStringCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="107e5-135">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="107e5-136">**IWMPStringCollection2. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="107e5-136">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





