---
title: Network. receptionQuality
description: A propriedade receptionQuality recupera a porcentagem de pacotes recebidos nos últimos 30 segundos.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Network. receptionQuality Windows Media Player
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813283"
---
# <a name="networkreceptionquality"></a><span data-ttu-id="23ba6-104">Network. receptionQuality</span><span class="sxs-lookup"><span data-stu-id="23ba6-104">Network.receptionQuality</span></span>

<span data-ttu-id="23ba6-105">A propriedade **receptionQuality** recupera a porcentagem de pacotes recebidos nos últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="23ba6-105">The **receptionQuality** property retrieves the percentage of packets received in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="23ba6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="23ba6-106">Syntax</span></span>

<span data-ttu-id="23ba6-107">*Player*. *rede*. **receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="23ba6-107">*player*.*network*.**receptionQuality**</span></span>

## <a name="possible-values"></a><span data-ttu-id="23ba6-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="23ba6-108">Possible Values</span></span>

<span data-ttu-id="23ba6-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="23ba6-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="23ba6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="23ba6-110">Remarks</span></span>

<span data-ttu-id="23ba6-111">O número de pacotes recebidos, perdidos e recuperados durante o streaming é monitorado uma vez a cada segundo.</span><span class="sxs-lookup"><span data-stu-id="23ba6-111">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="23ba6-112">**receptionQuality** é a porcentagem de pacotes não perdidos durante os últimos 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="23ba6-112">**receptionQuality** is the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="23ba6-113">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero.</span><span class="sxs-lookup"><span data-stu-id="23ba6-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="23ba6-114">Ele não será redefinido se a reprodução for pausada.</span><span class="sxs-lookup"><span data-stu-id="23ba6-114">It is not reset if playback is paused.</span></span>

<span data-ttu-id="23ba6-115">Essa propriedade retorna informações válidas somente durante o tempo de execução e somente se o *jogador*. A propriedade **URL** também é definida.</span><span class="sxs-lookup"><span data-stu-id="23ba6-115">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span>

## <a name="examples"></a><span data-ttu-id="23ba6-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23ba6-116">Examples</span></span>

<span data-ttu-id="23ba6-117">O exemplo de JScript a seguir usa a *rede*. **receptionQuality** para exibir a porcentagem de pacotes recebidos.</span><span class="sxs-lookup"><span data-stu-id="23ba6-117">The following JScript example uses *Network*.**receptionQuality** to display the percentage of packets received.</span></span> <span data-ttu-id="23ba6-118">As informações são exibidas em um DIV HTML criado com ID = "RQ".</span><span class="sxs-lookup"><span data-stu-id="23ba6-118">The information is displayed in an HTML DIV created with ID = "RQ".</span></span> <span data-ttu-id="23ba6-119">O exemplo usa um temporizador com um intervalo de 30 segundos para atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="23ba6-119">The example uses a timer with a 30-second interval to update the display.</span></span> <span data-ttu-id="23ba6-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="23ba6-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="23ba6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23ba6-121">Requirements</span></span>



| <span data-ttu-id="23ba6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="23ba6-122">Requirement</span></span> | <span data-ttu-id="23ba6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="23ba6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23ba6-124">Versão</span><span class="sxs-lookup"><span data-stu-id="23ba6-124">Version</span></span><br/> | <span data-ttu-id="23ba6-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="23ba6-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="23ba6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="23ba6-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="23ba6-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23ba6-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ba6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="23ba6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ba6-129">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="23ba6-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="23ba6-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="23ba6-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





