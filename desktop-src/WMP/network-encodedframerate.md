---
title: Network. encodedFrameRate
description: A propriedade encodedFrameRate recupera a taxa de quadros de vídeo especificada pelo autor do conteúdo em quadros por segundo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Network. encodedFrameRate Windows Media Player
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772935"
---
# <a name="networkencodedframerate"></a><span data-ttu-id="08d35-104">Network. encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="08d35-104">Network.encodedFrameRate</span></span>

<span data-ttu-id="08d35-105">A propriedade **encodedFrameRate** recupera a taxa de quadros de vídeo especificada pelo autor do conteúdo em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="08d35-105">The **encodedFrameRate** property retrieves the video frame rate specified by the content author in frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d35-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="08d35-106">Syntax</span></span>

<span data-ttu-id="08d35-107">*Player*. *rede*. **encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="08d35-107">*player*.*network*.**encodedFrameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="08d35-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="08d35-108">Possible Values</span></span>

<span data-ttu-id="08d35-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="08d35-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="08d35-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08d35-110">Examples</span></span>

<span data-ttu-id="08d35-111">O exemplo de JScript a seguir usa a *rede*. **encodedFrameRate** para exibir a taxa de quadros especificada quando o arquivo foi codificado.</span><span class="sxs-lookup"><span data-stu-id="08d35-111">The following JScript example uses *Network*.**encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="08d35-112">As informações são exibidas em um DIV HTML criado com ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="08d35-112">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="08d35-113">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="08d35-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="08d35-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08d35-114">Requirements</span></span>



| <span data-ttu-id="08d35-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="08d35-115">Requirement</span></span> | <span data-ttu-id="08d35-116">Valor</span><span class="sxs-lookup"><span data-stu-id="08d35-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08d35-117">Versão</span><span class="sxs-lookup"><span data-stu-id="08d35-117">Version</span></span><br/> | <span data-ttu-id="08d35-118">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="08d35-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="08d35-119">DLL</span><span class="sxs-lookup"><span data-stu-id="08d35-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="08d35-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08d35-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d35-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="08d35-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d35-122">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="08d35-122">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="08d35-123">**Network. taxa de quadros**</span><span class="sxs-lookup"><span data-stu-id="08d35-123">**Network.frameRate**</span></span>](network-framerate.md)
</dt> </dl>

 

 





