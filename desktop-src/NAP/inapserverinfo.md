---
title: Interface INapServerInfo (NapServerManagement. h)
description: Os clientes de gerenciamento (por exemplo, provedores WMI ou ferramentas de linha de comando) usam para consultar o status do sistema de servidor NAP.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- INapServerInfo da interface NAP
- INapServerInfo interface NAP, descrita
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760692"
---
# <a name="inapserverinfo-interface"></a><span data-ttu-id="d5980-105">Interface INapServerInfo</span><span class="sxs-lookup"><span data-stu-id="d5980-105">INapServerInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="d5980-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="d5980-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d5980-107">O **INapServerInfo** fornece métodos que os clientes de gerenciamento (por exemplo, provedores WMI ou ferramentas de linha de comando) usam para consultar o status do sistema de servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="d5980-107">The **INapServerInfo** provides methods that Management clients (for example, WMI providers or command-line tools) use to query the status of the NAP server system.</span></span>

## <a name="members"></a><span data-ttu-id="d5980-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d5980-108">Members</span></span>

<span data-ttu-id="d5980-109">A interface **INapServerInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d5980-109">The **INapServerInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5980-110">**INapServerInfo** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d5980-110">**INapServerInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="d5980-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d5980-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5980-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d5980-112">Methods</span></span>

<span data-ttu-id="d5980-113">A interface **INapServerInfo** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d5980-113">The **INapServerInfo** interface has these methods.</span></span>



| <span data-ttu-id="d5980-114">Método</span><span class="sxs-lookup"><span data-stu-id="d5980-114">Method</span></span>                                                                                                                   | <span data-ttu-id="d5980-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5980-115">Description</span></span>                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="d5980-116">**INapServerInfo::GetFailureCategoryMappings**</span><span class="sxs-lookup"><span data-stu-id="d5980-116">**INapServerInfo::GetFailureCategoryMappings**</span></span>](inapserverinfo-getfailurecategorymappings-method.md)                   | <span data-ttu-id="d5980-117">Recupera os mapeamentos de categoria de falha para um SHV especificado.</span><span class="sxs-lookup"><span data-stu-id="d5980-117">Retrieves the failure category mappings for a specified SHV.</span></span><br/> |
| [<span data-ttu-id="d5980-118">**INapServerInfo::GetNapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="d5980-118">**INapServerInfo::GetNapServerInfo**</span></span>](inapserverinfo-getnapserverinfo-method.md)                                       | <span data-ttu-id="d5980-119">Recupera informações sobre o servidor NAP.</span><span class="sxs-lookup"><span data-stu-id="d5980-119">Retrieves information about the NAP server.</span></span><br/>                  |
| [<span data-ttu-id="d5980-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span><span class="sxs-lookup"><span data-stu-id="d5980-120">**INapServerInfo::GetRegisteredSystemHealthValidators**</span></span>](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | <span data-ttu-id="d5980-121">Recupera uma lista de SHVs registrados.</span><span class="sxs-lookup"><span data-stu-id="d5980-121">Retrieves a list of registered SHVs.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="d5980-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5980-122">Remarks</span></span>

<span data-ttu-id="d5980-123">Esses métodos fornecem apenas informações estáticas sobre o servidor NAP e seus componentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="d5980-123">These methods provide only static information about the NAP Server and its components on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5980-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5980-124">Requirements</span></span>



| <span data-ttu-id="d5980-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5980-125">Requirement</span></span> | <span data-ttu-id="d5980-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d5980-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5980-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5980-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d5980-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d5980-128">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="d5980-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5980-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d5980-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5980-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d5980-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5980-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5980-132"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5980-132"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5980-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="d5980-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5980-134"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5980-134"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="d5980-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d5980-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5980-136"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5980-136"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="d5980-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5980-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5980-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="d5980-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="d5980-139">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="d5980-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

