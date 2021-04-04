---
description: Fornece serviços para definir o código de CHV (verificação de titular de cartão) e para verificar o usuário.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Interface ISCardVerify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662327"
---
# <a name="iscardverify-interface"></a><span data-ttu-id="f25d2-103">Interface ISCardVerify</span><span class="sxs-lookup"><span data-stu-id="f25d2-103">ISCardVerify interface</span></span>

<span data-ttu-id="f25d2-104">\[A interface **ISCardVerify** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="f25d2-104">\[The **ISCardVerify** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f25d2-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f25d2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f25d2-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="f25d2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f25d2-107">A definição de interface a seguir é fornecida como um padrão que pode ser seguido durante o desenvolvimento de um [*provedor de serviço*](../secgloss/c-gly.md)de [*cartão inteligente*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f25d2-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="f25d2-108">A interface **ISCardVerify** fornece serviços para configurar o código CHV (verificação de titular de cartão) e para verificar o usuário.</span><span class="sxs-lookup"><span data-stu-id="f25d2-108">The **ISCardVerify** interface provides services for setting CHV (card holder verification) code and for verifying the user.</span></span>

<span data-ttu-id="f25d2-109">A classe **ISCardVerify** é definida para aplicativos que implementam a política CHV específica do aplicativo e que têm um conhecimento detalhado da implementação interna do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="f25d2-109">The **ISCardVerify** class is defined for applications that implement application-specific CHV policy, and that have a detailed knowledge of the smart card's internal implementation.</span></span>

<span data-ttu-id="f25d2-110">Veja a seguir um uso típico da interface **ISCardVerify** .</span><span class="sxs-lookup"><span data-stu-id="f25d2-110">Following is a typical use of the **ISCardVerify** interface.</span></span>

<span data-ttu-id="f25d2-111">O procedimento a seguir usa **ISCardVerify** para alterar o código CHV.</span><span class="sxs-lookup"><span data-stu-id="f25d2-111">The following procedure uses **ISCardVerify** to change the CHV code.</span></span>

<span data-ttu-id="f25d2-112">**Para alterar o código CHV de um cartão inteligente**</span><span class="sxs-lookup"><span data-stu-id="f25d2-112">**To change the CHV code of a smart card**</span></span>

1.  <span data-ttu-id="f25d2-113">Crie uma interface **ISCardVerify** (por meio do método de interface [**ISCardManage**](iscardmanage.md) correspondente).</span><span class="sxs-lookup"><span data-stu-id="f25d2-113">Create an **ISCardVerify** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="f25d2-114">Chame o método [**ChangeCode**](iscardverify-changecode.md) e forneça um novo código, especificando se ele é local ou global e se está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f25d2-114">Call the [**ChangeCode**](iscardverify-changecode.md) method and provide new code, specifying if it is local or global and if it is enabled or disabled.</span></span>
3.  <span data-ttu-id="f25d2-115">Libere a interface **ISCardVerify** .</span><span class="sxs-lookup"><span data-stu-id="f25d2-115">Release the **ISCardVerify** interface.</span></span>

## <a name="members"></a><span data-ttu-id="f25d2-116">Membros</span><span class="sxs-lookup"><span data-stu-id="f25d2-116">Members</span></span>

<span data-ttu-id="f25d2-117">A interface **ISCardVerify** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="f25d2-117">The **ISCardVerify** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="f25d2-118">**ISCardVerify** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f25d2-118">**ISCardVerify** also has these types of members:</span></span>

-   [<span data-ttu-id="f25d2-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="f25d2-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f25d2-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="f25d2-120">Methods</span></span>

<span data-ttu-id="f25d2-121">A interface **ISCardVerify** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f25d2-121">The **ISCardVerify** interface has these methods.</span></span>



| <span data-ttu-id="f25d2-122">Método</span><span class="sxs-lookup"><span data-stu-id="f25d2-122">Method</span></span>                                                        | <span data-ttu-id="f25d2-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="f25d2-123">Description</span></span>                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f25d2-124">**ChangeCode**</span><span class="sxs-lookup"><span data-stu-id="f25d2-124">**ChangeCode**</span></span>](iscardverify-changecode.md)                 | <span data-ttu-id="f25d2-125">Altera o código CHV atual.</span><span class="sxs-lookup"><span data-stu-id="f25d2-125">Changes the current CHV code.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="f25d2-126">**ResetSecurityState**</span><span class="sxs-lookup"><span data-stu-id="f25d2-126">**ResetSecurityState**</span></span>](iscardverify-resetsecuritystate.md) | <span data-ttu-id="f25d2-127">Redefine o [*contexto de segurança*](../secgloss/s-gly.md) do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="f25d2-127">Resets the [*security context*](../secgloss/s-gly.md) of the smart card.</span></span><br/> |
| <span data-ttu-id="f25d2-128">[**Bloqueá**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f25d2-128">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>                       | <span data-ttu-id="f25d2-129">Habilita novamente o [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f25d2-129">Re-enables the [*security context*](../secgloss/s-gly.md).</span></span><br/>               |
| [<span data-ttu-id="f25d2-130">**Verificar**</span><span class="sxs-lookup"><span data-stu-id="f25d2-130">**Verify**</span></span>](iscardverify-verify.md)                         | <span data-ttu-id="f25d2-131">Autentica o usuário.</span><span class="sxs-lookup"><span data-stu-id="f25d2-131">Authenticates the user.</span></span><br/>                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="f25d2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f25d2-132">Requirements</span></span>



| <span data-ttu-id="f25d2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f25d2-133">Requirement</span></span> | <span data-ttu-id="f25d2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f25d2-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f25d2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f25d2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f25d2-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f25d2-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f25d2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f25d2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f25d2-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f25d2-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f25d2-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f25d2-139">End of client support</span></span><br/>    | <span data-ttu-id="f25d2-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f25d2-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="f25d2-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f25d2-141">End of server support</span></span><br/>    | <span data-ttu-id="f25d2-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f25d2-142">Windows Server 2003</span></span><br/>                       |



 

 
