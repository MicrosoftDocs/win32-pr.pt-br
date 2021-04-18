---
title: Network. lostPackets
description: A propriedade lostPackets recupera o número de pacotes perdidos.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Network. lostPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751781"
---
# <a name="networklostpackets"></a><span data-ttu-id="8d8e5-104">Network. lostPackets</span><span class="sxs-lookup"><span data-stu-id="8d8e5-104">Network.lostPackets</span></span>

<span data-ttu-id="8d8e5-105">A propriedade **lostPackets** recupera o número de pacotes perdidos.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-105">The **lostPackets** property retrieves the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8e5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d8e5-106">Syntax</span></span>

<span data-ttu-id="8d8e5-107">*Player*. *rede*. **lostPackets**</span><span class="sxs-lookup"><span data-stu-id="8d8e5-107">*player*.*network*.**lostPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="8d8e5-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="8d8e5-108">Possible Values</span></span>

<span data-ttu-id="8d8e5-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="8d8e5-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d8e5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d8e5-110">Remarks</span></span>

<span data-ttu-id="8d8e5-111">Essa propriedade só é válida para streaming de mídia e será igual a zero ao usar o protocolo HTTP, que é sem perdas.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-111">This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="8d8e5-112">Os pacotes podem ser perdidos por vários motivos, como o tipo e a qualidade da conexão de rede.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-112">Packets may be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="8d8e5-113">Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="8d8e5-114">Ele não será redefinido se a reprodução for pausada e reiniciada.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-114">It is not reset if playback is paused and restarted.</span></span> <span data-ttu-id="8d8e5-115">Essa propriedade retorna informações válidas somente durante o tempo de execução e somente se o *jogador*. A propriedade de **URL** está definida.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-115">This property returns valid information only during run time, and only if the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="8d8e5-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8d8e5-116">Examples</span></span>

<span data-ttu-id="8d8e5-117">O exemplo de JScript a seguir usa a *rede*. **lostPackets** para exibir o número total de pacotes perdidos durante a reprodução quando o usuário clica em um botão.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-117">The following JScript example uses *Network*.**lostPackets** to display the total number of packets lost during playback when the user clicks a button.</span></span> <span data-ttu-id="8d8e5-118">As informações são exibidas em uma DIV HTML criada com ID = "LP".</span><span class="sxs-lookup"><span data-stu-id="8d8e5-118">The information is displayed in an HTML DIV created with ID = "LP".</span></span> <span data-ttu-id="8d8e5-119">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="8d8e5-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a><span data-ttu-id="8d8e5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d8e5-120">Requirements</span></span>



| <span data-ttu-id="8d8e5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d8e5-121">Requirement</span></span> | <span data-ttu-id="8d8e5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8d8e5-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8e5-123">Versão</span><span class="sxs-lookup"><span data-stu-id="8d8e5-123">Version</span></span><br/> | <span data-ttu-id="8d8e5-124">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="8d8e5-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8d8e5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8d8e5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="8d8e5-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d8e5-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d8e5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d8e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8e5-128">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="8d8e5-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="8d8e5-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="8d8e5-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





