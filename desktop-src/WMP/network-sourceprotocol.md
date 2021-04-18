---
title: Network. sourceProtocol
description: A propriedade sourceProtocol recupera o protocolo de origem usado para receber dados.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Network. sourceProtocol Windows Media Player
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763469"
---
# <a name="networksourceprotocol"></a><span data-ttu-id="dfa43-104">Network. sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="dfa43-104">Network.sourceProtocol</span></span>

<span data-ttu-id="dfa43-105">A propriedade **sourceProtocol** recupera o protocolo de origem usado para receber dados.</span><span class="sxs-lookup"><span data-stu-id="dfa43-105">The **sourceProtocol** property retrieves the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa43-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfa43-106">Syntax</span></span>

<span data-ttu-id="dfa43-107">*Player*. *rede*. **sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="dfa43-107">*player*.*network*.**sourceProtocol**</span></span>

## <a name="possible-values"></a><span data-ttu-id="dfa43-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="dfa43-108">Possible Values</span></span>

<span data-ttu-id="dfa43-109">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="dfa43-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfa43-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfa43-110">Remarks</span></span>

<span data-ttu-id="dfa43-111">Essa propriedade é definida como "" (cadeia de caracteres vazia) ao reproduzir mídia de um CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="dfa43-111">This property is set to "" (empty string) when playing media from a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="dfa43-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dfa43-112">Examples</span></span>

<span data-ttu-id="dfa43-113">O exemplo de JScript a seguir usa a *rede*. **sourceProtocol** para exibir o protocolo de origem usado para receber dados.</span><span class="sxs-lookup"><span data-stu-id="dfa43-113">The following JScript example uses *Network*.**sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="dfa43-114">As informações são exibidas em um DIV HTML criado com ID = "SP".</span><span class="sxs-lookup"><span data-stu-id="dfa43-114">The information is displayed in an HTML DIV created with ID = "SP".</span></span> <span data-ttu-id="dfa43-115">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="dfa43-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="dfa43-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfa43-116">Requirements</span></span>



| <span data-ttu-id="dfa43-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa43-117">Requirement</span></span> | <span data-ttu-id="dfa43-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dfa43-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa43-119">Versão</span><span class="sxs-lookup"><span data-stu-id="dfa43-119">Version</span></span><br/> | <span data-ttu-id="dfa43-120">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="dfa43-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dfa43-121">DLL</span><span class="sxs-lookup"><span data-stu-id="dfa43-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="dfa43-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfa43-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa43-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfa43-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa43-124">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="dfa43-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





