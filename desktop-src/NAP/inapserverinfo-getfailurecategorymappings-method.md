---
title: Método INapServerInfo GetFailureCategoryMappings (NapServerManagement. h)
description: Recupera os mapeamentos de categoria de falha para um SHA ou SHV especificado.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- Método GetFailureCategoryMappings NAP
- Método GetFailureCategoryMappings NAP, interface INapServerInfo
- INapServerInfo interface NAP, método GetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456021"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a><span data-ttu-id="3ebb3-106">Método INapServerInfo:: GetFailureCategoryMappings</span><span class="sxs-lookup"><span data-stu-id="3ebb3-106">INapServerInfo::GetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="3ebb3-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="3ebb3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3ebb3-108">O método **INapServerInfo:: GetFailureCategoryMappings** recupera os mapeamentos de categoria de falha para um Sha ou SHV especificado.</span><span class="sxs-lookup"><span data-stu-id="3ebb3-108">The **INapServerInfo::GetFailureCategoryMappings** method retrieves the failure category mappings for a specified SHA or SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ebb3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ebb3-109">Syntax</span></span>


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a><span data-ttu-id="3ebb3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ebb3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ebb3-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="3ebb3-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ebb3-112">Um [**SystemHealthEntityId**](nap-type-constants.md) que contém o identificador exclusivo do SHA ou do SHV.</span><span class="sxs-lookup"><span data-stu-id="3ebb3-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHA or the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="3ebb3-113">*mapeamento* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="3ebb3-113">*mapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ebb3-114">Um ponteiro para um [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) que contém os dados de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="3ebb3-114">A pointer to a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) that contains the mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ebb3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ebb3-115">Return value</span></span>

<span data-ttu-id="3ebb3-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="3ebb3-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3ebb3-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3ebb3-117">Return code</span></span>                                                                                     | <span data-ttu-id="3ebb3-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ebb3-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ebb3-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ebb3-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3ebb3-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3ebb3-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3ebb3-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3ebb3-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3ebb3-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="3ebb3-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3ebb3-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3ebb3-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3ebb3-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="3ebb3-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ebb3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ebb3-125">Requirements</span></span>



| <span data-ttu-id="3ebb3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ebb3-126">Requirement</span></span> | <span data-ttu-id="3ebb3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3ebb3-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ebb3-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ebb3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3ebb3-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3ebb3-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="3ebb3-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ebb3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3ebb3-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ebb3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3ebb3-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3ebb3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ebb3-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ebb3-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ebb3-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="3ebb3-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ebb3-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ebb3-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ebb3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3ebb3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ebb3-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ebb3-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="3ebb3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ebb3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ebb3-139">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="3ebb3-139">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





