---
title: Propriedade AxWindowsMediaPlayer. windowlessVideo
description: A propriedade windowlessVideo Obtém ou define um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- Propriedade windowlessVideo Windows Media Player
- Propriedade windowlessVideo Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade windowlessVideo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759739"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a><span data-ttu-id="b4a12-106">Propriedade AxWindowsMediaPlayer. windowlessVideo</span><span class="sxs-lookup"><span data-stu-id="b4a12-106">AxWindowsMediaPlayer.windowlessVideo property</span></span>

<span data-ttu-id="b4a12-107">A propriedade windowlessVideo Obtém ou define um valor que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="b4a12-107">The windowlessVideo property gets or sets a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a12-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4a12-108">Syntax</span></span>


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="b4a12-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b4a12-109">Property value</span></span>

<span data-ttu-id="b4a12-110">Um valor System. booliano que indica se o controle do Windows Media Player renderiza o vídeo no modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="b4a12-110">A System.Boolean value indicating whether the Windows Media Player control renders video in windowless mode.</span></span> <span data-ttu-id="b4a12-111">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="b4a12-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a12-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4a12-112">Remarks</span></span>

<span data-ttu-id="b4a12-113">Por padrão, um controle do Windows Media Player inserido renderiza o vídeo em sua própria janela dentro da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="b4a12-113">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="b4a12-114">Quando **windowlessVideo** é definido como true, o objeto do Windows Media Player renderiza o vídeo diretamente na área do cliente, para que você possa aplicar efeitos especiais ou colocar em camadas o vídeo com texto.</span><span class="sxs-lookup"><span data-stu-id="b4a12-114">When **windowlessVideo** is set to true, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="b4a12-115">No Windows Vista, o vídeo de renderização no modo sem janela pode prejudicar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="b4a12-115">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="b4a12-116">Não há suporte para a obtenção de um valor para essa propriedade no Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="b4a12-116">Getting a value for this property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="b4a12-117">Definir um valor para essa propriedade no Netscape Navigator pode gerar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="b4a12-117">Setting a value for this property in Netscape Navigator may yield unexpected results.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a12-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a12-118">Requirements</span></span>



| <span data-ttu-id="b4a12-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a12-119">Requirement</span></span> | <span data-ttu-id="b4a12-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b4a12-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a12-121">Versão</span><span class="sxs-lookup"><span data-stu-id="b4a12-121">Version</span></span><br/>   | <span data-ttu-id="b4a12-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b4a12-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b4a12-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4a12-123">Namespace</span></span><br/> | <span data-ttu-id="b4a12-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b4a12-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b4a12-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="b4a12-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b4a12-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b4a12-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a12-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4a12-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a12-128">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b4a12-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





