---
title: Método INapClientManagement GetRegisteredEnforcementClients (NapManagement. h)
description: Recupera informações sobre os clientes de imposição registrados.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Método GetRegisteredEnforcementClients NAP
- Método GetRegisteredEnforcementClients NAP, interface INapClientManagement
- INapClientManagement interface NAP, método GetRegisteredEnforcementClients
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455514"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a><span data-ttu-id="8cd62-106">Método INapClientManagement:: GetRegisteredEnforcementClients</span><span class="sxs-lookup"><span data-stu-id="8cd62-106">INapClientManagement::GetRegisteredEnforcementClients method</span></span>

> [!Note]  
> <span data-ttu-id="8cd62-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="8cd62-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8cd62-108">O método **GetRegisteredEnforcementClients** recupera informações sobre os clientes de imposição registrados.</span><span class="sxs-lookup"><span data-stu-id="8cd62-108">The **GetRegisteredEnforcementClients** method retrieves information about the registered enforcement clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd62-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cd62-109">Syntax</span></span>


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a><span data-ttu-id="8cd62-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cd62-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cd62-111">*contagem* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="8cd62-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd62-112">Um ponteiro para um [**EnforcementEntityCount**](nap-datatypes.md) que contém o número de clientes de imposição registrados.</span><span class="sxs-lookup"><span data-stu-id="8cd62-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of registered enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="8cd62-113">*executores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cd62-113">*enforcers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cd62-114">Um ponteiro para uma matriz de estruturas [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que descrevem os clientes de imposição registrados.</span><span class="sxs-lookup"><span data-stu-id="8cd62-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered enforcement clients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cd62-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cd62-115">Return value</span></span>

<span data-ttu-id="8cd62-116">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="8cd62-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="8cd62-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8cd62-117">Return code</span></span>                                                                                         | <span data-ttu-id="8cd62-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="8cd62-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8cd62-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8cd62-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="8cd62-120">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="8cd62-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8cd62-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8cd62-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="8cd62-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="8cd62-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8cd62-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8cd62-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="8cd62-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8cd62-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8cd62-125"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="8cd62-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8cd62-126">O NapAgent não está em execução.</span><span class="sxs-lookup"><span data-stu-id="8cd62-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="8cd62-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cd62-127">Requirements</span></span>



| <span data-ttu-id="8cd62-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cd62-128">Requirement</span></span> | <span data-ttu-id="8cd62-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8cd62-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd62-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cd62-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd62-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cd62-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8cd62-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cd62-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd62-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8cd62-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8cd62-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cd62-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cd62-135"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cd62-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="8cd62-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="8cd62-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8cd62-137"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8cd62-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="8cd62-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8cd62-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cd62-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cd62-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="8cd62-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cd62-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd62-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="8cd62-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





