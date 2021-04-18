---
title: Network. taxa de quadros
description: A propriedade de taxa de quadros recupera a taxa de quadros de vídeo atual em quadros por centenas de segundos. Por exemplo, um valor de 2998 indica 29,98 quadros por segundo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Rede. taxa de quadros Windows Media Player
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781646"
---
# <a name="networkframerate"></a><span data-ttu-id="46919-105">Network. taxa de quadros</span><span class="sxs-lookup"><span data-stu-id="46919-105">Network.frameRate</span></span>

<span data-ttu-id="46919-106">A propriedade de **taxa** de quadros recupera a taxa de quadros de vídeo atual em quadros por centenas de segundos.</span><span class="sxs-lookup"><span data-stu-id="46919-106">The **frameRate** property retrieves the current video frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="46919-107">Por exemplo, um valor de 2998 indica 29,98 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="46919-107">For example, a value of 2998 indicates 29.98 frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="46919-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="46919-108">Syntax</span></span>

<span data-ttu-id="46919-109">*Player*. *rede*. **taxa de quadros**</span><span class="sxs-lookup"><span data-stu-id="46919-109">*player*.*network*.**frameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="46919-110">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="46919-110">Possible Values</span></span>

<span data-ttu-id="46919-111">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="46919-111">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="46919-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46919-112">Examples</span></span>

<span data-ttu-id="46919-113">O exemplo de JScript a seguir usa a *rede*. taxa **de quadros para exibir** a tarifa de quadros atual.</span><span class="sxs-lookup"><span data-stu-id="46919-113">The following JScript example uses *Network*.**frameRate** to display the current frame rate.</span></span> <span data-ttu-id="46919-114">As informações são exibidas em um DIV HTML criado com ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="46919-114">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="46919-115">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="46919-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="46919-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46919-116">Requirements</span></span>



| <span data-ttu-id="46919-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46919-117">Requirement</span></span> | <span data-ttu-id="46919-118">Valor</span><span class="sxs-lookup"><span data-stu-id="46919-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46919-119">Versão</span><span class="sxs-lookup"><span data-stu-id="46919-119">Version</span></span><br/> | <span data-ttu-id="46919-120">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="46919-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="46919-121">DLL</span><span class="sxs-lookup"><span data-stu-id="46919-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="46919-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46919-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46919-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="46919-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46919-124">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="46919-124">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="46919-125">**Network. encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="46919-125">**Network.encodedFrameRate**</span></span>](network-encodedframerate.md)
</dt> </dl>

 

 





