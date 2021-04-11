---
title: Recuperando informações de erro
description: Recuperando informações de erro
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008395"
---
# <a name="retrieving-error-information"></a><span data-ttu-id="b7a87-103">Recuperando informações de erro</span><span class="sxs-lookup"><span data-stu-id="b7a87-103">Retrieving Error Information</span></span>

<span data-ttu-id="b7a87-104">Usando as interfaces e funções de tratamento de erros COM, você pode recuperar informações de erro da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b7a87-104">Using the COM error-handling interfaces and functions, you can retrieve error information as follows:</span></span>

1.  <span data-ttu-id="b7a87-105">Verifique se o valor retornado representa um erro que o objeto está preparado para manipular.</span><span class="sxs-lookup"><span data-stu-id="b7a87-105">Check whether the returned value represents an error that the object is prepared to handle.</span></span>
2.  <span data-ttu-id="b7a87-106">Chame [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro para a interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="b7a87-106">Call [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span> <span data-ttu-id="b7a87-107">Em seguida, chame [**ISupportErrorInfo:: InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) para verificar se o erro foi gerado pelo objeto que o retornou e se o objeto de erro pertence ao erro atual e não a uma chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="b7a87-107">Then call [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) to verify that the error was raised by the object that returned it and that the error object pertains to the current error and not to a previous call.</span></span>
3.  <span data-ttu-id="b7a87-108">Para obter um ponteiro para o objeto Error, chame a função [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="b7a87-108">To get a pointer to the error object, call the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function.</span></span>
4.  <span data-ttu-id="b7a87-109">Para recuperar informações do objeto de erro, use os métodos [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="b7a87-109">To retrieve information from the error object, use the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) methods.</span></span>

<span data-ttu-id="b7a87-110">Se o objeto não estiver preparado para lidar com o erro, mas precisar propagar as informações de erro mais adiante na cadeia de chamadas, ele deverá simplesmente passar o valor de retorno para seu chamador.</span><span class="sxs-lookup"><span data-stu-id="b7a87-110">If the object is not prepared to handle the error but needs to propagate the error information further down the call chain, it should simply pass the return value to its caller.</span></span> <span data-ttu-id="b7a87-111">Como a função [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) limpa as informações de erro e passa a propriedade do objeto de erro para o chamador, a função deve ser chamada somente pelo objeto que manipula o erro.</span><span class="sxs-lookup"><span data-stu-id="b7a87-111">Because the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function clears the error information and passes ownership of the error object to the caller, the function should be called only by the object that handles the error.</span></span>

 

 