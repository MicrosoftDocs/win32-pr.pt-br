---
title: Rede. largura de banda
description: A propriedade bandWidth recupera a largura de banda atual do clipe.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Rede. largura de banda Windows Media Player
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772937"
---
# <a name="networkbandwidth"></a><span data-ttu-id="7c084-104">Rede. largura de banda</span><span class="sxs-lookup"><span data-stu-id="7c084-104">Network.bandWidth</span></span>

<span data-ttu-id="7c084-105">A propriedade **Bandwidth** recupera a largura de banda atual do clipe.</span><span class="sxs-lookup"><span data-stu-id="7c084-105">The **bandWidth** property retrieves the current bandwidth of the clip.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c084-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c084-106">Syntax</span></span>

<span data-ttu-id="7c084-107">*Player*. *rede*. **largura de banda**</span><span class="sxs-lookup"><span data-stu-id="7c084-107">*player*.*network*.**bandWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="7c084-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="7c084-108">Possible Values</span></span>

<span data-ttu-id="7c084-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="7c084-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c084-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c084-110">Remarks</span></span>

<span data-ttu-id="7c084-111">Essa propriedade retornará zero se o *Player*. A propriedade da **URL** não está definida.</span><span class="sxs-lookup"><span data-stu-id="7c084-111">This property returns zero if the *Player*.**URL** property is not set.</span></span> <span data-ttu-id="7c084-112">Esta propriedade só é válida para mídia de streaming.</span><span class="sxs-lookup"><span data-stu-id="7c084-112">This property is only valid for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="7c084-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c084-113">Examples</span></span>

<span data-ttu-id="7c084-114">O exemplo do Microsoft JScript a seguir usa a *rede*. **largura de banda** para exibir a largura de banda de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="7c084-114">The following Microsoft JScript example uses *Network*.**bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="7c084-115">As informações são exibidas em uma DIV HTML criada com ID = "BW".</span><span class="sxs-lookup"><span data-stu-id="7c084-115">The information is displayed in an HTML DIV created with ID = "BW".</span></span> <span data-ttu-id="7c084-116">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7c084-116">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="7c084-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c084-117">Requirements</span></span>



| <span data-ttu-id="7c084-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c084-118">Requirement</span></span> | <span data-ttu-id="7c084-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7c084-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c084-120">Versão</span><span class="sxs-lookup"><span data-stu-id="7c084-120">Version</span></span><br/> | <span data-ttu-id="7c084-121">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7c084-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7c084-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7c084-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c084-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c084-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c084-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c084-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c084-125">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="7c084-125">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="7c084-126">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="7c084-126">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





