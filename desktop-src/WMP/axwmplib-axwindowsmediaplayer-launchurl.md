---
title: Método AxWindowsMediaPlayer. launchURL
description: O método launchURL envia uma URL para o navegador padrão do usuário a ser renderizado. | Método AxWindowsMediaPlayer. launchURL
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- método launchURL Windows Media Player
- método launchURL Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, método launchURL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781060"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a><span data-ttu-id="a1eb6-107">Método AxWindowsMediaPlayer. launchURL</span><span class="sxs-lookup"><span data-stu-id="a1eb6-107">AxWindowsMediaPlayer.launchURL method</span></span>

<span data-ttu-id="a1eb6-108">O método launchURL envia uma URL para o navegador padrão do usuário a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="a1eb6-108">The launchURL method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1eb6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1eb6-109">Syntax</span></span>


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="a1eb6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1eb6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1eb6-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="a1eb6-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="a1eb6-112">O **System. String** que é a URL a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="a1eb6-112">The **System.String** that is the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1eb6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1eb6-113">Return value</span></span>

<span data-ttu-id="a1eb6-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a1eb6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1eb6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1eb6-115">Remarks</span></span>

<span data-ttu-id="a1eb6-116">Esse método abre apenas as páginas da Web usando os protocolos HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a1eb6-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

## <a name="examples"></a><span data-ttu-id="a1eb6-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1eb6-117">Examples</span></span>

<span data-ttu-id="a1eb6-118">O exemplo a seguir cria um botão que, quando clicado, exibe o site da Microsoft em uma nova janela do navegador.</span><span class="sxs-lookup"><span data-stu-id="a1eb6-118">The following example creates a button that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="a1eb6-119">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="a1eb6-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="a1eb6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1eb6-120">Requirements</span></span>



| <span data-ttu-id="a1eb6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1eb6-121">Requirement</span></span> | <span data-ttu-id="a1eb6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a1eb6-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1eb6-123">Versão</span><span class="sxs-lookup"><span data-stu-id="a1eb6-123">Version</span></span><br/>   | <span data-ttu-id="a1eb6-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="a1eb6-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="a1eb6-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1eb6-125">Namespace</span></span><br/> | <span data-ttu-id="a1eb6-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="a1eb6-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="a1eb6-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="a1eb6-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a1eb6-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a1eb6-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1eb6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1eb6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1eb6-130">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a1eb6-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





