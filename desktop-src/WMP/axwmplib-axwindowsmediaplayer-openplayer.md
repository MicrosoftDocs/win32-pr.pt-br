---
title: Método AxWindowsMediaPlayer. openPlayer
description: O método openPlayer abre o Windows Media Player usando a URL especificada. | Método AxWindowsMediaPlayer. openPlayer
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- método openPlayer Windows Media Player
- método openPlayer Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, método openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813190"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a><span data-ttu-id="d7172-107">Método AxWindowsMediaPlayer. openPlayer</span><span class="sxs-lookup"><span data-stu-id="d7172-107">AxWindowsMediaPlayer.openPlayer method</span></span>

<span data-ttu-id="d7172-108">O método **openPlayer** abre o Windows Media Player usando a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="d7172-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7172-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7172-109">Syntax</span></span>


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="d7172-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7172-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7172-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="d7172-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="d7172-112">O **System. String** que é a URL do item de mídia a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="d7172-112">The **System.String** that is the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7172-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7172-113">Return value</span></span>

<span data-ttu-id="d7172-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d7172-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7172-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7172-115">Remarks</span></span>

<span data-ttu-id="d7172-116">Esse método inicia o Windows Media Player com a URL especificada definida como o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="d7172-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="d7172-117">Se o Player foi fechado anteriormente no modo de capa, ele será aberto usando a capa escolhida pela última vez pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d7172-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="d7172-118">Caso contrário, o Player será aberto no modo completo.</span><span class="sxs-lookup"><span data-stu-id="d7172-118">Otherwise, the Player opens in full mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7172-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7172-119">Requirements</span></span>



| <span data-ttu-id="d7172-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7172-120">Requirement</span></span> | <span data-ttu-id="d7172-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d7172-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7172-122">Versão</span><span class="sxs-lookup"><span data-stu-id="d7172-122">Version</span></span><br/>   | <span data-ttu-id="d7172-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="d7172-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d7172-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7172-124">Namespace</span></span><br/> | <span data-ttu-id="d7172-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d7172-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d7172-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="d7172-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d7172-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d7172-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7172-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7172-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7172-129">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d7172-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





