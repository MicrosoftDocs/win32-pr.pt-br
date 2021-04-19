---
title: Network. taxa de bits
description: A propriedade taxa de bits recupera a taxa de bit atual que está sendo recebida.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Rede. taxa de bits Windows Media Player
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797612"
---
# <a name="networkbitrate"></a><span data-ttu-id="3d4dd-104">Network. taxa de bits</span><span class="sxs-lookup"><span data-stu-id="3d4dd-104">Network.bitRate</span></span>

<span data-ttu-id="3d4dd-105">A **Propriedade taxa de bits recupera** a taxa de bit atual que está sendo recebida.</span><span class="sxs-lookup"><span data-stu-id="3d4dd-105">The **bitRate** property retrieves the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d4dd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d4dd-106">Syntax</span></span>

<span data-ttu-id="3d4dd-107">*Player*. *rede*. **taxa de bits**</span><span class="sxs-lookup"><span data-stu-id="3d4dd-107">*player*.*network*.**bitRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3d4dd-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="3d4dd-108">Possible Values</span></span>

<span data-ttu-id="3d4dd-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="3d4dd-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d4dd-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d4dd-110">Remarks</span></span>

<span data-ttu-id="3d4dd-111">Esse valor é uma combinação das taxas de bits dos fluxos de áudio e vídeo atuais.</span><span class="sxs-lookup"><span data-stu-id="3d4dd-111">This value is a combination of the bit rates of both the current video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="3d4dd-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3d4dd-112">Examples</span></span>

<span data-ttu-id="3d4dd-113">O exemplo de JScript a seguir usa a *rede*. taxa **de bits para exibir** a tarifa de bit de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="3d4dd-113">The following JScript example uses *Network*.**bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="3d4dd-114">As informações são exibidas em uma DIV HTML criada com ID = "BR".</span><span class="sxs-lookup"><span data-stu-id="3d4dd-114">The information is displayed in an HTML DIV created with ID = "BR".</span></span> <span data-ttu-id="3d4dd-115">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3d4dd-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="3d4dd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d4dd-116">Requirements</span></span>



| <span data-ttu-id="3d4dd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d4dd-117">Requirement</span></span> | <span data-ttu-id="3d4dd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3d4dd-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4dd-119">Versão</span><span class="sxs-lookup"><span data-stu-id="3d4dd-119">Version</span></span><br/> | <span data-ttu-id="3d4dd-120">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3d4dd-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3d4dd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3d4dd-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d4dd-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d4dd-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4dd-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d4dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4dd-124">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="3d4dd-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





