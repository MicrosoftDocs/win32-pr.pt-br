---
title: Propriedade AxWindowsMediaPlayer. URL
description: A propriedade URL Obtém ou define o nome do item de mídia a ser reproduzido.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- Propriedade de URL Windows Media Player
- Propriedade de URL Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer do Windows Media Player, propriedade de URL
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811349"
---
# <a name="axwindowsmediaplayerurl-property"></a><span data-ttu-id="b320a-106">Propriedade AxWindowsMediaPlayer. URL</span><span class="sxs-lookup"><span data-stu-id="b320a-106">AxWindowsMediaPlayer.URL property</span></span>

<span data-ttu-id="b320a-107">A propriedade URL Obtém ou define o nome do item de mídia a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="b320a-107">The URL property gets or sets the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="b320a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b320a-108">Syntax</span></span>


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a><span data-ttu-id="b320a-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b320a-109">Property value</span></span>

<span data-ttu-id="b320a-110">Um System. String que é a URL do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="b320a-110">A System.String that is the URL of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b320a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b320a-111">Remarks</span></span>

<span data-ttu-id="b320a-112">Essa propriedade só pode ser definida como uma URL em uma zona de segurança que seja a mesma ou menos restritiva do que a zona de segurança do programa de chamada ou da página da Web.</span><span class="sxs-lookup"><span data-stu-id="b320a-112">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="b320a-113">Os aplicativos que abrirem itens de mídia atrás de um firewall terão um desempenho melhor se o endereço for especificado usando o nome DNS (servidor de nomes de domínio) em vez do endereço IP.</span><span class="sxs-lookup"><span data-stu-id="b320a-113">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="b320a-114">Não chame esse método do código do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="b320a-114">Do not call this method from event handler code.</span></span> <span data-ttu-id="b320a-115">A chamada de **URL** de um manipulador de eventos pode gerar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="b320a-115">Calling **URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="b320a-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b320a-116">Examples</span></span>

<span data-ttu-id="b320a-117">O exemplo a seguir permite que o usuário especifique um arquivo de mídia inserindo um caminho de arquivo em uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="b320a-117">The following example allows the user to specify a media file by entering a file path in a text box.</span></span> <span data-ttu-id="b320a-118">Quando um botão é clicado, a propriedade URL é definida como o arquivo especificado e o arquivo é reproduzido.</span><span class="sxs-lookup"><span data-stu-id="b320a-118">When a button is clicked, the URL property is set to the specified file and the file is played.</span></span> <span data-ttu-id="b320a-119">O objeto AxWMPLib. AxWindowsMediaPlayer é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="b320a-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b320a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b320a-120">Requirements</span></span>



| <span data-ttu-id="b320a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b320a-121">Requirement</span></span> | <span data-ttu-id="b320a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b320a-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b320a-123">Versão</span><span class="sxs-lookup"><span data-stu-id="b320a-123">Version</span></span><br/>   | <span data-ttu-id="b320a-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b320a-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b320a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="b320a-125">Namespace</span></span><br/> | <span data-ttu-id="b320a-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b320a-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b320a-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="b320a-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b320a-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b320a-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b320a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b320a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b320a-130">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b320a-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





