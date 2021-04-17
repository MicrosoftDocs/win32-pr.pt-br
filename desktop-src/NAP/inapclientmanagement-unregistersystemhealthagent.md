---
title: Método INapClientManagement UnregisterSystemHealthAgent (NapManagement. h)
description: Cancela o registro de um SHA com o sistema NAP.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- Método UnregisterSystemHealthAgent NAP
- Método UnregisterSystemHealthAgent NAP, interface INapClientManagement
- INapClientManagement interface NAP, método UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789753"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a><span data-ttu-id="5d868-106">Método INapClientManagement:: UnregisterSystemHealthAgent</span><span class="sxs-lookup"><span data-stu-id="5d868-106">INapClientManagement::UnregisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="5d868-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="5d868-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5d868-108">O método **UnregisterSystemHealthAgent** cancela o registro de um Sha com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="5d868-108">The **UnregisterSystemHealthAgent** method unregisters an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d868-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d868-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="5d868-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d868-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d868-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="5d868-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d868-112">Um [**SystemHealthEntityId**](nap-datatypes.md) que identifica o cancelamento do registro do agente de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="5d868-112">A [**SystemHealthEntityId**](nap-datatypes.md) that identifies the System Health Agent to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d868-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d868-113">Return value</span></span>

<span data-ttu-id="5d868-114">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d868-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="5d868-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5d868-115">Return code</span></span>                                                                                         | <span data-ttu-id="5d868-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d868-116">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d868-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5d868-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="5d868-118">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="5d868-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5d868-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5d868-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="5d868-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="5d868-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5d868-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5d868-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="5d868-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="5d868-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5d868-123"><dt>**NAP \_ E \_ ainda \_ associado**</dt></span><span class="sxs-lookup"><span data-stu-id="5d868-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="5d868-124">O SHA permanece associado e não teve seu registro cancelado.</span><span class="sxs-lookup"><span data-stu-id="5d868-124">The SHA remains bound and could not be unregistered.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="5d868-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d868-125">Requirements</span></span>



| <span data-ttu-id="5d868-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d868-126">Requirement</span></span> | <span data-ttu-id="5d868-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5d868-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d868-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d868-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5d868-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d868-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5d868-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d868-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5d868-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d868-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5d868-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d868-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d868-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d868-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d868-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="5d868-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d868-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d868-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="5d868-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5d868-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d868-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d868-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="5d868-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d868-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d868-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="5d868-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





