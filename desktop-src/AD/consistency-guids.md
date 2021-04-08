---
title: GUIDs de consistência
description: Os GUIDs de consistência são uma estratégia de detecção que permite que um aplicativo detecte atualizações parciais.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004812"
---
# <a name="consistency-guids"></a><span data-ttu-id="a2d91-103">GUIDs de consistência</span><span class="sxs-lookup"><span data-stu-id="a2d91-103">Consistency GUIDs</span></span>

<span data-ttu-id="a2d91-104">Os GUIDs de consistência são uma estratégia de detecção que permite que um aplicativo detecte atualizações parciais.</span><span class="sxs-lookup"><span data-stu-id="a2d91-104">Consistency GUIDs are a detection strategy that allows an application to detect partial updates.</span></span> <span data-ttu-id="a2d91-105">Um GUID de consistência (identificador global exclusivo) é aplicado a cada objeto em um conjunto relacionado.</span><span class="sxs-lookup"><span data-stu-id="a2d91-105">A consistency GUID (Globally Unique IDentifier) is applied to each object in a related set.</span></span> <span data-ttu-id="a2d91-106">Na implementação, um aplicativo de origem gera um novo GUID e o aplica a cada objeto que ele atualiza no conjunto de objetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="a2d91-106">In implementation, a source application generates a new GUID and applies it to each object it updates in the set of related objects.</span></span> <span data-ttu-id="a2d91-107">Em seguida, ele aplica o novo GUID ao restante dos objetos no conjunto e termina aplicando o novo GUID ao objeto "Master".</span><span class="sxs-lookup"><span data-stu-id="a2d91-107">It then applies the new GUID to the rest of the objects in the set, and finishes by applying the new GUID to the "master" object.</span></span> <span data-ttu-id="a2d91-108">Normalmente, o objeto "Master" será um contêiner que é o pai dos outros objetos no conjunto.</span><span class="sxs-lookup"><span data-stu-id="a2d91-108">Typically, the "master" object will be a container that is the parent of the other objects in the set.</span></span>

<span data-ttu-id="a2d91-109">Algumas considerações importantes:</span><span class="sxs-lookup"><span data-stu-id="a2d91-109">Some important considerations:</span></span>

-   <span data-ttu-id="a2d91-110">Os GUIDs de consistência combinados com contagens de objetos ou somas de verificação são mais eficazes do que os GUIDs de consistência sozinhos, pois o aplicativo que lê os objetos pode não saber quantos objetos com o GUID devem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="a2d91-110">Consistency GUIDs combined with object counts or checksums are more effective than consistency GUIDs alone, because the application reading the objects may not know how many objects with the GUID should be present.</span></span>
-   <span data-ttu-id="a2d91-111">Os aplicativos devem gerar seus próprios GUIDs (uma API do Microsoft Win32, UuidCreate, fornece essa função) e não usar os GUIDs gerados pelo sistema encontrados no atributo **objectGUID** de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a2d91-111">Applications must generate their own GUIDs (a Microsoft Win32 API, UuidCreate, provides this function), and not use the system-generated GUIDs found in an object's **objectGUID** attribute.</span></span> <span data-ttu-id="a2d91-112">Isso ocorre porque um GUID de consistência precisa ser alterado cada vez que o conjunto de objetos é atualizado.</span><span class="sxs-lookup"><span data-stu-id="a2d91-112">This is because a consistency GUID needs to change each time the set of objects is updated.</span></span> <span data-ttu-id="a2d91-113">Os GUIDs de identidade do objeto encontrados no **objectGUID** nunca são alterados após a criação do objeto.</span><span class="sxs-lookup"><span data-stu-id="a2d91-113">Object identity GUIDs found in **objectGUID** never change after the object has been created.</span></span>
-   <span data-ttu-id="a2d91-114">Os GUIDs de consistência pressupõem que nenhum objeto seja compartilhado entre os conjuntos, de modo que cada conjunto pode ter um GUID de consistência exclusivo.</span><span class="sxs-lookup"><span data-stu-id="a2d91-114">Consistency GUIDs assume that no object is shared among sets, so each set can have a unique consistency GUID.</span></span>

 

 




