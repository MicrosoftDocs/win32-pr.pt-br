---
title: Propriedade DefaultFrame do IWMPSettings
description: A propriedade DefaultFrame Obtém ou define o nome do quadro usado para exibir uma URL recebida em um \_ evento AxWindowsMediaPlayer WMPOCXEvents \_ ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- Propriedade DefaultFrame do Windows Media Player
- Propriedade DefaultFrame do Windows Media Player, interface IWMPSettings
- Interface IWMPSettings do Windows Media Player, Propriedade DefaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815490"
---
# <a name="iwmpsettingsdefaultframe-property"></a><span data-ttu-id="2a7f0-106">IWMPSettings: Propriedade efaultFrame de:d</span><span class="sxs-lookup"><span data-stu-id="2a7f0-106">IWMPSettings::defaultFrame property</span></span>

<span data-ttu-id="2a7f0-107">A propriedade **DefaultFrame** Obtém ou define o nome do quadro usado para exibir uma URL recebida em um evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .</span><span class="sxs-lookup"><span data-stu-id="2a7f0-107">The **defaultFrame** property gets or sets the name of the frame used to display a URL that is received in an **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a7f0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a7f0-108">Syntax</span></span>


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a><span data-ttu-id="2a7f0-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2a7f0-109">Property value</span></span>

<span data-ttu-id="2a7f0-110">Um **System. String** que é o valor do atributo Name do elemento de **quadro** de destino.</span><span class="sxs-lookup"><span data-stu-id="2a7f0-110">A **System.String** that is the value of the name attribute of the target **FRAME** element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a7f0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a7f0-111">Remarks</span></span>

<span data-ttu-id="2a7f0-112">Se um quadro de destino for especificado no evento **\_ WMPOCXEvents \_ ScriptCommandEvent** em si, essa propriedade será ignorada.</span><span class="sxs-lookup"><span data-stu-id="2a7f0-112">If a target frame is specified in the **\_WMPOCXEvents\_ScriptCommandEvent** event itself, this property is ignored.</span></span>

<span data-ttu-id="2a7f0-113">Essa propriedade é ignorada ao usar o miniaplicativo Java do Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="2a7f0-113">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="2a7f0-114">No Netscape Navigator, cada comando de script de URL recebido exibirá a URL em uma nova janela do navegador, independentemente do valor de **DefaultFrame**.</span><span class="sxs-lookup"><span data-stu-id="2a7f0-114">In Netscape Navigator, each URL script command received will display the URL in a new browser window, regardless of the value of **defaultFrame**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a7f0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a7f0-115">Requirements</span></span>



| <span data-ttu-id="2a7f0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a7f0-116">Requirement</span></span> | <span data-ttu-id="2a7f0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2a7f0-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7f0-118">Versão</span><span class="sxs-lookup"><span data-stu-id="2a7f0-118">Version</span></span><br/>   | <span data-ttu-id="2a7f0-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="2a7f0-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2a7f0-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a7f0-120">Namespace</span></span><br/> | <span data-ttu-id="2a7f0-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2a7f0-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2a7f0-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="2a7f0-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2a7f0-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2a7f0-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a7f0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a7f0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7f0-125">**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2a7f0-125">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="2a7f0-126">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2a7f0-126">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





