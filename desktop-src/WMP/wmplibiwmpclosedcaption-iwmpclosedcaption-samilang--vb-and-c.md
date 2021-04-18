---
title: Propriedade IWMPClosedCaption SAMILang
description: A propriedade SAMILang Obtém ou define o idioma exibido para Legendagem oculta.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Propriedade SAMILang Windows Media Player
- Propriedade SAMILang Windows Media Player, interface IWMPClosedCaption
- Interface IWMPClosedCaption Windows Media Player, Propriedade SAMILang
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810821"
---
# <a name="iwmpclosedcaptionsamilang-property"></a><span data-ttu-id="7a570-106">Propriedade IWMPClosedCaption:: SAMILang</span><span class="sxs-lookup"><span data-stu-id="7a570-106">IWMPClosedCaption::SAMILang property</span></span>

<span data-ttu-id="7a570-107">A propriedade **SAMILang** Obtém ou define o idioma exibido para Legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="7a570-107">The **SAMILang** property gets or sets the language displayed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a570-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a570-108">Syntax</span></span>


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a><span data-ttu-id="7a570-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7a570-109">Property value</span></span>

<span data-ttu-id="7a570-110">O **System. String** que é o nome especificado no identificador de idioma de um arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="7a570-110">The **System.String** that is the name specified in the language identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a570-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a570-111">Remarks</span></span>

<span data-ttu-id="7a570-112">Um arquivo SAMI pode conter texto para uma ou várias linguagens.</span><span class="sxs-lookup"><span data-stu-id="7a570-112">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="7a570-113">Os idiomas disponíveis para legendas codificadas são definidos entre as marcas <STYLE> e </STYLE> no arquivo Sami.</span><span class="sxs-lookup"><span data-stu-id="7a570-113">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="7a570-114">Um identificador de idioma é especificado com uma cadeia de caracteres alfanumérica exclusiva que é precedida por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="7a570-114">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="7a570-115">O nome especificado para um idioma pode ser qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7a570-115">The name specified for a language can be any string.</span></span> <span data-ttu-id="7a570-116">Por exemplo, o seguinte pode ser usado para definir o inglês dos EUA:</span><span class="sxs-lookup"><span data-stu-id="7a570-116">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



<span data-ttu-id="7a570-117">Se nenhum idioma SAMI for especificado, o primeiro idioma definido no arquivo SAMI será usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="7a570-117">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="7a570-118">A cadeia de caracteres que você define usando **SAMILang** deve corresponder ao atributo **Name** no especificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="7a570-118">The string you set using **SAMILang** must match the **Name** attribute in the language specifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a570-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a570-119">Requirements</span></span>



| <span data-ttu-id="7a570-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a570-120">Requirement</span></span> | <span data-ttu-id="7a570-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7a570-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a570-122">Versão</span><span class="sxs-lookup"><span data-stu-id="7a570-122">Version</span></span><br/>   | <span data-ttu-id="7a570-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7a570-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7a570-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a570-124">Namespace</span></span><br/> | <span data-ttu-id="7a570-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7a570-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7a570-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="7a570-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7a570-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7a570-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a570-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a570-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a570-129">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="7a570-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="7a570-130">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7a570-130">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7a570-131">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="7a570-131">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





