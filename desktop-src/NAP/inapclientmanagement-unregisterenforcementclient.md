---
title: Método INapClientManagement UnregisterEnforcementClient (NapManagement. h)
description: Cancela o registro de um cliente de imposição com o sistema NAP.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Método UnregisterEnforcementClient NAP
- Método UnregisterEnforcementClient NAP, interface INapClientManagement
- INapClientManagement interface NAP, método UnregisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085893"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a><span data-ttu-id="a758b-106">Método INapClientManagement:: UnregisterEnforcementClient</span><span class="sxs-lookup"><span data-stu-id="a758b-106">INapClientManagement::UnregisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="a758b-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="a758b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a758b-108">O método **UnregisterEnforcementClient** cancela o registro de um cliente de imposição com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="a758b-108">The **UnregisterEnforcementClient** method unregisters an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a758b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a758b-109">Syntax</span></span>


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="a758b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a758b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a758b-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="a758b-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a758b-112">Um valor [**EnforcementEntityId**](nap-datatypes.md) que identifica o cliente de imposição para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="a758b-112">An [**EnforcementEntityId**](nap-datatypes.md) value that identifies the enforcement client to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a758b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a758b-113">Return value</span></span>

<span data-ttu-id="a758b-114">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="a758b-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="a758b-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a758b-115">Return code</span></span>                                                                                         | <span data-ttu-id="a758b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a758b-116">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a758b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a758b-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="a758b-118">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="a758b-118">Operation successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="a758b-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a758b-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="a758b-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="a758b-120">Permissions error, access denied.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a758b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a758b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="a758b-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a758b-122">System resource limit, could not perform the operation.</span></span><br/>             |
| <dl> <span data-ttu-id="a758b-123"><dt>**NAP \_ E \_ ainda \_ associado**</dt></span><span class="sxs-lookup"><span data-stu-id="a758b-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="a758b-124">Não foi possível cancelar o registro do cliente de imposição e permanecer associado.</span><span class="sxs-lookup"><span data-stu-id="a758b-124">The enforcement client could not be unregistered and remains bound.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a758b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a758b-125">Requirements</span></span>



| <span data-ttu-id="a758b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a758b-126">Requirement</span></span> | <span data-ttu-id="a758b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a758b-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a758b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a758b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a758b-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a758b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a758b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a758b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a758b-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a758b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a758b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a758b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a758b-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="a758b-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="a758b-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="a758b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a758b-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a758b-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="a758b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a758b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a758b-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a758b-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="a758b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a758b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a758b-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="a758b-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





