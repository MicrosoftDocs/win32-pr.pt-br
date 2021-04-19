---
title: Controls. currentPosition
description: A propriedade currentPosition especifica ou recupera a posição atual no item de mídia em segundos desde o início.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Controls. currentPosition Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763363"
---
# <a name="controlscurrentposition"></a><span data-ttu-id="82714-104">Controls. currentPosition</span><span class="sxs-lookup"><span data-stu-id="82714-104">Controls.currentPosition</span></span>

<span data-ttu-id="82714-105">A propriedade **CurrentPosition** especifica ou recupera a posição atual no item de mídia em segundos desde o início.</span><span class="sxs-lookup"><span data-stu-id="82714-105">The **currentPosition** property specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a><span data-ttu-id="82714-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="82714-106">Possible Values</span></span>

<span data-ttu-id="82714-107">Essa propriedade é um **número** de leitura/gravação (**duplo**).</span><span class="sxs-lookup"><span data-stu-id="82714-107">This property is a read/write **Number** (**double**).</span></span>

## <a name="examples"></a><span data-ttu-id="82714-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="82714-108">Examples</span></span>

<span data-ttu-id="82714-109">O exemplo a seguir usa **CurrentPosition** para buscar uma posição fornecida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="82714-109">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="82714-110">Um elemento de botão HTML é criado para executar o código JScript.</span><span class="sxs-lookup"><span data-stu-id="82714-110">An HTML BUTTON element is created to execute the JScript code.</span></span> <span data-ttu-id="82714-111">Um elemento de entrada de texto HTML, chamado SETPOSITION, foi criado para aceitar um valor, em segundos, do usuário.</span><span class="sxs-lookup"><span data-stu-id="82714-111">An HTML TEXT input element, named setPosition, was created to accept a value, in seconds, from the user.</span></span> <span data-ttu-id="82714-112">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="82714-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a><span data-ttu-id="82714-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82714-113">Requirements</span></span>



| <span data-ttu-id="82714-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="82714-114">Requirement</span></span> | <span data-ttu-id="82714-115">Valor</span><span class="sxs-lookup"><span data-stu-id="82714-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82714-116">Versão</span><span class="sxs-lookup"><span data-stu-id="82714-116">Version</span></span><br/> | <span data-ttu-id="82714-117">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="82714-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="82714-118">DLL</span><span class="sxs-lookup"><span data-stu-id="82714-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="82714-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82714-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82714-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="82714-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82714-121">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="82714-121">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





