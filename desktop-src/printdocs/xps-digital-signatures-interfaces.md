---
description: Interfaces de API de assinatura digital XPS
ms.assetid: 44244035-f7d5-47f1-b4d8-b895562be855
title: Interfaces de API de assinatura digital XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fc532ed90cb41e4d0cb524daba87f72edefd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800114"
---
# <a name="xps-digital-signature-api-interfaces"></a><span data-ttu-id="56878-103">Interfaces de API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="56878-103">XPS Digital Signature API Interfaces</span></span>

## <a name="contents"></a><span data-ttu-id="56878-104">Sumário</span><span class="sxs-lookup"><span data-stu-id="56878-104">Contents</span></span>

## <a name="in-this-section"></a><span data-ttu-id="56878-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="56878-105">In this section</span></span>



| <span data-ttu-id="56878-106">Interface</span><span class="sxs-lookup"><span data-stu-id="56878-106">Interface</span></span>                                                                           | <span data-ttu-id="56878-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="56878-107">Description</span></span>                                                                                         |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56878-108">**IXpsSignature**</span><span class="sxs-lookup"><span data-stu-id="56878-108">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)<br/>                                   | <span data-ttu-id="56878-109">Representa uma única assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="56878-109">Represents a single digital signature.</span></span><br/>                                                   |
| [<span data-ttu-id="56878-110">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="56878-110">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)<br/>                         | <span data-ttu-id="56878-111">Representa um bloco de solicitações de assinatura que são armazenadas em uma parte SignatureDefinitions.</span><span class="sxs-lookup"><span data-stu-id="56878-111">Represents a block of signature requests that are stored in a SignatureDefinitions part.</span></span><br/> |
| [<span data-ttu-id="56878-112">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="56878-112">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)<br/>     | <span data-ttu-id="56878-113">Uma coleção de interfaces [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) .</span><span class="sxs-lookup"><span data-stu-id="56878-113">A collection of [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) interfaces.</span></span><br/>             |
| [<span data-ttu-id="56878-114">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="56878-114">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)<br/>               | <span data-ttu-id="56878-115">Uma coleção de ponteiros de interface [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) .</span><span class="sxs-lookup"><span data-stu-id="56878-115">A collection of [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) interface pointers.</span></span><br/>               |
| [<span data-ttu-id="56878-116">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="56878-116">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)<br/>                     | <span data-ttu-id="56878-117">Gerencia as assinaturas digitais e as solicitações de assinatura digital de um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="56878-117">Manages the digital signatures and digital signature requests of an XPS document.</span></span><br/>        |
| [<span data-ttu-id="56878-118">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="56878-118">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)<br/>                     | <span data-ttu-id="56878-119">Acessa os componentes de uma solicitação de assinatura.</span><span class="sxs-lookup"><span data-stu-id="56878-119">Accesses the components of a signature request.</span></span><br/>                                          |
| [<span data-ttu-id="56878-120">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="56878-120">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)<br/> | <span data-ttu-id="56878-121">Uma coleção de interfaces [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) .</span><span class="sxs-lookup"><span data-stu-id="56878-121">A collection of [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) interfaces.</span></span><br/>         |
| [<span data-ttu-id="56878-122">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="56878-122">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)<br/>                         | <span data-ttu-id="56878-123">Fornece acesso às opções de assinatura individuais que são usadas por novas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="56878-123">Provides access to the individual signing options that are used by new signatures.</span></span><br/>       |



 

 

 




