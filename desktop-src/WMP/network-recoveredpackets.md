---
title: Network. recoveredPackets
description: A propriedade recoveredPackets recupera o número de pacotes recuperados.
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- Network. recoveredPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788886"
---
# <a name="networkrecoveredpackets"></a><span data-ttu-id="68ee3-104">Network. recoveredPackets</span><span class="sxs-lookup"><span data-stu-id="68ee3-104">Network.recoveredPackets</span></span>

<span data-ttu-id="68ee3-105">A propriedade **recoveredPackets** recupera o número de pacotes recuperados.</span><span class="sxs-lookup"><span data-stu-id="68ee3-105">The **recoveredPackets** property retrieves the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ee3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ee3-106">Syntax</span></span>

<span data-ttu-id="68ee3-107">*Player*. *rede*. **recoveredPackets**</span><span class="sxs-lookup"><span data-stu-id="68ee3-107">*player*.*network*.**recoveredPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="68ee3-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="68ee3-108">Possible Values</span></span>

<span data-ttu-id="68ee3-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="68ee3-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="68ee3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="68ee3-110">Remarks</span></span>

<span data-ttu-id="68ee3-111">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero.</span><span class="sxs-lookup"><span data-stu-id="68ee3-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="68ee3-112">Ele não será redefinido se a reprodução for pausada.</span><span class="sxs-lookup"><span data-stu-id="68ee3-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="68ee3-113">Essa propriedade retorna informações válidas somente durante o tempo de execução e somente se o *jogador*. A propriedade **URL** também é definida.</span><span class="sxs-lookup"><span data-stu-id="68ee3-113">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span> <span data-ttu-id="68ee3-114">Ele será igual a zero ao usar o protocolo HTTP, que é sem perdas.</span><span class="sxs-lookup"><span data-stu-id="68ee3-114">It will equal zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="68ee3-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="68ee3-115">Examples</span></span>

<span data-ttu-id="68ee3-116">O exemplo de JScript a seguir usa a *rede*. **recoveredPackets** para exibir o número de pacotes recuperados.</span><span class="sxs-lookup"><span data-stu-id="68ee3-116">The following JScript example uses *Network*.**recoveredPackets** to display the number of recovered packets.</span></span> <span data-ttu-id="68ee3-117">As informações são exibidas em uma DIV HTML criada com ID = "PR".</span><span class="sxs-lookup"><span data-stu-id="68ee3-117">The information is displayed in an HTML DIV created with ID = "PR".</span></span> <span data-ttu-id="68ee3-118">O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="68ee3-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="68ee3-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="68ee3-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="68ee3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68ee3-120">Requirements</span></span>



| <span data-ttu-id="68ee3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="68ee3-121">Requirement</span></span> | <span data-ttu-id="68ee3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="68ee3-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68ee3-123">Versão</span><span class="sxs-lookup"><span data-stu-id="68ee3-123">Version</span></span><br/> | <span data-ttu-id="68ee3-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="68ee3-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="68ee3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="68ee3-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="68ee3-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68ee3-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68ee3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="68ee3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ee3-128">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="68ee3-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="68ee3-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="68ee3-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





