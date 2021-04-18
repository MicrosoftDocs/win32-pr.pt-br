---
title: Método AxWindowsMediaPlayer. Close
description: O método Close fecha o arquivo de mídia digital atual, interrompe a reprodução no Windows Media Player e libera os recursos do Windows Media Player.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- fechar o método Windows Media Player
- método Close Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, método Close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800168"
---
# <a name="axwindowsmediaplayerclose-method"></a><span data-ttu-id="37a43-106">Método AxWindowsMediaPlayer. Close</span><span class="sxs-lookup"><span data-stu-id="37a43-106">AxWindowsMediaPlayer.close method</span></span>

<span data-ttu-id="37a43-107">O método Close fecha o arquivo de mídia digital atual, interrompe a reprodução no Windows Media Player e libera os recursos do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="37a43-107">The close method closes the current digital media file, stops playback in Windows Media Player and releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a43-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37a43-108">Syntax</span></span>


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a><span data-ttu-id="37a43-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37a43-109">Parameters</span></span>

<span data-ttu-id="37a43-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="37a43-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37a43-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37a43-111">Return value</span></span>

<span data-ttu-id="37a43-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="37a43-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37a43-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="37a43-113">Remarks</span></span>

<span data-ttu-id="37a43-114">Esse método fecha o arquivo de mídia digital atual, não o Windows Media Player em si.</span><span class="sxs-lookup"><span data-stu-id="37a43-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="37a43-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37a43-115">Examples</span></span>

<span data-ttu-id="37a43-116">O exemplo a seguir cria um botão que, quando clicado, interrompe a reprodução no Windows Media Player e libera os recursos em uso.</span><span class="sxs-lookup"><span data-stu-id="37a43-116">The following example creates a button that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="37a43-117">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="37a43-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="37a43-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37a43-118">Requirements</span></span>



| <span data-ttu-id="37a43-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="37a43-119">Requirement</span></span> | <span data-ttu-id="37a43-120">Valor</span><span class="sxs-lookup"><span data-stu-id="37a43-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a43-121">Versão</span><span class="sxs-lookup"><span data-stu-id="37a43-121">Version</span></span><br/>   | <span data-ttu-id="37a43-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="37a43-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="37a43-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="37a43-123">Namespace</span></span><br/> | <span data-ttu-id="37a43-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="37a43-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="37a43-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="37a43-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="37a43-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="37a43-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37a43-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="37a43-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a43-128">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="37a43-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





