---
title: Método playlist. getItemInfo
description: O método getItemInfo recupera o valor de um atributo de playlist.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751511"
---
# <a name="playlistgetiteminfo-method"></a><span data-ttu-id="3e41d-106">Método playlist. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="3e41d-106">Playlist.getItemInfo method</span></span>

<span data-ttu-id="3e41d-107">O método **getItemInfo** recupera o valor de um atributo de playlist.</span><span class="sxs-lookup"><span data-stu-id="3e41d-107">The **getItemInfo** method retrieves the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e41d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e41d-108">Syntax</span></span>


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="3e41d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e41d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e41d-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3e41d-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e41d-111">**Cadeia de caracteres** que contém o nome do atributo a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="3e41d-111">**String** containing the name of the attribute to be retrieved.</span></span> <span data-ttu-id="3e41d-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="3e41d-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e41d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e41d-113">Return value</span></span>

<span data-ttu-id="3e41d-114">Esse método retorna uma **cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="3e41d-114">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e41d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e41d-115">Remarks</span></span>

<span data-ttu-id="3e41d-116">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3e41d-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="3e41d-117">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3e41d-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3e41d-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3e41d-118">Examples</span></span>

<span data-ttu-id="3e41d-119">Consulte a propriedade [attributeCount](playlist-attributecount.md) para obter o código de exemplo que usa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="3e41d-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e41d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e41d-120">Requirements</span></span>



| <span data-ttu-id="3e41d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e41d-121">Requirement</span></span> | <span data-ttu-id="3e41d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3e41d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3e41d-123">Versão</span><span class="sxs-lookup"><span data-stu-id="3e41d-123">Version</span></span><br/> | <span data-ttu-id="3e41d-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3e41d-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3e41d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3e41d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="3e41d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e41d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e41d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e41d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e41d-128">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="3e41d-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="3e41d-129">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="3e41d-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="3e41d-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3e41d-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3e41d-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3e41d-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





