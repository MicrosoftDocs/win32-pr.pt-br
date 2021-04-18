---
title: Propriedade IWMPSettings invokeURLs
description: A propriedade invokeURLs Obtém ou define um valor que indica se os eventos de URL devem iniciar um navegador da Web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- Propriedade invokeURLs Windows Media Player
- Propriedade invokeURLs Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade invokeURLs
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798168"
---
# <a name="iwmpsettingsinvokeurls-property"></a><span data-ttu-id="fec24-106">Propriedade IWMPSettings:: invokeURLs</span><span class="sxs-lookup"><span data-stu-id="fec24-106">IWMPSettings::invokeURLs property</span></span>

<span data-ttu-id="fec24-107">A propriedade **invokeURLs** Obtém ou define um valor que indica se os eventos de URL devem iniciar um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="fec24-107">The **invokeURLs** property gets or sets a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="fec24-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fec24-108">Syntax</span></span>


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="fec24-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fec24-109">Property value</span></span>

<span data-ttu-id="fec24-110">Um valor **System. booliano** que indica se os eventos de URL devem iniciar um navegador da Web.</span><span class="sxs-lookup"><span data-stu-id="fec24-110">A **System.Boolean** value indicating whether URL events should launch a Web browser.</span></span> <span data-ttu-id="fec24-111">O padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="fec24-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec24-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="fec24-112">Remarks</span></span>

<span data-ttu-id="fec24-113">Os arquivos de mídia digital e os fluxos podem conter comandos de script de URL.</span><span class="sxs-lookup"><span data-stu-id="fec24-113">Digital media files and streams can contain URL script commands.</span></span> <span data-ttu-id="fec24-114">Quando um comando de script de URL é enviado ao controle do Windows Media Player, ele é passado primeiro para o manipulador de eventos **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** , independentemente do valor recuperado por **invokeURLs**.</span><span class="sxs-lookup"><span data-stu-id="fec24-114">When a URL script command is sent to the Windows Media Player control, it is passed first to the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event handler regardless of the value retrieved by **invokeURLs**.</span></span> <span data-ttu-id="fec24-115">Após o **\_ WMPOCXEvents \_ ScriptCommandEvent** sair, o Windows Media Player verifica **invokeURLs** para determinar se o navegador da Web padrão deve ser iniciado com a URL.</span><span class="sxs-lookup"><span data-stu-id="fec24-115">After **\_WMPOCXEvents\_ScriptCommandEvent** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Web browser with the URL.</span></span> <span data-ttu-id="fec24-116">Você pode exibir URLs seletivamente, verificando-as em **\_ WMPOCXEvents \_ ScriptCommandEvent** e configurando **invokeURLs** conforme desejado.</span><span class="sxs-lookup"><span data-stu-id="fec24-116">You can selectively display URLs by checking them in **\_WMPOCXEvents\_ScriptCommandEvent** and setting **invokeURLs** as desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec24-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec24-117">Requirements</span></span>



| <span data-ttu-id="fec24-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec24-118">Requirement</span></span> | <span data-ttu-id="fec24-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fec24-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec24-120">Versão</span><span class="sxs-lookup"><span data-stu-id="fec24-120">Version</span></span><br/>   | <span data-ttu-id="fec24-121">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="fec24-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fec24-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="fec24-122">Namespace</span></span><br/> | <span data-ttu-id="fec24-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fec24-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fec24-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="fec24-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fec24-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fec24-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec24-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="fec24-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec24-127">**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fec24-127">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="fec24-128">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="fec24-128">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





