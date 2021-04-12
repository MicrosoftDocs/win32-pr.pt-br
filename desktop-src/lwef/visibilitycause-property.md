---
title: Propriedade VisibilityCause
description: Propriedade VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364036"
---
# <a name="visibilitycause-property"></a><span data-ttu-id="54dec-103">Propriedade VisibilityCause</span><span class="sxs-lookup"><span data-stu-id="54dec-103">VisibilityCause Property</span></span>

<span data-ttu-id="54dec-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54dec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="54dec-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="54dec-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="54dec-106">Retorna um valor inteiro que especifica o que causou o estado visível do caractere.</span><span class="sxs-lookup"><span data-stu-id="54dec-106">Returns an integer value that specifies what caused the character's visible state.</span></span>

</dd> <dt>

<span data-ttu-id="54dec-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="54dec-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="54dec-108">*agente* do. **Caracteres ("***characterid***"). VisibilityCause**</span><span class="sxs-lookup"><span data-stu-id="54dec-108">*agent*.**Characters("***CharacterID***").VisibilityCause**</span></span>



| <span data-ttu-id="54dec-109">Valor</span><span class="sxs-lookup"><span data-stu-id="54dec-109">Value</span></span> | <span data-ttu-id="54dec-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="54dec-110">Description</span></span>                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54dec-111">0</span><span class="sxs-lookup"><span data-stu-id="54dec-111">0</span></span>     | <span data-ttu-id="54dec-112">O caractere não foi mostrado.</span><span class="sxs-lookup"><span data-stu-id="54dec-112">The character has not been shown.</span></span>                                                                            |
| <span data-ttu-id="54dec-113">1</span><span class="sxs-lookup"><span data-stu-id="54dec-113">1</span></span>     | <span data-ttu-id="54dec-114">O usuário ocultou o caractere usando o comando no menu pop-up do ícone da barra de tarefas do caractere ou usando a entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="54dec-114">User hid the character using the command on the character's taskbar icon pop-up menu or using speech input..</span></span> |
| <span data-ttu-id="54dec-115">2</span><span class="sxs-lookup"><span data-stu-id="54dec-115">2</span></span>     | <span data-ttu-id="54dec-116">O usuário mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="54dec-116">The user showed the character.</span></span>                                                                               |
| <span data-ttu-id="54dec-117">3</span><span class="sxs-lookup"><span data-stu-id="54dec-117">3</span></span>     | <span data-ttu-id="54dec-118">O aplicativo ocultou o caractere.</span><span class="sxs-lookup"><span data-stu-id="54dec-118">Your application hid the character.</span></span>                                                                          |
| <span data-ttu-id="54dec-119">4</span><span class="sxs-lookup"><span data-stu-id="54dec-119">4</span></span>     | <span data-ttu-id="54dec-120">Seu aplicativo mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="54dec-120">Your application showed the character.</span></span>                                                                       |
| <span data-ttu-id="54dec-121">5</span><span class="sxs-lookup"><span data-stu-id="54dec-121">5</span></span>     | <span data-ttu-id="54dec-122">Outro aplicativo cliente ocultou o caractere.</span><span class="sxs-lookup"><span data-stu-id="54dec-122">Another client application hid the character.</span></span>                                                                |
| <span data-ttu-id="54dec-123">6</span><span class="sxs-lookup"><span data-stu-id="54dec-123">6</span></span>     | <span data-ttu-id="54dec-124">Outro aplicativo cliente mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="54dec-124">Another client application showed the character.</span></span>                                                             |
| <span data-ttu-id="54dec-125">7</span><span class="sxs-lookup"><span data-stu-id="54dec-125">7</span></span>     | <span data-ttu-id="54dec-126">O usuário ocultou o caractere usando o comando no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="54dec-126">The user hid the character using the command on the character's pop-up menu.</span></span>                                 |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54dec-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="54dec-127">Remarks</span></span>

<span data-ttu-id="54dec-128">Você pode usar essa propriedade para determinar o que causou o caractere a ser movido quando mais de um aplicativo estiver compartilhando (carregado) o mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="54dec-128">You can use this property to determine what caused the character to move when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="54dec-129">Esses valores são os mesmos retornados pelos eventos [**show**](show-event.md) e [**Hide**](hide-event.md) .</span><span class="sxs-lookup"><span data-stu-id="54dec-129">These values are the same as those returned by the [**Show**](show-event.md) and [**Hide**](hide-event.md) events.</span></span>

## <a name="see-also"></a><span data-ttu-id="54dec-130">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="54dec-130">See Also</span></span>

<span data-ttu-id="54dec-131">[**Ocultar evento**](hide-event.md), [**Mostrar evento**](show-event.md), [**ocultar método**](hide-method.md), [**Mostrar método**](show-method.md)</span><span class="sxs-lookup"><span data-stu-id="54dec-131">[**Hide event**](hide-event.md), [**Show event**](show-event.md), [**Hide method**](hide-method.md), [**Show method**](show-method.md)</span></span>


 

 




