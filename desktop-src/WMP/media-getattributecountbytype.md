---
title: Método Media. getAttributeCountByType
description: O método getAttributeCountByType recupera o número de atributos associados ao nome de atributo e idioma especificados.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- método getAttributeCountByType Windows Media Player
- método getAttributeCountByType Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613dca43c32322cd5e7de2b2b04605789009cbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763207"
---
# <a name="mediagetattributecountbytype-method"></a><span data-ttu-id="20c58-106">Método Media. getAttributeCountByType</span><span class="sxs-lookup"><span data-stu-id="20c58-106">Media.getAttributeCountByType method</span></span>

<span data-ttu-id="20c58-107">O método **getAttributeCountByType** recupera o número de atributos associados ao nome de atributo e idioma especificados.</span><span class="sxs-lookup"><span data-stu-id="20c58-107">The **getAttributeCountByType** method retrieves the number of attributes associated with the specified attribute name and language.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c58-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20c58-108">Syntax</span></span>


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a><span data-ttu-id="20c58-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20c58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20c58-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="20c58-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c58-111">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="20c58-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="20c58-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="20c58-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="20c58-113">*idioma* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="20c58-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20c58-114">**Cadeia de caracteres** que representa o idioma.</span><span class="sxs-lookup"><span data-stu-id="20c58-114">**String** representing the language.</span></span> <span data-ttu-id="20c58-115">Se o valor for definido como nulo ou "" (cadeia de caracteres vazia), a cadeia de caracteres de localidade atual será usada.</span><span class="sxs-lookup"><span data-stu-id="20c58-115">If the value is set to null or "" (empty string), the current locale string is used.</span></span> <span data-ttu-id="20c58-116">Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="20c58-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20c58-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20c58-117">Return value</span></span>

<span data-ttu-id="20c58-118">Esse método retorna um **número** (**longo**) que contém a contagem de atributos.</span><span class="sxs-lookup"><span data-stu-id="20c58-118">This method returns a **Number** (**long**) containing the attribute count.</span></span>

## <a name="remarks"></a><span data-ttu-id="20c58-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="20c58-119">Remarks</span></span>

<span data-ttu-id="20c58-120">Esse método é usado para determinar o número de atributos que correspondem a um determinado nome de atributo para um determinado objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="20c58-120">This method is used to determine the number of attributes corresponding to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="20c58-121">Os números de índice podem então ser passados para o método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="20c58-121">Index numbers can then be passed to the **getItemInfoByType** method.</span></span> <span data-ttu-id="20c58-122">Isso é útil, por exemplo, quando um item de mídia é categorizado em vários gêneros.</span><span class="sxs-lookup"><span data-stu-id="20c58-122">This is useful, for example, when a media item has been categorized under multiple genres.</span></span>

<span data-ttu-id="20c58-123">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="20c58-123">To use this method, read access to the library is required.</span></span> <span data-ttu-id="20c58-124">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="20c58-124">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="20c58-125">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.</span><span class="sxs-lookup"><span data-stu-id="20c58-125">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="20c58-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20c58-126">Requirements</span></span>



| <span data-ttu-id="20c58-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="20c58-127">Requirement</span></span> | <span data-ttu-id="20c58-128">Valor</span><span class="sxs-lookup"><span data-stu-id="20c58-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20c58-129">Versão</span><span class="sxs-lookup"><span data-stu-id="20c58-129">Version</span></span><br/> | <span data-ttu-id="20c58-130">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="20c58-130">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="20c58-131">DLL</span><span class="sxs-lookup"><span data-stu-id="20c58-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="20c58-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20c58-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20c58-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="20c58-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c58-134">**Mediaobject**</span><span class="sxs-lookup"><span data-stu-id="20c58-134">**MediaObject**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="20c58-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="20c58-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="20c58-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="20c58-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="20c58-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="20c58-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





