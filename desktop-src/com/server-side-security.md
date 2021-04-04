---
title: Segurança de Server-Side
description: Segurança de Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917714"
---
# <a name="server-side-security"></a><span data-ttu-id="ab686-103">Segurança de Server-Side</span><span class="sxs-lookup"><span data-stu-id="ab686-103">Server-Side Security</span></span>

<span data-ttu-id="ab686-104">O servidor pode recuperar informações de segurança sobre um chamador ou representar o chamador usando os métodos de [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span><span class="sxs-lookup"><span data-stu-id="ab686-104">The server can retrieve security information about a caller or impersonate the caller by using the methods of [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity).</span></span> <span data-ttu-id="ab686-105">Uma implementação de **IServerSecurity** é fornecida pelo com no objeto de contexto para a chamada atual quando o empacotamento padrão é usado.</span><span class="sxs-lookup"><span data-stu-id="ab686-105">An implementation of **IServerSecurity** is supplied by COM on the context object for the current call when standard marshaling is used.</span></span> <span data-ttu-id="ab686-106">No entanto, essa interface pode estar ausente para algumas interfaces com marshaling personalizado.</span><span class="sxs-lookup"><span data-stu-id="ab686-106">However, this interface may be absent for some custom-marshaled interfaces.</span></span>

<span data-ttu-id="ab686-107">Quando uma chamada chega ao servidor, o servidor pode chamar [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obter um ponteiro para a interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) .</span><span class="sxs-lookup"><span data-stu-id="ab686-107">When a call arrives at the server, the server can call [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) to obtain a pointer to the [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface.</span></span> <span data-ttu-id="ab686-108">Com esse ponteiro, os métodos **IServerSecurity** podem ser chamados pelo servidor para descobrir quais são as configurações de autenticação do cliente e para representar o cliente, se necessário.</span><span class="sxs-lookup"><span data-stu-id="ab686-108">With this pointer, **IServerSecurity** methods can be called by the server to find out what the client's authentication settings are and to impersonate the client, if needed.</span></span> <span data-ttu-id="ab686-109">O objeto **IServerSecurity** é válido em qualquer thread no apartamento até que a chamada representada por **IServerSecurity** seja concluída.</span><span class="sxs-lookup"><span data-stu-id="ab686-109">The **IServerSecurity** object is valid on any thread in the apartment until the call represented by **IServerSecurity** completes.</span></span> <span data-ttu-id="ab686-110">Para obter mais informações sobre representação, consulte [representação](impersonation.md) e [encobrimento](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="ab686-110">For more information about impersonation, see [Impersonation](impersonation.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="ab686-111">As seguintes funções auxiliares que dependem da implementação da interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) do objeto de contexto de chamada também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="ab686-111">The following helper functions that rely on the call context object's [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) interface implementation are also available:</span></span>

-   [<span data-ttu-id="ab686-112">**CoQueryClientBlanket**</span><span class="sxs-lookup"><span data-stu-id="ab686-112">**CoQueryClientBlanket**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [<span data-ttu-id="ab686-113">**CoImpersonateClient**</span><span class="sxs-lookup"><span data-stu-id="ab686-113">**CoImpersonateClient**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [<span data-ttu-id="ab686-114">**CoRevertToSelf**</span><span class="sxs-lookup"><span data-stu-id="ab686-114">**CoRevertToSelf**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a><span data-ttu-id="ab686-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab686-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab686-116">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="ab686-116">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 