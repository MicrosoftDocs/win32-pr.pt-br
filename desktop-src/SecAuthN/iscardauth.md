---
description: A definição da interface ISCardAuth é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um provedor de serviços de cartão inteligente. A interface ISCardAuth pode ser usada para expor os serviços de autenticação com suporte por um cartão inteligente.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Interface ISCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461060"
---
# <a name="iscardauth-interface"></a><span data-ttu-id="5494f-103">Interface ISCardAuth</span><span class="sxs-lookup"><span data-stu-id="5494f-103">ISCardAuth interface</span></span>

<span data-ttu-id="5494f-104">\[A interface **ISCardAuth** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="5494f-104">\[The **ISCardAuth** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5494f-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5494f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5494f-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="5494f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="5494f-107">A definição da interface **ISCardAuth** é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um [*provedor de serviços*](../secgloss/c-gly.md)de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5494f-107">The **ISCardAuth** interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="5494f-108">A interface **ISCardAuth** pode ser usada para expor os serviços de autenticação com suporte por um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="5494f-108">The **ISCardAuth** interface can be used to expose authentication services supported by a smart card.</span></span> <span data-ttu-id="5494f-109">Esses serviços incluem autenticação de aplicativo, autenticação de cartão inteligente e autenticação de usuário.</span><span class="sxs-lookup"><span data-stu-id="5494f-109">These services include application authentication, smart card authentication, and user authentication.</span></span>

<span data-ttu-id="5494f-110">O exemplo a seguir mostra um uso típico da interface **ISCardAuth** .</span><span class="sxs-lookup"><span data-stu-id="5494f-110">The following example shows a typical use of the **ISCardAuth** interface.</span></span>

<span data-ttu-id="5494f-111">**Para usar o ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="5494f-111">**To use ISCardAuth**</span></span>

1.  <span data-ttu-id="5494f-112">Crie uma interface **ISCardAuth** (por meio do método de interface [**ISCardManage**](iscardmanage.md) correspondente).</span><span class="sxs-lookup"><span data-stu-id="5494f-112">Create an **ISCardAuth** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="5494f-113">Chame o método **ISCardAuth** apropriado ([**app \_ auth**](iscardauth-app-auth.md), [**Getchallenge**](iscardauth-getchallenge.md), [**ICC \_ auth**](iscardauth-icc-auth.md)ou [**user \_ auth**](iscardauth-user-auth.md)).</span><span class="sxs-lookup"><span data-stu-id="5494f-113">Call the appropriate **ISCardAuth** method ([**APP\_Auth**](iscardauth-app-auth.md), [**GetChallenge**](iscardauth-getchallenge.md), [**ICC\_Auth**](iscardauth-icc-auth.md), or [**User\_Auth**](iscardauth-user-auth.md)).</span></span>
3.  <span data-ttu-id="5494f-114">Libere a interface **ISCardAuth** .</span><span class="sxs-lookup"><span data-stu-id="5494f-114">Release the **ISCardAuth** interface.</span></span>

## <a name="members"></a><span data-ttu-id="5494f-115">Membros</span><span class="sxs-lookup"><span data-stu-id="5494f-115">Members</span></span>

<span data-ttu-id="5494f-116">A interface **ISCardAuth** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="5494f-116">The **ISCardAuth** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5494f-117">**ISCardAuth** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5494f-117">**ISCardAuth** also has these types of members:</span></span>

-   [<span data-ttu-id="5494f-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="5494f-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5494f-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="5494f-119">Methods</span></span>

<span data-ttu-id="5494f-120">A interface **ISCardAuth** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5494f-120">The **ISCardAuth** interface has these methods.</span></span>



| <span data-ttu-id="5494f-121">Método</span><span class="sxs-lookup"><span data-stu-id="5494f-121">Method</span></span>                                          | <span data-ttu-id="5494f-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="5494f-122">Description</span></span>                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5494f-123">**Autenticação de aplicativo \_**</span><span class="sxs-lookup"><span data-stu-id="5494f-123">**APP\_Auth**</span></span>](iscardauth-app-auth.md)        | <span data-ttu-id="5494f-124">Permite que o aplicativo se autentique usando um protocolo de desafio/assinatura.</span><span class="sxs-lookup"><span data-stu-id="5494f-124">Allows the application to authenticate itself using a challenge/signature protocol.</span></span><br/> |
| [<span data-ttu-id="5494f-125">**Getchallenge**</span><span class="sxs-lookup"><span data-stu-id="5494f-125">**GetChallenge**</span></span>](iscardauth-getchallenge.md) | <span data-ttu-id="5494f-126">Retorna um desafio do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="5494f-126">Returns a challenge from the smart card.</span></span><br/>                                            |
| [<span data-ttu-id="5494f-127">**\_Autenticação ICC**</span><span class="sxs-lookup"><span data-stu-id="5494f-127">**ICC\_Auth**</span></span>](iscardauth-icc-auth.md)        | <span data-ttu-id="5494f-128">Permite que um aplicativo autentique o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="5494f-128">Allows an application to authenticate the smart card.</span></span><br/>                               |
| [<span data-ttu-id="5494f-129">**Autenticação do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="5494f-129">**User\_Auth**</span></span>](iscardauth-user-auth.md)      | <span data-ttu-id="5494f-130">Permite o acesso aos serviços de autenticação de usuário.</span><span class="sxs-lookup"><span data-stu-id="5494f-130">Allows access to user authentication services.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="5494f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5494f-131">Requirements</span></span>



| <span data-ttu-id="5494f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5494f-132">Requirement</span></span> | <span data-ttu-id="5494f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5494f-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5494f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5494f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5494f-135">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5494f-135">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5494f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5494f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5494f-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5494f-137">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5494f-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5494f-138">End of client support</span></span><br/>    | <span data-ttu-id="5494f-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5494f-139">Windows XP</span></span><br/>                                |
| <span data-ttu-id="5494f-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="5494f-140">End of server support</span></span><br/>    | <span data-ttu-id="5494f-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5494f-141">Windows Server 2003</span></span><br/>                       |



 

 
