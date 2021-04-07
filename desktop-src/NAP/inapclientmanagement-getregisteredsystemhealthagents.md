---
title: Método INapClientManagement GetRegisteredSystemHealthAgents (NapManagement. h)
description: Recupera informações sobre os SHAs registrados.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Método GetRegisteredSystemHealthAgents NAP
- Método GetRegisteredSystemHealthAgents NAP, interface INapClientManagement
- INapClientManagement interface NAP, método GetRegisteredSystemHealthAgents
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918751"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a><span data-ttu-id="0d743-106">Método INapClientManagement:: GetRegisteredSystemHealthAgents</span><span class="sxs-lookup"><span data-stu-id="0d743-106">INapClientManagement::GetRegisteredSystemHealthAgents method</span></span>

> [!Note]  
> <span data-ttu-id="0d743-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="0d743-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0d743-108">O método **GetRegisteredSystemHealthAgents** recupera informações sobre os SHAs registrados.</span><span class="sxs-lookup"><span data-stu-id="0d743-108">The **GetRegisteredSystemHealthAgents** method retrieves information about the registered SHAs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d743-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d743-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a><span data-ttu-id="0d743-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d743-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d743-111">*contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="0d743-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d743-112">Um ponteiro para um [**SystemHealthEntityCount**](nap-datatypes.md) que descreve o número de SHAs registrados.</span><span class="sxs-lookup"><span data-stu-id="0d743-112">A pointer to a [**SystemHealthEntityCount**](nap-datatypes.md) that describes the number of registered SHAs.</span></span>

</dd> <dt>

<span data-ttu-id="0d743-113">*agentes* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0d743-113">*agents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d743-114">Um ponteiro para uma matriz de estruturas [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que descrevem os SHAs registrados.</span><span class="sxs-lookup"><span data-stu-id="0d743-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered SHAs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d743-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d743-115">Return value</span></span>

<span data-ttu-id="0d743-116">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d743-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="0d743-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0d743-117">Return code</span></span>                                                                                         | <span data-ttu-id="0d743-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d743-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d743-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d743-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="0d743-120">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="0d743-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0d743-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0d743-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="0d743-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="0d743-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0d743-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d743-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="0d743-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="0d743-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0d743-125"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="0d743-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0d743-126">O NapAgent não está em execução.</span><span class="sxs-lookup"><span data-stu-id="0d743-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="0d743-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d743-127">Requirements</span></span>



| <span data-ttu-id="0d743-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d743-128">Requirement</span></span> | <span data-ttu-id="0d743-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0d743-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d743-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d743-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0d743-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d743-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0d743-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d743-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0d743-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d743-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0d743-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d743-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d743-135"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d743-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d743-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="0d743-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d743-137"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d743-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d743-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0d743-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d743-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d743-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="0d743-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d743-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d743-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="0d743-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





