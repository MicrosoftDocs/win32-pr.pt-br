---
title: Método AxWindowsMediaPlayer. newMedia
description: O método newMedia retorna uma interface IWMPMedia para um novo item de mídia.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- método newMedia Windows Media Player
- método newMedia Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, método newMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784915"
---
# <a name="axwindowsmediaplayernewmedia-method"></a><span data-ttu-id="2beb0-106">Método AxWindowsMediaPlayer. newMedia</span><span class="sxs-lookup"><span data-stu-id="2beb0-106">AxWindowsMediaPlayer.newMedia method</span></span>

<span data-ttu-id="2beb0-107">O método newMedia retorna uma interface IWMPMedia para um novo item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2beb0-107">The newMedia method returns an IWMPMedia interface for a new media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="2beb0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2beb0-108">Syntax</span></span>


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a><span data-ttu-id="2beb0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2beb0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2beb0-110">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="2beb0-110">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="2beb0-111">Um **System. String** que é a URL do arquivo de mídia digital usado para inicializar o novo item de mídia.</span><span class="sxs-lookup"><span data-stu-id="2beb0-111">A **System.String** that is the URL of the digital media file that is used to initialize the new media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2beb0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2beb0-112">Return value</span></span>

<span data-ttu-id="2beb0-113">Uma interface WMPLib. IWMPMedia que representa o item de mídia recém-criado.</span><span class="sxs-lookup"><span data-stu-id="2beb0-113">A WMPLib.IWMPMedia interface that represents the newly created media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="2beb0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2beb0-114">Remarks</span></span>

<span data-ttu-id="2beb0-115">O parâmetro *bstrURL* não deve ser uma cadeia de caracteres de comprimento zero ("") ou NULL.</span><span class="sxs-lookup"><span data-stu-id="2beb0-115">The *bstrURL* parameter must not be a zero-length string ("") or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="2beb0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2beb0-116">Requirements</span></span>



| <span data-ttu-id="2beb0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2beb0-117">Requirement</span></span> | <span data-ttu-id="2beb0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2beb0-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2beb0-119">Versão</span><span class="sxs-lookup"><span data-stu-id="2beb0-119">Version</span></span><br/>   | <span data-ttu-id="2beb0-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="2beb0-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2beb0-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="2beb0-121">Namespace</span></span><br/> | <span data-ttu-id="2beb0-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2beb0-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2beb0-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="2beb0-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2beb0-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2beb0-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2beb0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2beb0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2beb0-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2beb0-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2beb0-127">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2beb0-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





