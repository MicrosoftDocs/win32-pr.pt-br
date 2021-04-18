---
title: Método playlist. setItemInfo
description: O método setItemInfo especifica o valor de um atributo de playlist.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- método setItemInfo Windows Media Player
- método setItemInfo Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813658"
---
# <a name="playlistsetiteminfo-method"></a><span data-ttu-id="aef13-106">Método playlist. setItemInfo</span><span class="sxs-lookup"><span data-stu-id="aef13-106">Playlist.setItemInfo method</span></span>

<span data-ttu-id="aef13-107">O método **setItemInfo** especifica o valor de um atributo de playlist.</span><span class="sxs-lookup"><span data-stu-id="aef13-107">The **setItemInfo** method specifies the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef13-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aef13-108">Syntax</span></span>


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="aef13-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aef13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef13-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="aef13-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aef13-111">**Cadeia de caracteres** que contém o nome do atributo a ser definido.</span><span class="sxs-lookup"><span data-stu-id="aef13-111">**String** containing the name of the attribute to be set.</span></span> <span data-ttu-id="aef13-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="aef13-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="aef13-113">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="aef13-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aef13-114">**Cadeia de caracteres** que contém o novo valor para o atributo.</span><span class="sxs-lookup"><span data-stu-id="aef13-114">**String** containing the new value for the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef13-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aef13-115">Return value</span></span>

<span data-ttu-id="aef13-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="aef13-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aef13-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="aef13-117">Remarks</span></span>

<span data-ttu-id="aef13-118">Um uso especial do método **setItemInfo** é classificar os itens na lista de reprodução usando o atributo SortAttribute.</span><span class="sxs-lookup"><span data-stu-id="aef13-118">A special use of the **setItemInfo** method is to sort the items in the playlist by using the SortAttribute attribute.</span></span> <span data-ttu-id="aef13-119">O exemplo de JScript a seguir classifica uma lista de reprodução pelos valores do atributo UserLastPlayedTime.</span><span class="sxs-lookup"><span data-stu-id="aef13-119">The following JScript example sorts a playlist by the values of the UserLastPlayedTime attribute.</span></span> <span data-ttu-id="aef13-120">A playlist de variável é uma referência a um objeto de **playlist** .</span><span class="sxs-lookup"><span data-stu-id="aef13-120">The variable playlist is a reference to a **Playlist** object.</span></span>


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



<span data-ttu-id="aef13-121">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="aef13-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="aef13-122">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="aef13-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="aef13-123">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="aef13-123">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="aef13-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aef13-124">Examples</span></span>

<span data-ttu-id="aef13-125">Consulte a propriedade [attributeCount](playlist-attributecount.md) para obter o código de exemplo que usa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="aef13-125">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef13-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aef13-126">Requirements</span></span>



| <span data-ttu-id="aef13-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="aef13-127">Requirement</span></span> | <span data-ttu-id="aef13-128">Valor</span><span class="sxs-lookup"><span data-stu-id="aef13-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aef13-129">Versão</span><span class="sxs-lookup"><span data-stu-id="aef13-129">Version</span></span><br/> | <span data-ttu-id="aef13-130">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="aef13-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="aef13-131">DLL</span><span class="sxs-lookup"><span data-stu-id="aef13-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="aef13-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aef13-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef13-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="aef13-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef13-134">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="aef13-134">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="aef13-135">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="aef13-135">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="aef13-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="aef13-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="aef13-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="aef13-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





