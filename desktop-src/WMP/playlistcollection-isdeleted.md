---
title: Método playlistcollection. IsDeleted
description: O método IsDeleted recupera um valor que indica se a lista de reprodução especificada está na pasta itens excluídos.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- método IsDeleted Windows Media Player
- método IsDeleted Windows Media Player, classe Playlistcollection
- Classe playlistcollection Windows Media Player, método IsDeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765323"
---
# <a name="playlistcollectionisdeleted-method"></a><span data-ttu-id="758e1-106">Método playlistcollection. IsDeleted</span><span class="sxs-lookup"><span data-stu-id="758e1-106">PlaylistCollection.isDeleted method</span></span>

<span data-ttu-id="758e1-107">O método **IsDeleted** recupera um valor que indica se a lista de reprodução especificada está na pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="758e1-107">The **isDeleted** method retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="758e1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="758e1-108">Syntax</span></span>


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="758e1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="758e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="758e1-110">*lista de reprodução* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="758e1-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="758e1-111">O objeto de **playlist** a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="758e1-111">The **Playlist** object to be searched for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="758e1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="758e1-112">Return value</span></span>

<span data-ttu-id="758e1-113">Esse método retorna um **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="758e1-113">This method returns a **Boolean**.</span></span>

<span data-ttu-id="758e1-114">**Windows Media Player 10 Mobile**: esse método sempre retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="758e1-114">**Windows Media Player 10 Mobile**: This method always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="758e1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="758e1-115">Requirements</span></span>



| <span data-ttu-id="758e1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="758e1-116">Requirement</span></span> | <span data-ttu-id="758e1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="758e1-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="758e1-118">Versão</span><span class="sxs-lookup"><span data-stu-id="758e1-118">Version</span></span><br/> | <span data-ttu-id="758e1-119">Windows Media Player versão 7,0, Windows Media Player versão 7,1 ou Windows Media Player para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="758e1-119">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="758e1-120">Esse método não tem suporte no Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="758e1-120">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="758e1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="758e1-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="758e1-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="758e1-122"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="758e1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="758e1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758e1-124">**Objeto playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="758e1-124">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 





