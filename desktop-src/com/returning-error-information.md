---
title: Retornando informações de erro
description: Retornando informações de erro
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366739"
---
# <a name="returning-error-information"></a><span data-ttu-id="87784-103">Retornando informações de erro</span><span class="sxs-lookup"><span data-stu-id="87784-103">Returning Error Information</span></span>

<span data-ttu-id="87784-104">Usando as interfaces e funções de tratamento de erros COM, você pode retornar informações de erro executando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="87784-104">Using the COM error-handling interfaces and functions, you can return error information by performing the following the steps:</span></span>

1.  <span data-ttu-id="87784-105">Implemente a interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="87784-105">Implement the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span>
2.  <span data-ttu-id="87784-106">Para criar uma instância do objeto de erro genérico, chame a função [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="87784-106">To create an instance of the generic error object, call the [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) function.</span></span>
3.  <span data-ttu-id="87784-107">Para definir seu conteúdo, use os métodos [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="87784-107">To set its contents, use the [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) methods.</span></span>
4.  <span data-ttu-id="87784-108">Para associar o objeto de erro ao thread lógico atual, chame a função [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="87784-108">To associate the error object with the current logical thread, call the [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) function.</span></span>

<span data-ttu-id="87784-109">As interfaces de tratamento de erros criam e gerenciam um objeto de erro, que fornece informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="87784-109">The error handling interfaces create and manage an error object, which provides information about the error.</span></span> <span data-ttu-id="87784-110">O objeto de erro não é o mesmo que o objeto que encontrou o erro.</span><span class="sxs-lookup"><span data-stu-id="87784-110">The error object is not the same as the object that encountered the error.</span></span> <span data-ttu-id="87784-111">É um objeto separado associado ao thread atual de execução.</span><span class="sxs-lookup"><span data-stu-id="87784-111">It is a separate object associated with the current thread of execution.</span></span>

 

 