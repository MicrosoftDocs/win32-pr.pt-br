---
title: Controls. currentPositionString
description: A propriedade currentPositionString recupera a posição atual no item de mídia como uma cadeia de caracteres formatada como HH MM SS (horas, minutos e segundos).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Controls. currentPositionString Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770512"
---
# <a name="controlscurrentpositionstring"></a><span data-ttu-id="d811c-104">Controls. currentPositionString</span><span class="sxs-lookup"><span data-stu-id="d811c-104">Controls.currentPositionString</span></span>

<span data-ttu-id="d811c-105">A propriedade **currentPositionString** recupera a posição atual no item de mídia como uma **cadeia de caracteres** formatada como hh: mm: SS (horas, minutos e segundos).</span><span class="sxs-lookup"><span data-stu-id="d811c-105">The **currentPositionString** property retrieves the current position in the media item as a **String** formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a><span data-ttu-id="d811c-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d811c-106">Possible Values</span></span>

<span data-ttu-id="d811c-107">Esta propriedade é uma **cadeia de caracteres** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d811c-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d811c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d811c-108">Remarks</span></span>

<span data-ttu-id="d811c-109">Se o item de mídia tiver menos de uma hora, a parte HH: não será incluída.</span><span class="sxs-lookup"><span data-stu-id="d811c-109">If the media item is less than an hour long, the HH: portion is not included.</span></span>

> [!Note]  
> <span data-ttu-id="d811c-110">Você deve incluir o código para interromper o timer quando o item de mídia for interrompido ou pausado.</span><span class="sxs-lookup"><span data-stu-id="d811c-110">You should include code to stop the timer when the media item is stopped or paused.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d811c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d811c-111">Examples</span></span>

<span data-ttu-id="d811c-112">O exemplo de JScript a seguir inicia um temporizador HTML que exibe a posição atual do arquivo de mídia em intervalos de um segundo.</span><span class="sxs-lookup"><span data-stu-id="d811c-112">The following JScript example starts an HTML timer that displays the current position of the media file at one-second intervals.</span></span> <span data-ttu-id="d811c-113">Um elemento de texto HTML chamado mytext foi criado para exibir a posição atual.</span><span class="sxs-lookup"><span data-stu-id="d811c-113">An HTML TEXT element named MyText was created to display the current position.</span></span> <span data-ttu-id="d811c-114">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d811c-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a><span data-ttu-id="d811c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d811c-115">Requirements</span></span>



| <span data-ttu-id="d811c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d811c-116">Requirement</span></span> | <span data-ttu-id="d811c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d811c-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d811c-118">Versão</span><span class="sxs-lookup"><span data-stu-id="d811c-118">Version</span></span><br/> | <span data-ttu-id="d811c-119">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d811c-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d811c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d811c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="d811c-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d811c-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d811c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d811c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d811c-123">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="d811c-123">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





