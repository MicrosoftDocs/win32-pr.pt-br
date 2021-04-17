---
title: Método do opAll
description: Método do opAll
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105782531"
---
# <a name="stopall-method"></a><span data-ttu-id="f39fa-103">Método do opAll</span><span class="sxs-lookup"><span data-stu-id="f39fa-103">StopAll Method</span></span>

<span data-ttu-id="f39fa-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f39fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f39fa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="f39fa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f39fa-106">Interrompe todas as solicitações de animação ou tipos especificados de solicitações para o caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="f39fa-106">Stops all animation requests or specified types of requests for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="f39fa-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="f39fa-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f39fa-108">\*agente do ***. Caracteres ("*** characterid \* \* *"). Tipo de interopall* \*  \[ \]</span><span class="sxs-lookup"><span data-stu-id="f39fa-108">*agent ***.Characters ("*** CharacterID\*\*\*").StopAll*\* \[*Type*\]</span></span>



| <span data-ttu-id="f39fa-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f39fa-109">Part</span></span>   | <span data-ttu-id="f39fa-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f39fa-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f39fa-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="f39fa-111">*Type*</span></span> | <span data-ttu-id="f39fa-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f39fa-112">Optional.</span></span> <span data-ttu-id="f39fa-113">Para usar esse parâmetro, você pode usar qualquer um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f39fa-113">To use this parameter you can use any of the following values.</span></span> <span data-ttu-id="f39fa-114">Você também pode especificar vários tipos separando-os com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="f39fa-114">You can also specify multiple types by separating them with commas.</span></span> <br/> <span data-ttu-id="f39fa-115">"**Obter**"</span><span class="sxs-lookup"><span data-stu-id="f39fa-115">"**Get**"</span></span> <br/> <span data-ttu-id="f39fa-116">Para interromper todas as solicitações [**Get**](get-method.md) em fila.</span><span class="sxs-lookup"><span data-stu-id="f39fa-116">To stop all queued [**Get**](get-method.md) requests.</span></span><br/> <span data-ttu-id="f39fa-117">"**NonQueuedGet**"</span><span class="sxs-lookup"><span data-stu-id="f39fa-117">"**NonQueuedGet**"</span></span> <br/> <span data-ttu-id="f39fa-118">Para interromper todas as solicitações [**Get**](get-method.md) não enfileiradas (método **Get** com o parâmetro **Queue** definido como **false**).</span><span class="sxs-lookup"><span data-stu-id="f39fa-118">To stop all non-queued [**Get**](get-method.md) requests (**Get** method with **Queue** parameter set to **False**).</span></span><br/> <span data-ttu-id="f39fa-119">"**Mover**"</span><span class="sxs-lookup"><span data-stu-id="f39fa-119">"**Move**"</span></span> <br/> <span data-ttu-id="f39fa-120">Para interromper todas as solicitações [**MoveTo**](moveto-method.md) enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="f39fa-120">To stop all queued [**MoveTo**](moveto-method.md) requests.</span></span><br/> <span data-ttu-id="f39fa-121">"**Reproduzir**"</span><span class="sxs-lookup"><span data-stu-id="f39fa-121">"**Play**"</span></span> <br/> <span data-ttu-id="f39fa-122">Para interromper todas as solicitações de [**reprodução**](play-method.md) em fila.</span><span class="sxs-lookup"><span data-stu-id="f39fa-122">To stop all queued [**Play**](play-method.md) requests.</span></span><br/> <span data-ttu-id="f39fa-123">"**Fale**"</span><span class="sxs-lookup"><span data-stu-id="f39fa-123">"**Speak**"</span></span> <br/> <span data-ttu-id="f39fa-124">Para interromper todas as solicitações de [**fala**](speak-method.md) enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="f39fa-124">To stop all queued [**Speak**](speak-method.md) requests.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f39fa-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f39fa-125">Remarks</span></span>

<span data-ttu-id="f39fa-126">Se você não definir o parâmetro de **tipo** , o servidor interromperá todas as animações para o caractere, incluindo solicitações [**Get**](get-method.md) enfileiradas e não enfileiradas, e limpará sua fila de animação.</span><span class="sxs-lookup"><span data-stu-id="f39fa-126">If you don't set the **Type** parameter, the server stops all animations for the character, including queued and non-queued [**Get**](get-method.md) requests, and clears its animation queue.</span></span> <span data-ttu-id="f39fa-127">Ele também interrompe a reprodução de uma animação de ocultar ou mostrar um caractere.</span><span class="sxs-lookup"><span data-stu-id="f39fa-127">It also stops playing a character's Hiding or Showing animation.</span></span>

<span data-ttu-id="f39fa-128">Esse método não gerará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="f39fa-128">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="f39fa-129">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f39fa-129">See Also</span></span>

[<span data-ttu-id="f39fa-130">**Método Stop**</span><span class="sxs-lookup"><span data-stu-id="f39fa-130">**Stop method**</span></span>](stop-method.md)


 

