---
description: Uma interface implementada pelo cliente que permite aos desenvolvedores fornecer suas próprias credenciais dinamicamente em tempo de execução para autenticar contêineres não ingressados no domínio com o Active Directory.
title: Interface ICcgDomainAuthCredentials (ccgplugins.h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387787"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="1e749-103">Interface ICcgDomainAuthCredentials</span><span class="sxs-lookup"><span data-stu-id="1e749-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="1e749-104">Uma interface implementada pelo cliente que permite aos desenvolvedores fornecer suas próprias credenciais dinamicamente em tempo de execução para autenticar contêineres não ingressados no domínio com o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1e749-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="1e749-105">Membros</span><span class="sxs-lookup"><span data-stu-id="1e749-105">Members</span></span>

<span data-ttu-id="1e749-106">A interface **ICcgDomainAuthCredentials** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="1e749-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1e749-107">**ICcgDomainAuthCredentials** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1e749-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="1e749-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e749-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1e749-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e749-109">Methods</span></span>

<span data-ttu-id="1e749-110">A interface **ICcgDomainAuthCredentials** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1e749-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="1e749-111">Método</span><span class="sxs-lookup"><span data-stu-id="1e749-111">Method</span></span>                                           | <span data-ttu-id="1e749-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e749-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e749-113">**GetPasswordCredentials**</span><span class="sxs-lookup"><span data-stu-id="1e749-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="1e749-114">Retorna credenciais para autenticar um contêiner não ingressado no domínio com o Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1e749-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="1e749-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e749-115">Requirements</span></span>



| <span data-ttu-id="1e749-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e749-116">Requirement</span></span> | <span data-ttu-id="1e749-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1e749-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e749-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e749-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e749-119">Somente \[ aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1e749-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1e749-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e749-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e749-121">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e749-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e749-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1e749-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e749-123"><dt>ccgplugins.h</dt></span><span class="sxs-lookup"><span data-stu-id="1e749-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e749-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1e749-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e749-125"><dt>ccgplugins.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1e749-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1e749-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1e749-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e749-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e749-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e749-128">IID</span><span class="sxs-lookup"><span data-stu-id="1e749-128">IID</span></span><br/>                      | <span data-ttu-id="1e749-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="1e749-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 

