---
title: Network. framesSkipped
description: A propriedade framesSkipped recupera o número total de quadros ignorados durante a reprodução.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Network. framesSkipped Windows Media Player
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810782"
---
# <a name="networkframesskipped"></a><span data-ttu-id="56e77-104">Network. framesSkipped</span><span class="sxs-lookup"><span data-stu-id="56e77-104">Network.framesSkipped</span></span>

<span data-ttu-id="56e77-105">A propriedade **framesSkipped** recupera o número total de quadros ignorados durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="56e77-105">The **framesSkipped** property retrieves the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e77-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="56e77-106">Syntax</span></span>

<span data-ttu-id="56e77-107">*Player*. *rede*. **framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="56e77-107">*player*.*network*.**framesSkipped**</span></span>

## <a name="possible-values"></a><span data-ttu-id="56e77-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="56e77-108">Possible Values</span></span>

<span data-ttu-id="56e77-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="56e77-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="56e77-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="56e77-110">Examples</span></span>

<span data-ttu-id="56e77-111">O exemplo de JScript a seguir usa a *rede*. **framesSkipped** para exibir o número total de quadros ignorados durante a reprodução quando o usuário clica em um botão.</span><span class="sxs-lookup"><span data-stu-id="56e77-111">The following JScript example uses *Network*.**framesSkipped** to display the total number of frames skipped during playback when the user clicks a button.</span></span> <span data-ttu-id="56e77-112">As informações são exibidas em uma DIV HTML criada com ID = "FS".</span><span class="sxs-lookup"><span data-stu-id="56e77-112">The information is displayed in an HTML DIV created with ID = "FS".</span></span> <span data-ttu-id="56e77-113">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="56e77-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a><span data-ttu-id="56e77-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56e77-114">Requirements</span></span>



| <span data-ttu-id="56e77-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56e77-115">Requirement</span></span> | <span data-ttu-id="56e77-116">Valor</span><span class="sxs-lookup"><span data-stu-id="56e77-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56e77-117">Versão</span><span class="sxs-lookup"><span data-stu-id="56e77-117">Version</span></span><br/> | <span data-ttu-id="56e77-118">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="56e77-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="56e77-119">DLL</span><span class="sxs-lookup"><span data-stu-id="56e77-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="56e77-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e77-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e77-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="56e77-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e77-122">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="56e77-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





