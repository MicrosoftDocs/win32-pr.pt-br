---
title: Método IWMPMedia3 getAttributeCountByType
description: O método getAttributeCountByType retorna o número de atributos associados ao tipo de atributo especificado.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- método getAttributeCountByType Windows Media Player
- método getAttributeCountByType Windows Media Player, interface IWMPMedia3
- Interface IWMPMedia3 Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811777"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a><span data-ttu-id="ac3da-106">Método IWMPMedia3:: getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="ac3da-106">IWMPMedia3::getAttributeCountByType method</span></span>

<span data-ttu-id="ac3da-107">O método **getAttributeCountByType** retorna o número de atributos associados ao tipo de atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="ac3da-107">The **getAttributeCountByType** method returns the number of attributes associated with the specified attribute type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac3da-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac3da-108">Syntax</span></span>


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a><span data-ttu-id="ac3da-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac3da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac3da-110">*bstrtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac3da-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3da-111">Um **System. String** que é o tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="ac3da-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="ac3da-112">*bstrLanguage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac3da-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac3da-113">Um **System. String** que é o idioma.</span><span class="sxs-lookup"><span data-stu-id="ac3da-113">A **System.String** that is the language.</span></span> <span data-ttu-id="ac3da-114">Se o valor for definido como NULL ou uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada.</span><span class="sxs-lookup"><span data-stu-id="ac3da-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="ac3da-115">Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="ac3da-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac3da-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac3da-116">Return value</span></span>

<span data-ttu-id="ac3da-117">Um **System. Int32** que é a contagem de atributos que estão associados ao tipo.</span><span class="sxs-lookup"><span data-stu-id="ac3da-117">A **System.Int32** that is the count of attributes that are associated with the type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac3da-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac3da-118">Remarks</span></span>

<span data-ttu-id="ac3da-119">Esse método é usado para descobrir o número de atributos correspondentes a um nome de atributo específico para um determinado item de mídia.</span><span class="sxs-lookup"><span data-stu-id="ac3da-119">This method is used to discover the number of attributes corresponding to a particular attribute name for a given media item.</span></span> <span data-ttu-id="ac3da-120">Os números de índice podem então ser passados para o método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="ac3da-120">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="ac3da-121">Isso é útil, por exemplo, quando um item de mídia é categorizado em vários gêneros.</span><span class="sxs-lookup"><span data-stu-id="ac3da-121">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="ac3da-122">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ac3da-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="ac3da-123">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ac3da-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac3da-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac3da-124">Requirements</span></span>



| <span data-ttu-id="ac3da-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac3da-125">Requirement</span></span> | <span data-ttu-id="ac3da-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ac3da-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac3da-127">Versão</span><span class="sxs-lookup"><span data-stu-id="ac3da-127">Version</span></span><br/>   | <span data-ttu-id="ac3da-128">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ac3da-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ac3da-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac3da-129">Namespace</span></span><br/> | <span data-ttu-id="ac3da-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ac3da-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ac3da-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="ac3da-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ac3da-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ac3da-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac3da-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac3da-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac3da-134">**Interface IWMPMedia3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ac3da-134">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ac3da-135">**IWMPMedia3. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ac3da-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





