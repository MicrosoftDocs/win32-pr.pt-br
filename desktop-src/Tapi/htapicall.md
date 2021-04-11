---
description: O DataType HTAPICALL representa o identificador opaco TAPI para uma estrutura de dados de chamada.
ms.assetid: a2a17b03-5779-411e-8959-6e2de5e53c5a
title: HTAPICALL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abd90dc8453be5f5bec18e92b384b7ace830d14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296505"
---
# <a name="htapicall"></a><span data-ttu-id="e54bb-103">HTAPICALL</span><span class="sxs-lookup"><span data-stu-id="e54bb-103">HTAPICALL</span></span>

<span data-ttu-id="e54bb-104">O DataType **HTAPICALL** representa o identificador opaco TAPI para uma estrutura de dados de chamada.</span><span class="sxs-lookup"><span data-stu-id="e54bb-104">The **HTAPICALL** datatype represents the TAPI opaque handle for a call data structure.</span></span> <span data-ttu-id="e54bb-105">A TAPI deve resolver um valor desse tipo em uma referência à instância de estrutura de dados apropriada.</span><span class="sxs-lookup"><span data-stu-id="e54bb-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="e54bb-106">O provedor de serviços não deve tentar fazer referência a isso como se fosse um ponteiro, fazer suposições sobre seus valores ou interpretar sua representação de qualquer forma diferente de passar seu valor para a TAPI em momentos apropriados.</span><span class="sxs-lookup"><span data-stu-id="e54bb-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



