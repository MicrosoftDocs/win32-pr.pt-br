---
description: Alguns tipos definidos por TSPI são identificadores opacos.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Identificadores opacos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502004"
---
# <a name="opaque-handles"></a><span data-ttu-id="dd13d-103">Identificadores opacos</span><span class="sxs-lookup"><span data-stu-id="dd13d-103">Opaque Handles</span></span>

<span data-ttu-id="dd13d-104">Alguns tipos definidos por TSPI são identificadores opacos.</span><span class="sxs-lookup"><span data-stu-id="dd13d-104">A few types defined by TSPI are opaque handles.</span></span> <span data-ttu-id="dd13d-105">Eles são usados em TSPI como referências públicas para estruturas de dados privadas.</span><span class="sxs-lookup"><span data-stu-id="dd13d-105">These are used in TSPI as public references to private data structures.</span></span> <span data-ttu-id="dd13d-106">Isso permite a verificação de tipos de parâmetros fornecidos aos procedimentos de interface enquanto ainda oferece uma medida de proteção de tipo.</span><span class="sxs-lookup"><span data-stu-id="dd13d-106">This allows type-checking of parameters supplied to the interface procedures while still giving a measure of type protection.</span></span> <span data-ttu-id="dd13d-107">Somente o proprietário da estrutura de dados privada sabe como interpretar o tipo opaco como uma referência à sua representação de estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="dd13d-107">Only the owner of the private data structure knows how to interpret the opaque type as a reference to its data structure representation.</span></span> <span data-ttu-id="dd13d-108">Como um exemplo de como as alças opacas são usadas, considere um dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="dd13d-108">As an example of how opaque handles are used, consider a phone device.</span></span> <span data-ttu-id="dd13d-109">A TAPI e o provedor de serviços normalmente mantêm estruturas de dados que representam suas respectivas exibições do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd13d-109">Both TAPI and the service provider typically maintain data structures representing their respective views of the device.</span></span>

<span data-ttu-id="dd13d-110">Em estruturas de dados de telefone típicas mantidas pela TAPI e por um provedor de serviços, cada uma contém um identificador opaco para a outra estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="dd13d-110">In typical phone data structures maintained by TAPI and a service provider, each contains an opaque handle for the other data structure.</span></span> <span data-ttu-id="dd13d-111">Elas eram trocadas em uma etapa de inicialização antecipada.</span><span class="sxs-lookup"><span data-stu-id="dd13d-111">These were exchanged at an early initialization step.</span></span> <span data-ttu-id="dd13d-112">Quando a TAPI chama uma função TSPI, ela passa o identificador opaco para se referir ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd13d-112">When TAPI calls a TSPI function, it passes the opaque handle to refer to the device.</span></span> <span data-ttu-id="dd13d-113">O provedor de serviços sabe como resolver isso como uma referência (seta) para sua estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="dd13d-113">The service provider knows how to resolve this as a reference (arrow) to its data structure.</span></span> <span data-ttu-id="dd13d-114">Um processo semelhante ocorre quando o provedor de serviços chama uma função de retorno de chamada na TAPI.</span><span class="sxs-lookup"><span data-stu-id="dd13d-114">A similar process occurs when the service provider calls a callback function in TAPI.</span></span>

 

 



