---
title: Propriedade AxWindowsMediaPlayer. versionInfo
description: A propriedade versionInfo Obtém um valor que especifica a versão do Windows Media Player.
ms.assetid: e128bec5-1ae9-4710-800e-4f97df362909
keywords:
- Propriedade versionInfo Windows Media Player
- Propriedade versionInfo Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, Propriedade versionInfo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.versionInfo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f759c2aedb19e21c4b7d90f3634141e4c37ec8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762099"
---
# <a name="axwindowsmediaplayerversioninfo-property"></a><span data-ttu-id="c8f4e-106">Propriedade AxWindowsMediaPlayer. versionInfo</span><span class="sxs-lookup"><span data-stu-id="c8f4e-106">AxWindowsMediaPlayer.versionInfo property</span></span>

<span data-ttu-id="c8f4e-107">A propriedade versionInfo Obtém um valor que especifica a versão do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-107">The versionInfo property gets a value that specifies the version of the Windows Media Player.</span></span>

<span data-ttu-id="c8f4e-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f4e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8f4e-109">Syntax</span></span>


```CSharp
public System.String versionInfo {get;}
```


```VB

Public ReadOnly Property versionInfo As System.String
```





## <a name="property-value"></a><span data-ttu-id="c8f4e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c8f4e-110">Property value</span></span>

<span data-ttu-id="c8f4e-111">Um System. String que é a informação de versão no seguinte formato: "*X*. 0,0. *Aaaa*", em que *X* representa o número de versão principal e *yyyy* representa o número de Build.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-111">A System.String that is the version information in the following format: "*X*.0.0.*YYYY*" where *X* represents the major version number and *YYYY* represents the build number.</span></span>

## <a name="examples"></a><span data-ttu-id="c8f4e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8f4e-112">Examples</span></span>

<span data-ttu-id="c8f4e-113">O exemplo a seguir cria um botão que, quando clicado, exibe uma caixa de mensagem contendo as informações de versão do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-113">The following example creates a button that, when clicked, displays a message box containing the version information for Windows Media Player.</span></span> <span data-ttu-id="c8f4e-114">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="c8f4e-114">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void showVersion_Click(object sender, System.EventArgs e)
{
    // Build the message containing the version info. 
    string message = ("Windows Media Player Version: " + player.versionInfo);

    // Display the message. 
    System.Windows.Forms.MessageBox.Show(message);
}
```


```VB

Public Sub showVersion_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showVersion.Click

    &#39; Build the message containing the version info. 
    Dim message As String = (&quot;Windows Media Player Version: &quot; + player.versionInfo)

    &#39; Display the message. 
    System.Windows.Forms.MessageBox.Show(message)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c8f4e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8f4e-115">Requirements</span></span>



| <span data-ttu-id="c8f4e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8f4e-116">Requirement</span></span> | <span data-ttu-id="c8f4e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c8f4e-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f4e-118">Versão</span><span class="sxs-lookup"><span data-stu-id="c8f4e-118">Version</span></span><br/>   | <span data-ttu-id="c8f4e-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="c8f4e-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c8f4e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8f4e-120">Namespace</span></span><br/> | <span data-ttu-id="c8f4e-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c8f4e-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c8f4e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="c8f4e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c8f4e-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f4e-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f4e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8f4e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f4e-125">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c8f4e-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





