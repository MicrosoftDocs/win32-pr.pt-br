---
title: Propriedade IWMPClosedCaption SAMIFileName
description: A propriedade SAMIFileName Obtém ou define o nome de um arquivo que contém as informações necessárias para Legendagem oculta.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Propriedade SAMIFileName Windows Media Player
- Propriedade SAMIFileName Windows Media Player, interface IWMPClosedCaption
- Interface IWMPClosedCaption Windows Media Player, Propriedade SAMIFileName
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251f2bbf0c8839ab9a0005c69e1869c47af16ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752553"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a><span data-ttu-id="0d5ab-106">Propriedade IWMPClosedCaption:: SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="0d5ab-106">IWMPClosedCaption::SAMIFileName property</span></span>

<span data-ttu-id="0d5ab-107">A propriedade **SAMIFileName** Obtém ou define o nome de um arquivo que contém as informações necessárias para Legendagem oculta.</span><span class="sxs-lookup"><span data-stu-id="0d5ab-107">The **SAMIFileName** property gets or sets the name of a file containing the information needed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5ab-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d5ab-108">Syntax</span></span>


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a><span data-ttu-id="0d5ab-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0d5ab-109">Property value</span></span>

<span data-ttu-id="0d5ab-110">O **System. String** que é o nome do arquivo de intercâmbio de mídia acessível (Sami) sincronizado.</span><span class="sxs-lookup"><span data-stu-id="0d5ab-110">The **System.String** that is the name of the Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d5ab-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d5ab-111">Remarks</span></span>

<span data-ttu-id="0d5ab-112">O arquivo SAMI deve usar uma extensão de nome de arquivo. SMI ou. Sami.</span><span class="sxs-lookup"><span data-stu-id="0d5ab-112">The SAMI file must use an .smi or .sami file name extension.</span></span>

<span data-ttu-id="0d5ab-113">Se você não definir um valor usando **SAMIFileName**, essa propriedade obterá uma **cadeia de caracteres** que contém o nome de arquivo padrão ou a URL associada ao item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="0d5ab-113">If you do not set a value using **SAMIFileName**, this property gets a **string** containing the default file name or URL associated with the current media item.</span></span> <span data-ttu-id="0d5ab-114">Essa associação pode ocorrer quando um arquivo SAMI é especificado usando o parâmetro de URL *Sami* , ou automaticamente quando o arquivo Sami tem o mesmo nome que o arquivo de mídia digital (exceto para a extensão de nome de arquivo).</span><span class="sxs-lookup"><span data-stu-id="0d5ab-114">This association can occur when a SAMI file is specified by using the *sami* URL parameter, or automatically when the SAMI file has the same name as the digital media file (except for the file name extension).</span></span> <span data-ttu-id="0d5ab-115">Se não houver nenhum arquivo SAMI padrão associado à mídia atual, essa propriedade obterá uma cadeia de caracteres de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="0d5ab-115">If there is no default SAMI file associated with the current media, this property gets a zero-length string ("").</span></span>

<span data-ttu-id="0d5ab-116">Depois de definir um valor usando **SAMIFileName**, esse valor persiste até que você defina um novo valor (ou até que um novo item de mídia seja aberto usando o parâmetro de URL Sami).</span><span class="sxs-lookup"><span data-stu-id="0d5ab-116">Once you set a value using **SAMIFileName**, that value persists until you set a new value (or until a new media item is opened using the sami URL parameter).</span></span> <span data-ttu-id="0d5ab-117">Portanto, você deve definir um novo valor para essa propriedade antes de reproduzir cada novo item de mídia.</span><span class="sxs-lookup"><span data-stu-id="0d5ab-117">Therefore, you must set a new value for this property before you play each new media item.</span></span> <span data-ttu-id="0d5ab-118">Dessa forma, o novo valor de **SAMIFileName** entrará em vigor quando o próximo item de mídia for aberto (ou quando **AxWindowsMediaPlayer. Close** for chamado).</span><span class="sxs-lookup"><span data-stu-id="0d5ab-118">That way, the new value for **SAMIFileName** will take effect when the next media item is opened (or when **AxWindowsMediaPlayer.close** is called).</span></span> <span data-ttu-id="0d5ab-119">A especificação de um novo valor para **SAMIFileName** não tem nenhum efeito para a mídia atual.</span><span class="sxs-lookup"><span data-stu-id="0d5ab-119">Specifying a new value for **SAMIFileName** has no effect for the current media.</span></span>

<span data-ttu-id="0d5ab-120">Para fazer com que o Windows Media Player use o arquivo SAMI padrão associado a um item de mídia específico, defina **SAMIFileName** como uma cadeia de caracteres de comprimento zero ("") antes de reproduzir o próximo item de mídia.</span><span class="sxs-lookup"><span data-stu-id="0d5ab-120">To cause Windows Media Player to use the default SAMI file associated with a particular media item, set **SAMIFileName** to a zero-length string ("") before you play the next media item.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5ab-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d5ab-121">Requirements</span></span>



| <span data-ttu-id="0d5ab-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d5ab-122">Requirement</span></span> | <span data-ttu-id="0d5ab-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0d5ab-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5ab-124">Versão</span><span class="sxs-lookup"><span data-stu-id="0d5ab-124">Version</span></span><br/>   | <span data-ttu-id="0d5ab-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="0d5ab-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0d5ab-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d5ab-126">Namespace</span></span><br/> | <span data-ttu-id="0d5ab-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0d5ab-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0d5ab-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="0d5ab-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0d5ab-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5ab-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d5ab-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d5ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5ab-131">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="0d5ab-131">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="0d5ab-132">**AxWindowsMediaPlayer. Close**</span><span class="sxs-lookup"><span data-stu-id="0d5ab-132">**AxWindowsMediaPlayer.close**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="0d5ab-133">**Interface IWMPClosedCaption (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0d5ab-133">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d5ab-134">**Interface IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="0d5ab-134">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





