---
title: Obtendo uma identidade de codificação
description: Um aplicativo que está decodificando dados codificados pode obter a identidade da rotina usada para codificar os dados, antes de chamar uma rotina para decodificá-lo. A rotina MesInqProcEncodingId fornece essa identidade.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Chamada de procedimento remoto RPC, tarefas, obtendo identidade de codificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636759"
---
# <a name="obtaining-an-encoding-identity"></a><span data-ttu-id="55be9-105">Obtendo uma identidade de codificação</span><span class="sxs-lookup"><span data-stu-id="55be9-105">Obtaining an Encoding Identity</span></span>

<span data-ttu-id="55be9-106">Um aplicativo que está decodificando dados codificados pode obter a identidade da rotina usada para codificar os dados, antes de chamar uma rotina para decodificá-lo.</span><span class="sxs-lookup"><span data-stu-id="55be9-106">An application that is decoding encoded data can obtain the identity of the routine used to encode the data, prior to calling a routine to decode it.</span></span> <span data-ttu-id="55be9-107">A rotina [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) fornece essa identidade.</span><span class="sxs-lookup"><span data-stu-id="55be9-107">The [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) routine provides this identity.</span></span>

<span data-ttu-id="55be9-108">Cada procedimento em uma interface é atribuído a um número de identificação de número inteiro, chamado de *identificador de procedimento* ou *ID de proc*, pelo compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="55be9-108">Each procedure in an interface is assigned an integer identification number, called a *procedure identifier* or a *proc ID*, by the MIDL compiler.</span></span> <span data-ttu-id="55be9-109">A numeração começa com zero.</span><span class="sxs-lookup"><span data-stu-id="55be9-109">Numbering begins with zero.</span></span> <span data-ttu-id="55be9-110">As bibliotecas de tempo de execução RPC não estão envolvidas na conversão da ID do procedimento em uma chamada de procedimento real.</span><span class="sxs-lookup"><span data-stu-id="55be9-110">The RPC run-time libraries are not involved in translating the procedure ID into an actual procedure call.</span></span> <span data-ttu-id="55be9-111">Dada uma ID proc, seu aplicativo deve fornecer um meio de chamar o procedimento correto.</span><span class="sxs-lookup"><span data-stu-id="55be9-111">Given a proc ID, your application must provide a means of calling the correct procedure.</span></span> <span data-ttu-id="55be9-112">Normalmente, os desenvolvedores de aplicativos usam uma série de instruções **If** ou (ao usar C/C++) uma instrução **switch** para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="55be9-112">Typically, application developers use a series of **if** statements, or (when using C/C++) a **switch** statement for this purpose.</span></span>

 

 




