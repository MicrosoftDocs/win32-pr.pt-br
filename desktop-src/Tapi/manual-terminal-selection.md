---
description: Se as regras de seleção padrão não atenderem às necessidades do aplicativo, o aplicativo terá a opção de selecionar o terminal manualmente.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Seleção de terminal manual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95335402690c57cc3f564f5d238ca031df4b3549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661785"
---
# <a name="manual-terminal-selection"></a><span data-ttu-id="e43f1-103">Seleção de terminal manual</span><span class="sxs-lookup"><span data-stu-id="e43f1-103">Manual Terminal Selection</span></span>

<span data-ttu-id="e43f1-104">Se as regras de seleção padrão não atenderem às necessidades do aplicativo, o aplicativo terá a opção de selecionar o terminal como sempre tem: ou seja, ele poderá usar [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) para enumerar os fluxos presentes na chamada e selecionar o terminal nos fluxos apropriados (ou, no caso de terminais do multitrack, criar faixas para os fluxos e selecionar faixas criadas nos fluxos).</span><span class="sxs-lookup"><span data-stu-id="e43f1-104">If the rules of Default selection do not meet the needs of the application, the application has the option of selecting the terminal as it always has: that is, it can use [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) to enumerate the streams present on the call and select the terminal on the appropriate streams (or, in case of multitrack terminals, create tracks for the streams and select created tracks on the streams).</span></span>

 

 
