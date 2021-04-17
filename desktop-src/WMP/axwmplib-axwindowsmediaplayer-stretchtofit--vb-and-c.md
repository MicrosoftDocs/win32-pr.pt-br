---
title: Propriedade AxWindowsMediaPlayer. stretchToFit
description: A propriedade stretchToFit Obtém ou define um valor que indica se o vídeo exibido pelo controle do Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Propriedade stretchToFit Windows Media Player
- Propriedade stretchToFit Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade stretchToFit
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759740"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a><span data-ttu-id="b997c-106">Propriedade AxWindowsMediaPlayer. stretchToFit</span><span class="sxs-lookup"><span data-stu-id="b997c-106">AxWindowsMediaPlayer.stretchToFit property</span></span>

<span data-ttu-id="b997c-107">A propriedade stretchToFit Obtém ou define um valor que indica se o vídeo exibido pelo controle do Windows Media Player é dimensionado automaticamente para se ajustar à janela de vídeo, quando a janela de vídeo é maior do que as dimensões da imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b997c-107">The stretchToFit property gets or sets a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="b997c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b997c-108">Syntax</span></span>


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="b997c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b997c-109">Property value</span></span>

<span data-ttu-id="b997c-110">O valor System. Boolean que indica se o vídeo será alongado para se ajustar à janela.</span><span class="sxs-lookup"><span data-stu-id="b997c-110">The System.Boolean value that indicates whether the video will stretch to fit the window.</span></span> <span data-ttu-id="b997c-111">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="b997c-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="b997c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b997c-112">Remarks</span></span>

<span data-ttu-id="b997c-113">Quando **stretchToFit** é definido como true, o controle do Windows Media Player mantém a taxa de proporção original do vídeo.</span><span class="sxs-lookup"><span data-stu-id="b997c-113">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="b997c-114">Se a taxa de proporção do vídeo não corresponder à taxa de proporção da janela de vídeo, as áreas de máscara preta poderão aparecer na parte superior e inferior, ou à esquerda e à direita da imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b997c-114">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="b997c-115">Essa propriedade se aplica ao controle do Windows Media Player somente quando ele é inserido em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="b997c-115">This property applies to the Windows Media Player control only when it is embedded in a webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="b997c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b997c-116">Requirements</span></span>



| <span data-ttu-id="b997c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b997c-117">Requirement</span></span> | <span data-ttu-id="b997c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b997c-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b997c-119">Versão</span><span class="sxs-lookup"><span data-stu-id="b997c-119">Version</span></span><br/>   | <span data-ttu-id="b997c-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b997c-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b997c-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="b997c-121">Namespace</span></span><br/> | <span data-ttu-id="b997c-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b997c-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b997c-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="b997c-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b997c-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b997c-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b997c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b997c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b997c-126">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b997c-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





