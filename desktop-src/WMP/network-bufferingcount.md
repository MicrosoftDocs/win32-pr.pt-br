---
title: Network. bufferingCount
description: A propriedade bufferingCount recupera o número de vezes que o buffer ocorreu durante a reprodução do clipe.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Network. bufferingCount Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796148"
---
# <a name="networkbufferingcount"></a><span data-ttu-id="bbb40-104">Network. bufferingCount</span><span class="sxs-lookup"><span data-stu-id="bbb40-104">Network.bufferingCount</span></span>

<span data-ttu-id="bbb40-105">A propriedade **bufferingCount** recupera o número de vezes que o buffer ocorreu durante a reprodução do clipe.</span><span class="sxs-lookup"><span data-stu-id="bbb40-105">The **bufferingCount** property retrieves the number of times buffering occurred during clip playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb40-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbb40-106">Syntax</span></span>

<span data-ttu-id="bbb40-107">*Player*. *rede*. **bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="bbb40-107">*player*.*network*.**bufferingCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="bbb40-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="bbb40-108">Possible Values</span></span>

<span data-ttu-id="bbb40-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="bbb40-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="bbb40-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbb40-110">Remarks</span></span>

<span data-ttu-id="bbb40-111">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero.</span><span class="sxs-lookup"><span data-stu-id="bbb40-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="bbb40-112">Ele não será redefinido se a reprodução for pausada.</span><span class="sxs-lookup"><span data-stu-id="bbb40-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="bbb40-113">O armazenamento em buffer só se aplica ao conteúdo de streaming.</span><span class="sxs-lookup"><span data-stu-id="bbb40-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="bbb40-114">Essa propriedade retorna informações válidas somente durante o tempo de execução quando o *Player*. A propriedade de **URL** está definida.</span><span class="sxs-lookup"><span data-stu-id="bbb40-114">This property returns valid information only during run time when the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="bbb40-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bbb40-115">Examples</span></span>

<span data-ttu-id="bbb40-116">O exemplo de JScript a seguir usa a *rede*. **bufferingCount** para exibir o número de vezes que o buffer ocorre durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="bbb40-116">The following JScript example uses *Network*.**bufferingCount** to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="bbb40-117">As informações são exibidas em uma DIV HTML criada com ID = "CB".</span><span class="sxs-lookup"><span data-stu-id="bbb40-117">The information is displayed in an HTML DIV created with ID = "CB".</span></span> <span data-ttu-id="bbb40-118">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="bbb40-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="bbb40-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbb40-119">Requirements</span></span>



| <span data-ttu-id="bbb40-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbb40-120">Requirement</span></span> | <span data-ttu-id="bbb40-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bbb40-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb40-122">Versão</span><span class="sxs-lookup"><span data-stu-id="bbb40-122">Version</span></span><br/> | <span data-ttu-id="bbb40-123">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bbb40-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bbb40-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bbb40-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="bbb40-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbb40-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbb40-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbb40-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb40-127">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="bbb40-127">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="bbb40-128">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="bbb40-128">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





