---
title: Propriedade MoveCause
description: Propriedade MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822665"
---
# <a name="movecause-property"></a><span data-ttu-id="3b35a-103">Propriedade MoveCause</span><span class="sxs-lookup"><span data-stu-id="3b35a-103">MoveCause Property</span></span>

<span data-ttu-id="3b35a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3b35a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3b35a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="3b35a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3b35a-106">Retorna um valor inteiro que especifica o que causou a última movimentação do caractere.</span><span class="sxs-lookup"><span data-stu-id="3b35a-106">Returns an integer value that specifies what caused the character's last move.</span></span>

</dd> <dt>

<span data-ttu-id="3b35a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="3b35a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3b35a-108">*agente* do. **Caracteres ("***characterid***"). MoveCause**</span><span class="sxs-lookup"><span data-stu-id="3b35a-108">*agent*.**Characters("***CharacterID***").MoveCause**</span></span>



| <span data-ttu-id="3b35a-109">Valor</span><span class="sxs-lookup"><span data-stu-id="3b35a-109">Value</span></span> | <span data-ttu-id="3b35a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b35a-110">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b35a-111">0</span><span class="sxs-lookup"><span data-stu-id="3b35a-111">0</span></span>     | <span data-ttu-id="3b35a-112">O caractere não foi movido.</span><span class="sxs-lookup"><span data-stu-id="3b35a-112">The character has not been moved.</span></span>                                                          |
| <span data-ttu-id="3b35a-113">1</span><span class="sxs-lookup"><span data-stu-id="3b35a-113">1</span></span>     | <span data-ttu-id="3b35a-114">O usuário moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="3b35a-114">The user moved the character.</span></span>                                                              |
| <span data-ttu-id="3b35a-115">2</span><span class="sxs-lookup"><span data-stu-id="3b35a-115">2</span></span>     | <span data-ttu-id="3b35a-116">Seu aplicativo moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="3b35a-116">Your application moved the character.</span></span>                                                      |
| <span data-ttu-id="3b35a-117">3</span><span class="sxs-lookup"><span data-stu-id="3b35a-117">3</span></span>     | <span data-ttu-id="3b35a-118">Outro aplicativo cliente moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="3b35a-118">Another client application moved the character.</span></span>                                            |
| <span data-ttu-id="3b35a-119">4</span><span class="sxs-lookup"><span data-stu-id="3b35a-119">4</span></span>     | <span data-ttu-id="3b35a-120">O servidor do agente moveu o caractere para mantê-lo na tela após a alteração da resolução da tela.</span><span class="sxs-lookup"><span data-stu-id="3b35a-120">The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b35a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b35a-121">Remarks</span></span>

<span data-ttu-id="3b35a-122">Você pode usar essa propriedade para determinar o que causou o caractere a ser movido, quando mais de um aplicativo estiver compartilhando (carregado) o mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="3b35a-122">You can use this property to determine what caused the character to move, when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="3b35a-123">Esses valores são os mesmos retornados pelo evento de [**movimentação**](move-event.md) .</span><span class="sxs-lookup"><span data-stu-id="3b35a-123">These values are the same as those returned by the [**Move**](move-event.md) event.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b35a-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3b35a-124">See Also</span></span>

<span data-ttu-id="3b35a-125">[**Mover evento**](move-event.md), [ **método MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="3b35a-125">[**Move event**](move-event.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




