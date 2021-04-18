---
title: Network. downloadProgress
description: A propriedade downloadProgress recupera a porcentagem de download concluído.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- Network. downloadProgress Windows Media Player
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781258"
---
# <a name="networkdownloadprogress"></a><span data-ttu-id="942bb-104">Network. downloadProgress</span><span class="sxs-lookup"><span data-stu-id="942bb-104">Network.downloadProgress</span></span>

<span data-ttu-id="942bb-105">A propriedade **downloadProgress** recupera a porcentagem de download concluído.</span><span class="sxs-lookup"><span data-stu-id="942bb-105">The **downloadProgress** property retrieves the percentage of download completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="942bb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="942bb-106">Syntax</span></span>

<span data-ttu-id="942bb-107">*Player*. *rede*. **downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="942bb-107">*player*.*network*.**downloadProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="942bb-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="942bb-108">Possible Values</span></span>

<span data-ttu-id="942bb-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="942bb-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="942bb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="942bb-110">Remarks</span></span>

<span data-ttu-id="942bb-111">Quando o controle do Windows Media Player está conectado a um arquivo de mídia que pode ser reproduzido e baixado ao mesmo tempo, a propriedade **downloadProgress** retorna a porcentagem do arquivo total que foi baixado.</span><span class="sxs-lookup"><span data-stu-id="942bb-111">When the Windows Media Player control is connected to a media file that can be played and downloaded at the same time, the **downloadProgress** property returns the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="942bb-112">Atualmente, esse recurso tem suporte apenas em servidores Web.</span><span class="sxs-lookup"><span data-stu-id="942bb-112">This feature is currently supported only on web servers.</span></span> <span data-ttu-id="942bb-113">Os seguintes formatos de arquivo podem ser baixados e reproduzidos simultaneamente:</span><span class="sxs-lookup"><span data-stu-id="942bb-113">The following file formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="942bb-114">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="942bb-114">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="942bb-115">Áudio do Windows Media (WMA)</span><span class="sxs-lookup"><span data-stu-id="942bb-115">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="942bb-116">Vídeo do Windows Media (WMV)</span><span class="sxs-lookup"><span data-stu-id="942bb-116">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="942bb-117">MP3</span><span class="sxs-lookup"><span data-stu-id="942bb-117">MP3</span></span>
-   <span data-ttu-id="942bb-118">FUNCIONALIDADES</span><span class="sxs-lookup"><span data-stu-id="942bb-118">MPEG</span></span>
-   <span data-ttu-id="942bb-119">WAV</span><span class="sxs-lookup"><span data-stu-id="942bb-119">WAV</span></span>
-   <span data-ttu-id="942bb-120">Alguns arquivos AVI</span><span class="sxs-lookup"><span data-stu-id="942bb-120">Some AVI files</span></span>

<span data-ttu-id="942bb-121">Use o *Player*. Evento de **buffer** para determinar quando o download começa e termina.</span><span class="sxs-lookup"><span data-stu-id="942bb-121">Use the *Player*.**Buffering** event to determine when the downloading begins and ends.</span></span>

## <a name="examples"></a><span data-ttu-id="942bb-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="942bb-122">Examples</span></span>

<span data-ttu-id="942bb-123">O exemplo de JScript a seguir usa a *rede*. **downloadProgress** para exibir a porcentagem de download concluído.</span><span class="sxs-lookup"><span data-stu-id="942bb-123">The following JScript example uses *Network*.**downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="942bb-124">As informações são exibidas em um DIV HTML criado com ID = "DP".</span><span class="sxs-lookup"><span data-stu-id="942bb-124">The information is displayed in an HTML DIV created with ID = "DP".</span></span> <span data-ttu-id="942bb-125">O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="942bb-125">The example uses a timer with a 1 second interval to update the display.</span></span> <span data-ttu-id="942bb-126">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="942bb-126">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="942bb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="942bb-127">Requirements</span></span>



| <span data-ttu-id="942bb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="942bb-128">Requirement</span></span> | <span data-ttu-id="942bb-129">Valor</span><span class="sxs-lookup"><span data-stu-id="942bb-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="942bb-130">Versão</span><span class="sxs-lookup"><span data-stu-id="942bb-130">Version</span></span><br/> | <span data-ttu-id="942bb-131">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="942bb-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="942bb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="942bb-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="942bb-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="942bb-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="942bb-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="942bb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="942bb-135">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="942bb-135">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="942bb-136">**Evento Player. buffering**</span><span class="sxs-lookup"><span data-stu-id="942bb-136">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> </dl>

 

 





