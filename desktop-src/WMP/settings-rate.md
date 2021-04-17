---
title: Settings. Rate
description: A propriedade Rate especifica ou recupera a taxa de reprodução atual da mídia de vídeo.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Settings. Rate Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748108"
---
# <a name="settingsrate"></a><span data-ttu-id="91026-104">Settings. Rate</span><span class="sxs-lookup"><span data-stu-id="91026-104">Settings.rate</span></span>

<span data-ttu-id="91026-105">A propriedade **Rate** especifica ou recupera a taxa de reprodução atual da mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="91026-105">The **rate** property specifies or retrieves the current playback rate of video media.</span></span>

## <a name="syntax"></a><span data-ttu-id="91026-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="91026-106">Syntax</span></span>

<span data-ttu-id="91026-107">Player. Settings. Rate</span><span class="sxs-lookup"><span data-stu-id="91026-107">player.settings.rate</span></span>

## <a name="possible-values"></a><span data-ttu-id="91026-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="91026-108">Possible Values</span></span>

<span data-ttu-id="91026-109">Essa propriedade é um **número** de leitura/gravação (**duplo**) com um valor padrão de 1,0.</span><span class="sxs-lookup"><span data-stu-id="91026-109">This property is a read/write **Number** (**double**) with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="91026-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="91026-110">Remarks</span></span>

<span data-ttu-id="91026-111">Essa propriedade atua como um valor de multiplicador que permite que você reproduza um clipe em uma taxa mais rápida ou mais lenta.</span><span class="sxs-lookup"><span data-stu-id="91026-111">This property acts as a multiplier value that allows you to play a clip at a faster or slower rate.</span></span> <span data-ttu-id="91026-112">O valor padrão de 1,0 indica a velocidade de criação.</span><span class="sxs-lookup"><span data-stu-id="91026-112">The default value of 1.0 indicates the authored speed.</span></span> <span data-ttu-id="91026-113">Observe que uma faixa de áudio torna-se difícil de entender em taxas menores que 0,5 ou superiores a 1,5.</span><span class="sxs-lookup"><span data-stu-id="91026-113">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="91026-114">Uma taxa de reprodução de 2 equivale a duas vezes a velocidade de reprodução normal.</span><span class="sxs-lookup"><span data-stu-id="91026-114">A playback rate of 2 equates to twice the normal playback speed.</span></span>

<span data-ttu-id="91026-115">O Windows Media Player tentará usar o mais eficiente de quatro modos de reprodução diferentes.</span><span class="sxs-lookup"><span data-stu-id="91026-115">Windows Media Player will attempt to use the most effective of four different playback modes.</span></span> <span data-ttu-id="91026-116">Esses modos são reprodução de vídeo suave com densidade de áudio mantida, reprodução de vídeo suave com densidade de áudio não mantida, reprodução de vídeo suave sem áudio e reprodução de vídeo com quadro-chave sem áudio.</span><span class="sxs-lookup"><span data-stu-id="91026-116">These modes are smooth video playback with audio pitch maintained, smooth video playback with audio pitch not maintained, smooth video playback with no audio, and keyframe video playback with no audio.</span></span> <span data-ttu-id="91026-117">O modo escolhido pelo player depende de vários fatores, incluindo tipo de arquivo e local, sistema operacional, rede e servidor.</span><span class="sxs-lookup"><span data-stu-id="91026-117">The mode chosen by the Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="91026-118">Outras considerações também se aplicam, dependendo do tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="91026-118">Other considerations apply as well, depending on media type:</span></span>

