---
description: Lista as interfaces em APIs de autenticação.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfaces de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170032"
---
# <a name="authentication-interfaces"></a><span data-ttu-id="a55a0-103">Interfaces de autenticação</span><span class="sxs-lookup"><span data-stu-id="a55a0-103">Authentication Interfaces</span></span>

<span data-ttu-id="a55a0-104">As interfaces de autenticação são categorizadas de acordo com o uso da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a55a0-104">Authentication interfaces are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="a55a0-105">Interfaces de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="a55a0-105">Smart Card Interfaces</span></span>](#smart-card-interfaces)
-   [<span data-ttu-id="a55a0-106">Interfaces de compartilhamento de identidade</span><span class="sxs-lookup"><span data-stu-id="a55a0-106">Identity Sharing Interfaces</span></span>](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a><span data-ttu-id="a55a0-107">Interfaces de cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="a55a0-107">Smart Card Interfaces</span></span>

<span data-ttu-id="a55a0-108">O SDK do cartão inteligente fornece as seguintes interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="a55a0-108">The Smart Card SDK provides the following COM interfaces.</span></span> <span data-ttu-id="a55a0-109">Os métodos para uma interface específica são listados no sumário e na página de referência para essa interface.</span><span class="sxs-lookup"><span data-stu-id="a55a0-109">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="a55a0-110">Interface</span><span class="sxs-lookup"><span data-stu-id="a55a0-110">Interface</span></span>                                    | <span data-ttu-id="a55a0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a55a0-111">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a55a0-112">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="a55a0-112">**IByteBuffer**</span></span>](ibytebuffer.md)           | <span data-ttu-id="a55a0-113">Gerencia um objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a55a0-113">Manages a stream object.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="a55a0-114">**Iscard**</span><span class="sxs-lookup"><span data-stu-id="a55a0-114">**ISCard**</span></span>](iscard.md)                     | <span data-ttu-id="a55a0-115">Abre e gerencia uma conexão com um [*cartão inteligente*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="a55a0-115">Opens and manages a connection to a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span>                                                                    |
| [<span data-ttu-id="a55a0-116">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="a55a0-116">**ISCardAuth**</span></span>](iscardauth.md)             | <span data-ttu-id="a55a0-117">Autentica um aplicativo, um cartão inteligente ou um usuário.</span><span class="sxs-lookup"><span data-stu-id="a55a0-117">Authenticates an application, smart card, or user.</span></span>                                                                                                                                       |
| [<span data-ttu-id="a55a0-118">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="a55a0-118">**ISCardCmd**</span></span>](iscardcmd.md)               | <span data-ttu-id="a55a0-119">Constrói e gerencia uma APDU ( [*unidade de dados do protocolo de aplicativo*](/windows/desktop/SecGloss/a-gly) de cartão inteligente).</span><span class="sxs-lookup"><span data-stu-id="a55a0-119">Constructs and manages a smart card [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) (APDU).</span></span> |
| [<span data-ttu-id="a55a0-120">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="a55a0-120">**ISCardDatabase**</span></span>](iscarddatabase.md)     | <span data-ttu-id="a55a0-121">Executa operações de banco de dados do [*Gerenciador de recursos*](/windows/desktop/SecGloss/r-gly) de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="a55a0-121">Performs smart card [*resource manager*](/windows/desktop/SecGloss/r-gly) database operations.</span></span>                                              |
| [<span data-ttu-id="a55a0-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="a55a0-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md) | <span data-ttu-id="a55a0-123">Executa serviços de arquivos comuns, como localizar, selecionar, ler, gravar, criar e excluir arquivos.</span><span class="sxs-lookup"><span data-stu-id="a55a0-123">Performs common file services such as locating, selecting, reading, writing, creating, and deleting files.</span></span>                                                                               |
| [<span data-ttu-id="a55a0-124">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a55a0-124">**ISCardISO7816**</span></span>](iscardiso7816.md)       | <span data-ttu-id="a55a0-125">Constrói um comando APDU.</span><span class="sxs-lookup"><span data-stu-id="a55a0-125">Constructs an APDU command.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="a55a0-126">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="a55a0-126">**ISCardLocate**</span></span>](iscardlocate.md)         | <span data-ttu-id="a55a0-127">Localiza um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="a55a0-127">Locates a smart card.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="a55a0-128">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="a55a0-128">**ISCardManage**</span></span>](iscardmanage.md)         | <span data-ttu-id="a55a0-129">Gerencia o sistema de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="a55a0-129">Manages the smart card system.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="a55a0-130">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="a55a0-130">**ISCardTypeConv**</span></span>](iscardtypeconv.md)     | <span data-ttu-id="a55a0-131">Fornece métodos usados para dar suporte a outras interfaces COM de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="a55a0-131">Provides methods used to support other smart card COM interfaces.</span></span> <span data-ttu-id="a55a0-132">Essa interface é fornecida apenas para fins de compatibilidade com versões anteriores e não deve mais ser usada.</span><span class="sxs-lookup"><span data-stu-id="a55a0-132">This interface is provided for backward compatibility only and should no longer be used.</span></span>                               |
| [<span data-ttu-id="a55a0-133">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="a55a0-133">**ISCardVerify**</span></span>](iscardverify.md)         | <span data-ttu-id="a55a0-134">Verifica ou altera a política de verificação do titular do cartão (CHV).</span><span class="sxs-lookup"><span data-stu-id="a55a0-134">Verifies or changes card holder verification (CHV) policy.</span></span>                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a><span data-ttu-id="a55a0-135">Interfaces de compartilhamento de identidade</span><span class="sxs-lookup"><span data-stu-id="a55a0-135">Identity Sharing Interfaces</span></span>

<span data-ttu-id="a55a0-136">O SDK de compartilhamento de identidade fornece as seguintes interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="a55a0-136">The Identity Sharing SDK provides the following COM interfaces.</span></span> <span data-ttu-id="a55a0-137">Os métodos para uma interface específica são listados no sumário e na página de referência para essa interface.</span><span class="sxs-lookup"><span data-stu-id="a55a0-137">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="a55a0-138">Interface</span><span class="sxs-lookup"><span data-stu-id="a55a0-138">Interface</span></span>                                                          | <span data-ttu-id="a55a0-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="a55a0-139">Description</span></span>                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a55a0-140">**IAssociatedIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="a55a0-140">**IAssociatedIdentityProvider**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | <span data-ttu-id="a55a0-141">Permite que um provedor de identidade associe identidades a contas de usuário locais.</span><span class="sxs-lookup"><span data-stu-id="a55a0-141">Allows an identity provider to associate identities with local user accounts.</span></span>            |
| [<span data-ttu-id="a55a0-142">**IIdentityAdvise**</span><span class="sxs-lookup"><span data-stu-id="a55a0-142">**IIdentityAdvise**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | <span data-ttu-id="a55a0-143">Permite que um provedor de identidade Notifique um aplicativo de chamada quando uma identidade for atualizada.</span><span class="sxs-lookup"><span data-stu-id="a55a0-143">Allows an identity provider to notify a calling application when an identity is updated.</span></span> |
| [<span data-ttu-id="a55a0-144">**IIdentityprovider**</span><span class="sxs-lookup"><span data-stu-id="a55a0-144">**IIdentityProvider**</span></span>](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | <span data-ttu-id="a55a0-145">Representa um provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="a55a0-145">Represents an identity provider.</span></span>                                                         |
| [<span data-ttu-id="a55a0-146">**IIdentityStore**</span><span class="sxs-lookup"><span data-stu-id="a55a0-146">**IIdentityStore**</span></span>](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | <span data-ttu-id="a55a0-147">Fornece métodos para enumerar e gerenciar identidades e provedores de identidade.</span><span class="sxs-lookup"><span data-stu-id="a55a0-147">Provides methods to enumerate and manage identities and identity providers.</span></span>              |



 

 

 
