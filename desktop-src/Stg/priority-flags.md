---
title: Sinalizadores de prioridade
description: O sinalizador de prioridade abre um objeto de armazenamento no modo de prioridade.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Sinalizadores de prioridade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006201"
---
# <a name="priority-flags"></a><span data-ttu-id="adc50-104">Sinalizadores de prioridade</span><span class="sxs-lookup"><span data-stu-id="adc50-104">Priority Flags</span></span>

<span data-ttu-id="adc50-105">O sinalizador de prioridade abre um objeto de armazenamento no modo de prioridade.</span><span class="sxs-lookup"><span data-stu-id="adc50-105">The priority flag opens a storage object in priority mode.</span></span> <span data-ttu-id="adc50-106">Quando ele abre um objeto, um aplicativo geralmente funciona a partir de uma cópia de instantâneo porque outros aplicativos também podem estar usando o objeto ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="adc50-106">When it opens an object, an application usually works from a snapshot copy because other applications may also be using the object at the same time.</span></span> <span data-ttu-id="adc50-107">No entanto, ao abrir um objeto de armazenamento no modo de prioridade, o aplicativo tem direitos exclusivos para confirmar as alterações no objeto.</span><span class="sxs-lookup"><span data-stu-id="adc50-107">When opening a storage object in priority mode, however, the application has exclusive rights to commit changes to the object.</span></span>

<span data-ttu-id="adc50-108">O modo de prioridade permite que um aplicativo Leia alguns fluxos do armazenamento antes de abrir o objeto em um modo que exige que o sistema faça uma cópia de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="adc50-108">Priority mode enables an application to read some streams from storage before opening the object in a mode that would require the system to make a snapshot copy.</span></span> <span data-ttu-id="adc50-109">Como o aplicativo tem acesso exclusivo, ele não precisa fazer uma cópia de instantâneo do objeto.</span><span class="sxs-lookup"><span data-stu-id="adc50-109">Because the application has exclusive access, it does not have to make a snapshot copy of the object.</span></span> <span data-ttu-id="adc50-110">Quando o aplicativo abre o objeto subsequentemente em um modo em que uma cópia de instantâneo é necessária, o aplicativo pode excluir os fluxos já lidos do instantâneo, reduzindo assim a sobrecarga de abrir o objeto.</span><span class="sxs-lookup"><span data-stu-id="adc50-110">When the application subsequently opens the object in a mode where a snapshot copy is required, the application can exclude the streams it has already read from the snapshot, thereby reducing the overhead of opening the object.</span></span>

<span data-ttu-id="adc50-111">Como outros aplicativos não podem confirmar alterações em um objeto enquanto ele está aberto no modo de prioridade, os aplicativos devem manter o objeto nesse modo pelo menor tempo possível.</span><span class="sxs-lookup"><span data-stu-id="adc50-111">Because other applications cannot commit changes to an object while it is open in priority mode, applications should keep the object in that mode for as short a time as possible.</span></span>

 

 




