---
title: Propriedade baseURL IWMPSettings
description: A propriedade baseURL Obtém ou define a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos no conteúdo de mídia digital.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- Propriedade baseURL Windows Media Player
- Propriedade baseURL Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791342"
---
# <a name="iwmpsettingsbaseurl-property"></a><span data-ttu-id="605dc-106">Propriedade IWMPSettings:: baseURL</span><span class="sxs-lookup"><span data-stu-id="605dc-106">IWMPSettings::baseURL property</span></span>

<span data-ttu-id="605dc-107">A propriedade **baseURL** Obtém ou define a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos no conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="605dc-107">The **baseURL** property gets or sets the base URL used for relative path resolution with URL script commands that are embedded in digital media content.</span></span>

## <a name="syntax"></a><span data-ttu-id="605dc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="605dc-108">Syntax</span></span>


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="605dc-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="605dc-109">Property value</span></span>

<span data-ttu-id="605dc-110">Um **System. String** que é a URL base.</span><span class="sxs-lookup"><span data-stu-id="605dc-110">A **System.String** that is the base URL.</span></span>

## <a name="remarks"></a><span data-ttu-id="605dc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="605dc-111">Remarks</span></span>

<span data-ttu-id="605dc-112">Essa propriedade especifica a URL HTTP base que é passada como o parâmetro de comando pelo evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .</span><span class="sxs-lookup"><span data-stu-id="605dc-112">This property specifies the base HTTP URL that is passed as the command parameter by the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span> <span data-ttu-id="605dc-113">A URL base é concatenada com a URL relativa da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="605dc-113">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="605dc-114">Uma barra (/) à direita é adicionada ao valor recuperado pela propriedade **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="605dc-114">A trailing forward slash (/) is added to the value retrieved by the **baseURL** property.</span></span>
2.  <span data-ttu-id="605dc-115">Um ponto à esquerda, uma barra invertida ou um caractere de barra invertida (., \\ e/) é excluído da URL relativa.</span><span class="sxs-lookup"><span data-stu-id="605dc-115">A leading period, backward slash, or forward slash character (., \\, and /) is deleted from the relative URL.</span></span>
3.  <span data-ttu-id="605dc-116">A URL relativa é adicionada ao final da URL base.</span><span class="sxs-lookup"><span data-stu-id="605dc-116">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="605dc-117">Todos os caracteres de barra na URL totalmente qualificada resultante são apontados na mesma direção (convertida para barras para frente ou para trás) com base na direção do caractere de primeira barra encontrado na nova URL.</span><span class="sxs-lookup"><span data-stu-id="605dc-117">All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="605dc-118">**Observação**</span><span class="sxs-lookup"><span data-stu-id="605dc-118">**Note**</span></span>

<span data-ttu-id="605dc-119">O controle do Windows Media Player não oferece suporte ao uso de dois pontos (..) na URL relativa para indicar o pai do local atual.</span><span class="sxs-lookup"><span data-stu-id="605dc-119">The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

## <a name="requirements"></a><span data-ttu-id="605dc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="605dc-120">Requirements</span></span>



| <span data-ttu-id="605dc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="605dc-121">Requirement</span></span> | <span data-ttu-id="605dc-122">Valor</span><span class="sxs-lookup"><span data-stu-id="605dc-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="605dc-123">Versão</span><span class="sxs-lookup"><span data-stu-id="605dc-123">Version</span></span><br/>   | <span data-ttu-id="605dc-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="605dc-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="605dc-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="605dc-125">Namespace</span></span><br/> | <span data-ttu-id="605dc-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="605dc-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="605dc-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="605dc-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="605dc-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="605dc-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="605dc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="605dc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="605dc-130">**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="605dc-130">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="605dc-131">**Interface IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="605dc-131">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





