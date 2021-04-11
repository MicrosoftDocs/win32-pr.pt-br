---
title: Interface INapCertRelyingParty (NapCertRelyingParty. h)
description: As partes confiáveis do certificado devem usar o para se comunicar com o NapAgent.
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- INapCertRelyingParty da interface NAP
- INapCertRelyingParty interface NAP, descrita
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009539"
---
# <a name="inapcertrelyingparty-interface"></a><span data-ttu-id="292bb-105">Interface INapCertRelyingParty</span><span class="sxs-lookup"><span data-stu-id="292bb-105">INapCertRelyingParty interface</span></span>

> [!Note]  
> <span data-ttu-id="292bb-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="292bb-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="292bb-107">A interface **INapCertRelyingParty** fornece métodos que as partes confiáveis de certificado devem usar para se comunicar com o NapAgent.</span><span class="sxs-lookup"><span data-stu-id="292bb-107">The **INapCertRelyingParty** interface provides methods that certificate-relying parties must use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="292bb-108">Membros</span><span class="sxs-lookup"><span data-stu-id="292bb-108">Members</span></span>

<span data-ttu-id="292bb-109">A interface **INapCertRelyingParty** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="292bb-109">The **INapCertRelyingParty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="292bb-110">**INapCertRelyingParty** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="292bb-110">**INapCertRelyingParty** also has these types of members:</span></span>

-   [<span data-ttu-id="292bb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="292bb-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="292bb-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="292bb-112">Methods</span></span>

<span data-ttu-id="292bb-113">A interface **INapCertRelyingParty** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="292bb-113">The **INapCertRelyingParty** interface has these methods.</span></span>



| <span data-ttu-id="292bb-114">Método</span><span class="sxs-lookup"><span data-stu-id="292bb-114">Method</span></span>                                                                                                        | <span data-ttu-id="292bb-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="292bb-115">Description</span></span>                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="292bb-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span><span class="sxs-lookup"><span data-stu-id="292bb-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span></span>](inapcertrelyingparty-getsubscribedrelyingparties.md) | <span data-ttu-id="292bb-117">Obtém uma lista de terceiras partes confiáveis que se inscreveram.</span><span class="sxs-lookup"><span data-stu-id="292bb-117">Gets a list of relying parties that have subscribed.</span></span><br/>                 |
| [<span data-ttu-id="292bb-118">**INapCertRelyingParty::SubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="292bb-118">**INapCertRelyingParty::SubscribeCertByGroup**</span></span>](inapcertrelyingparty-subscribecertbygroup.md)               | <span data-ttu-id="292bb-119">Assina um servidor de certificado de integridade já registrado (HCS).</span><span class="sxs-lookup"><span data-stu-id="292bb-119">Subscribes to an already-registered health certificate server (HCS).</span></span><br/> |
| [<span data-ttu-id="292bb-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="292bb-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span></span>](inapcertrelyingparty-unsubscribecertbygroup.md)           | <span data-ttu-id="292bb-121">Cancela a assinatura de um servidor HCS.</span><span class="sxs-lookup"><span data-stu-id="292bb-121">Unsubscribes from an HCS server.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="292bb-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="292bb-122">Requirements</span></span>



| <span data-ttu-id="292bb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="292bb-123">Requirement</span></span> | <span data-ttu-id="292bb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="292bb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="292bb-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="292bb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="292bb-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="292bb-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="292bb-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="292bb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="292bb-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="292bb-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="292bb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="292bb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="292bb-130"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="292bb-130"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="292bb-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="292bb-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="292bb-132"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="292bb-132"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="292bb-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="292bb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292bb-134">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="292bb-134">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="292bb-135">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="292bb-135">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

