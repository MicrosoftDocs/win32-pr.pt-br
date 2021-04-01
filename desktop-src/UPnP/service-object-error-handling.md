---
title: Tratamento de erros de objeto de serviço
description: Quando ocorre um erro em um objeto de serviço, o valor de retorno para a chamada IDispatch Invoke deve ser DISP \_ e \_ Exception, e o ponteiro do parâmetro pExceptInfo para uma estrutura EXCEPTINFO no deve ser preenchido.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084623"
---
# <a name="service-object-error-handling"></a><span data-ttu-id="94d62-103">Tratamento de erros de objeto de serviço</span><span class="sxs-lookup"><span data-stu-id="94d62-103">Service Object Error Handling</span></span>

<span data-ttu-id="94d62-104">Quando ocorre um erro em um objeto de serviço, o valor de retorno para a chamada [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) deve ser DISP \_ e \_ Exception, e o ponteiro do parâmetro *pExceptInfo* para uma estrutura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) no deve ser preenchido.</span><span class="sxs-lookup"><span data-stu-id="94d62-104">When an error occurs in a service object, the return value for the call [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) should be DISP\_E\_EXCEPTION, and the *pExceptInfo* parameter pointer to an [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure in the should be filled in.</span></span>

<span data-ttu-id="94d62-105">Especificamente, os membros **bstrname** e **BstrDescription** da estrutura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) são usados pelo host do dispositivo com tecnologia UPnP para criar uma resposta de falha de UPnP; **bstrname** é o código de erro e **bstrDescription** é a descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="94d62-105">Specifically, the **bstrSource**, and **bstrDescription** members of the [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure are used by the Device Host with UPnP technology to create a UPnP Fault response; **bstrSource** is the error code and **bstrDescription** is the error description.</span></span>

 

 