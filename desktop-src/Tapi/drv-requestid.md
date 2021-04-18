---
description: O \_ tipo de dados drv REQUESTID é usado para fornecer um identificador exclusivo para uma solicitação ao provedor de serviços.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788068"
---
# <a name="drv_requestid"></a><span data-ttu-id="db4ef-103">DRV \_ REQUESTID</span><span class="sxs-lookup"><span data-stu-id="db4ef-103">DRV\_REQUESTID</span></span>

<span data-ttu-id="db4ef-104">O tipo de dados **drv \_ REQUESTID** é usado para fornecer um identificador exclusivo para uma solicitação ao provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="db4ef-104">The **DRV\_REQUESTID** datatype is used to supply a unique identifier for a request to the service provider.</span></span> <span data-ttu-id="db4ef-105">Um valor desse tipo é passado como um parâmetro para cada função que permite a operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="db4ef-105">A value of this type is passed as a parameter to every function that allows for asynchronous operation.</span></span> <span data-ttu-id="db4ef-106">Se a operação for assíncrona, o provedor de serviços retornará esse valor como o valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="db4ef-106">If the operation is asynchronous, the service provider returns this value as the return value of the function.</span></span> <span data-ttu-id="db4ef-107">Sempre que o provedor de serviços sinaliza uma solicitação como assíncrona dessa forma, ele deve eventualmente relatar que a operação foi concluída chamando a função de retorno de chamada [*\_ proc de conclusão*](/windows/win32/api/tspi/nc-tspi-async_completion) .</span><span class="sxs-lookup"><span data-stu-id="db4ef-107">Whenever the service provider flags a request as asynchronous in this way, it must eventually report the operation is complete by calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function.</span></span>

<span data-ttu-id="db4ef-108">A TAPI garante que os valores **drv \_ REQUESTID** fornecidos sejam estritamente positivos, ou seja, entre os valores de 0x00000001 e 0x7FFFFFFF, inclusive.</span><span class="sxs-lookup"><span data-stu-id="db4ef-108">TAPI ensures that the **DRV\_REQUESTID** values it supplies are strictly positive, that is, between the values of 0x00000001 and 0x7FFFFFFF, inclusive.</span></span> <span data-ttu-id="db4ef-109">Além disso, os valores são exclusivos, pois nenhum valor retornado de uma função para sinalizar a solicitação como assíncrona será reutilizado antes que a operação seja relatada como concluída.</span><span class="sxs-lookup"><span data-stu-id="db4ef-109">Furthermore, the values are unique in that no value returned from a function to flag the request as asynchronous will be re-used before the operation is reported complete.</span></span>

 

 
