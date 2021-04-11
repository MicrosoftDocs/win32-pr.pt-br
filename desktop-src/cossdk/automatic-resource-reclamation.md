---
description: Recuperação automática de recursos
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Recuperação automática de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296107"
---
# <a name="automatic-resource-reclamation"></a><span data-ttu-id="11499-103">Recuperação automática de recursos</span><span class="sxs-lookup"><span data-stu-id="11499-103">Automatic Resource Reclamation</span></span>

<span data-ttu-id="11499-104">O COM+ notifica o Gerenciador do dispensador sempre que o tempo de vida de um objeto termina.</span><span class="sxs-lookup"><span data-stu-id="11499-104">COM+ notifies the dispenser manager each time an object's lifetime ends.</span></span> <span data-ttu-id="11499-105">Em seguida, o Gerenciador do dispensador notifica cada portador da dispensador do recurso registrado para ver se ele tem algum recurso ainda mantido por esse objeto.</span><span class="sxs-lookup"><span data-stu-id="11499-105">The dispenser manager then notifies each registered resource dispenser's Holder to see whether it has any resources still held by this object.</span></span> <span data-ttu-id="11499-106">Nesse caso, esses recursos são liberados, impedindo a possibilidade de vazamentos de recursos por componentes que obtêm recursos por meio de um dispensador de recursos.</span><span class="sxs-lookup"><span data-stu-id="11499-106">If so, those resources are freed, preventing the possibility of resource leaks by components that get resources through a resource dispenser.</span></span>

<span data-ttu-id="11499-107">O recurso de recuperação automática é uma opção desativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="11499-107">The auto-reclamation feature is an option that is turned off by default.</span></span> <span data-ttu-id="11499-108">Um dispensador de recurso pode optar por habilitar essa opção e, ao fazer isso, garante que uma referência a qualquer recurso dispensado para um objeto nunca seja retornada pelos métodos de objeto.</span><span class="sxs-lookup"><span data-stu-id="11499-108">A resource dispenser can choose to enable this option and, in doing so, guarantees that a reference to any resource dispensed to an object is never returned by the object methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11499-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11499-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11499-110">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="11499-110">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



