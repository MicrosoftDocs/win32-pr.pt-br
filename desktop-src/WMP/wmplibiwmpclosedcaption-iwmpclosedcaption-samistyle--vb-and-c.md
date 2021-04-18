---
title: Propriedade SAMIstyle IWMPClosedCaption
description: A propriedade SAMIstyle Obtém ou define o estilo de legendagem oculta.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Propriedade SAMIstyle Windows Media Player
- Propriedade SAMIstyle Windows Media Player, interface IWMPClosedCaption
- Interface IWMPClosedCaption Windows Media Player, Propriedade SAMIstyle
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751133"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a><span data-ttu-id="60e14-106">Propriedade IWMPClosedCaption:: SAMIstyle</span><span class="sxs-lookup"><span data-stu-id="60e14-106">IWMPClosedCaption::SAMIStyle property</span></span>

<span data-ttu-id="60e14-107">A propriedade **samistyle** Obtém ou define o estilo de legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="60e14-107">The **SAMIStyle** property gets or sets the closed captioning style.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e14-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="60e14-108">Syntax</span></span>


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a><span data-ttu-id="60e14-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="60e14-109">Property value</span></span>

<span data-ttu-id="60e14-110">O **System. String** que é o nome especificado no identificador de estilo de um arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="60e14-110">The **System.String** that is the name specified in the style identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="60e14-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="60e14-111">Remarks</span></span>

<span data-ttu-id="60e14-112">Um arquivo SAMI pode conter várias definições de estilo de formato.</span><span class="sxs-lookup"><span data-stu-id="60e14-112">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="60e14-113">Os estilos SAMI são definidos entre as marcas <STYLE> e </STYLE> no arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="60e14-113">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="60e14-114">Um estilo é definido com uma cadeia de caracteres de texto precedida por um \# caractere.</span><span class="sxs-lookup"><span data-stu-id="60e14-114">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="60e14-115">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="60e14-115">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



<span data-ttu-id="60e14-116">Isso especifica um estilo que produz uma fonte específica.</span><span class="sxs-lookup"><span data-stu-id="60e14-116">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="60e14-117">Se nenhum estilo SAMI for especificado, o primeiro estilo definido no arquivo SAMI será usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="60e14-117">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="60e14-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60e14-118">Requirements</span></span>



| <span data-ttu-id="60e14-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="60e14-119">Requirement</span></span> | <span data-ttu-id="60e14-120">Valor</span><span class="sxs-lookup"><span data-stu-id="60e14-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e14-121">Versão</span><span class="sxs-lookup"><span data-stu-id="60e14-121">Version</span></span><br/>   | <span data-ttu-id="60e14-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="60e14-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="60e14-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="60e14-123">Namespace</span></span><br/> | <span data-ttu-id="60e14-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="60e14-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="60e14-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="60e14-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="60e14-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="60e14-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60e14-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="60e14-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e14-128">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="60e14-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="60e14-129">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="60e14-129">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="60e14-130">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="60e14-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





