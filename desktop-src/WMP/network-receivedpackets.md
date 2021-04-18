---
title: Network. receivedPackets
description: A propriedade receivedPackets recupera o número de pacotes recebidos.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- Network. receivedPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788887"
---
# <a name="networkreceivedpackets"></a><span data-ttu-id="c0191-104">Network. receivedPackets</span><span class="sxs-lookup"><span data-stu-id="c0191-104">Network.receivedPackets</span></span>

<span data-ttu-id="c0191-105">A propriedade **receivedPackets** recupera o número de pacotes recebidos.</span><span class="sxs-lookup"><span data-stu-id="c0191-105">The **receivedPackets** property retrieves the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0191-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0191-106">Syntax</span></span>

<span data-ttu-id="c0191-107">*Player*. *rede*. **receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="c0191-107">*player*.*network*.**receivedPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c0191-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="c0191-108">Possible Values</span></span>

<span data-ttu-id="c0191-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="c0191-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0191-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0191-110">Remarks</span></span>

<span data-ttu-id="c0191-111">Toda vez que a reprodução de clipe é interrompida e reiniciada, essa propriedade é definida como zero.</span><span class="sxs-lookup"><span data-stu-id="c0191-111">Each time clip playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="c0191-112">Ela não será redefinida se a reprodução do arquivo for pausada.</span><span class="sxs-lookup"><span data-stu-id="c0191-112">It is not reset if file playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="c0191-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0191-113">Examples</span></span>

<span data-ttu-id="c0191-114">O exemplo de JScript a seguir usa a *rede*. **receivedPackets** para exibir o número de pacotes recebidos.</span><span class="sxs-lookup"><span data-stu-id="c0191-114">The following JScript example uses *Network*.**receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="c0191-115">As informações são exibidas em um DIV HTML criado com ID = "RP".</span><span class="sxs-lookup"><span data-stu-id="c0191-115">The information is displayed in an HTML DIV created with ID = "RP".</span></span> <span data-ttu-id="c0191-116">O exemplo usa um temporizador com um intervalo de 1 segundo para atualizar a exibição.</span><span class="sxs-lookup"><span data-stu-id="c0191-116">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="c0191-117">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c0191-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a><span data-ttu-id="c0191-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0191-118">Requirements</span></span>



| <span data-ttu-id="c0191-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0191-119">Requirement</span></span> | <span data-ttu-id="c0191-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c0191-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0191-121">Versão</span><span class="sxs-lookup"><span data-stu-id="c0191-121">Version</span></span><br/> | <span data-ttu-id="c0191-122">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c0191-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c0191-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c0191-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0191-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0191-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0191-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0191-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0191-126">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="c0191-126">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