-   <span data-ttu-id="91026-119">Arquivos WMV (Windows Media Format) e ASF: os valores ideais para essa propriedade são de 1 a 10 ou de 1 a 10 para reprodução reversa.</span><span class="sxs-lookup"><span data-stu-id="91026-119">Windows Media Format (WMV) and ASF files: Optimal values for this property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="91026-120">Os valores de 0,5 a 1,0 ou de-0,5 a-1,0 também podem funcionar bem em casos em que a densidade de áudio pode ser mantida, por exemplo, ao reproduzir arquivos localizados no computador local.</span><span class="sxs-lookup"><span data-stu-id="91026-120">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, for example, when playing files located on the local computer.</span></span> <span data-ttu-id="91026-121">Valores com uma magnitude absoluta maior que 10 são permitidos, mas não são muito significativos.</span><span class="sxs-lookup"><span data-stu-id="91026-121">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="91026-122">Outros tipos de mídia de vídeo: essa propriedade pode variar de 0 a 9.</span><span class="sxs-lookup"><span data-stu-id="91026-122">Other Video Media Types: This property can range from 0 to 9.</span></span> <span data-ttu-id="91026-123">Valores negativos não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="91026-123">Negative values are not allowed.</span></span> <span data-ttu-id="91026-124">Valores menores que 1 representam movimento lento.</span><span class="sxs-lookup"><span data-stu-id="91026-124">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="91026-125">Os valores acima de 9 são permitidos, mas não são muito significativos.</span><span class="sxs-lookup"><span data-stu-id="91026-125">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="91026-126">Os *controles*. o método **Fastforward** altera o valor de **Rate** para 5,0, enquanto os *controles*. o método **fastReverse** altera a **taxa** para 5,0.</span><span class="sxs-lookup"><span data-stu-id="91026-126">The *Controls*.**fastForward** method changes the value of **rate** to 5.0, while the *Controls*.**fastReverse** method changes **rate** to  5.0.</span></span>

<span data-ttu-id="91026-127">A taxa de reprodução de alguns tipos de mídia não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="91026-127">The playback rate of some media types cannot be altered.</span></span> <span data-ttu-id="91026-128">Use as *configurações*. método **IsAvailable** para determinar se essa propriedade pode ser especificada para um item de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="91026-128">Use the *Settings*.**isAvailable** method to determine whether this property can be specified for a particular media item.</span></span>

<span data-ttu-id="91026-129">**Windows Media Player 10 Mobile**: essa propriedade só aceita ou retorna valores de-5,0, 1,0 ou 5,0.</span><span class="sxs-lookup"><span data-stu-id="91026-129">**Windows Media Player 10 Mobile**: This property only accepts or returns values of -5.0, 1.0, or 5.0.</span></span>

## <a name="examples"></a><span data-ttu-id="91026-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91026-130">Examples</span></span>

<span data-ttu-id="91026-131">O exemplo a seguir cria um elemento HTML SELECT que permite ao usuário alterar a velocidade de reprodução da mídia atual.</span><span class="sxs-lookup"><span data-stu-id="91026-131">The following example creates an HTML SELECT element that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="91026-132">As opções SELECT oferecem velocidade normal, meia velocidade e taxas de reprodução de velocidade dupla.</span><span class="sxs-lookup"><span data-stu-id="91026-132">The SELECT options offer normal speed, half -speed and double-speed playback rates.</span></span> <span data-ttu-id="91026-133">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="91026-133">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="91026-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91026-134">Requirements</span></span>



| <span data-ttu-id="91026-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="91026-135">Requirement</span></span> | <span data-ttu-id="91026-136">Valor</span><span class="sxs-lookup"><span data-stu-id="91026-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="91026-137">Versão</span><span class="sxs-lookup"><span data-stu-id="91026-137">Version</span></span><br/> | <span data-ttu-id="91026-138">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="91026-138">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="91026-139">DLL</span><span class="sxs-lookup"><span data-stu-id="91026-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="91026-140"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91026-140"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91026-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="91026-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91026-142">**Controls. fastForward**</span><span class="sxs-lookup"><span data-stu-id="91026-142">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="91026-143">**Controls. fastReverse**</span><span class="sxs-lookup"><span data-stu-id="91026-143">**Controls.fastReverse**</span></span>](controls-fastreverse.md)
</dt> <dt>

[<span data-ttu-id="91026-144">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="91026-144">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="91026-145">**Settings. IsAvailable**</span><span class="sxs-lookup"><span data-stu-id="91026-145">**Settings.isAvailable**</span></span>](settings-isavailable.md)
</dt> </dl>

 

 





