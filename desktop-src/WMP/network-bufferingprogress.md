---
title: Network. bufferingProgress
description: A propriedade bufferingProgress recupera a porcentagem de buffer concluído.
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- Network. bufferingProgress Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764117"
---
# <a name="networkbufferingprogress"></a><span data-ttu-id="86baa-104">Network. bufferingProgress</span><span class="sxs-lookup"><span data-stu-id="86baa-104">Network.bufferingProgress</span></span>

<span data-ttu-id="86baa-105">A propriedade **bufferingProgress** recupera a porcentagem de buffer concluído.</span><span class="sxs-lookup"><span data-stu-id="86baa-105">The **bufferingProgress** property retrieves the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="86baa-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="86baa-106">Syntax</span></span>

<span data-ttu-id="86baa-107">*Player*. *rede*. **bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="86baa-107">*player*.*network*.**bufferingProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="86baa-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="86baa-108">Possible Values</span></span>

<span data-ttu-id="86baa-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="86baa-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="86baa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="86baa-110">Remarks</span></span>

<span data-ttu-id="86baa-111">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero.</span><span class="sxs-lookup"><span data-stu-id="86baa-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="86baa-112">Ele não será redefinido se a reprodução for pausada.</span><span class="sxs-lookup"><span data-stu-id="86baa-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="86baa-113">O armazenamento em buffer só se aplica ao conteúdo de streaming.</span><span class="sxs-lookup"><span data-stu-id="86baa-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="86baa-114">Essa propriedade retorna informações válidas somente durante o tempo de execução, quando o *Player*. A propriedade de **URL** está definida.</span><span class="sxs-lookup"><span data-stu-id="86baa-114">This property returns valid information only during run time, when the *Player*.**URL** property is set.</span></span>

<span data-ttu-id="86baa-115">Use o evento *Player*. \* \* \* \* buffer \* \* \* \* para determinar quando o buffer inicia ou pára.</span><span class="sxs-lookup"><span data-stu-id="86baa-115">Use the *Player*.\*\*\*\*Buffering\*\*\*\* event to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="86baa-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="86baa-116">Examples</span></span>

<span data-ttu-id="86baa-117">O exemplo de JScript a seguir usa a *rede*. **bufferingProgress** para exibir a porcentagem de buffer concluído.</span><span class="sxs-lookup"><span data-stu-id="86baa-117">The following JScript example uses *Network*.**bufferingProgress** to display the percentage of buffering completed.</span></span> <span data-ttu-id="86baa-118">As informações são exibidas em um DIV HTML criado com ID = "BP".</span><span class="sxs-lookup"><span data-stu-id="86baa-118">The information is displayed in an HTML DIV created with ID = "BP".</span></span> <span data-ttu-id="86baa-119">O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="86baa-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="86baa-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="86baa-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="86baa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86baa-121">Requirements</span></span>



| <span data-ttu-id="86baa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="86baa-122">Requirement</span></span> | <span data-ttu-id="86baa-123">Valor</span><span class="sxs-lookup"><span data-stu-id="86baa-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86baa-124">Versão</span><span class="sxs-lookup"><span data-stu-id="86baa-124">Version</span></span><br/> | <span data-ttu-id="86baa-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="86baa-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="86baa-126">DLL</span><span class="sxs-lookup"><span data-stu-id="86baa-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="86baa-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86baa-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86baa-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="86baa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86baa-129">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="86baa-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="86baa-130">**Evento Player. buffering**</span><span class="sxs-lookup"><span data-stu-id="86baa-130">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> <dt>

[<span data-ttu-id="86baa-131">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="86baa-131">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





