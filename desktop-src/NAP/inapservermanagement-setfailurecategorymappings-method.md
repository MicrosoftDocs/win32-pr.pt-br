---
title: Método INapServerManagement SetFailureCategoryMappings (NapServerManagement. h)
description: É usado para definir os mapeamentos de categoria de falha do SHV.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- Método SetFailureCategoryMappings NAP
- Método SetFailureCategoryMappings NAP, interface INapServerManagement
- INapServerManagement interface NAP, método SetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918749"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a><span data-ttu-id="2b885-106">Método INapServerManagement:: SetFailureCategoryMappings</span><span class="sxs-lookup"><span data-stu-id="2b885-106">INapServerManagement::SetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="2b885-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="2b885-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2b885-108">O método **INapServerManagement:: SetFailureCategoryMappings** é usado para definir os mapeamentos de categoria de falha do SHV.</span><span class="sxs-lookup"><span data-stu-id="2b885-108">The **INapServerManagement::SetFailureCategoryMappings** method is used to set the SHV's failure category mappings.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b885-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b885-109">Syntax</span></span>


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a><span data-ttu-id="2b885-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b885-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b885-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2b885-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b885-112">Um [**SystemHealthEntityId**](nap-type-constants.md) que contém o identificador exclusivo do SHV.</span><span class="sxs-lookup"><span data-stu-id="2b885-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="2b885-113">*mapeamento* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="2b885-113">*mapping* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b885-114">Uma estrutura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) que contém os dados de mapeamento da categoria de falha.</span><span class="sxs-lookup"><span data-stu-id="2b885-114">A [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure that contains the failure category mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b885-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b885-115">Return value</span></span>

<span data-ttu-id="2b885-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="2b885-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2b885-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2b885-117">Return code</span></span>                                                                                     | <span data-ttu-id="2b885-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b885-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b885-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b885-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="2b885-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2b885-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2b885-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2b885-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="2b885-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2b885-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2b885-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2b885-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="2b885-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="2b885-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b885-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b885-125">Requirements</span></span>



| <span data-ttu-id="2b885-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b885-126">Requirement</span></span> | <span data-ttu-id="2b885-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2b885-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b885-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b885-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2b885-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2b885-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="2b885-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b885-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2b885-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b885-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2b885-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b885-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b885-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b885-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b885-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="2b885-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b885-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b885-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="2b885-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2b885-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b885-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b885-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="2b885-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b885-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b885-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="2b885-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





