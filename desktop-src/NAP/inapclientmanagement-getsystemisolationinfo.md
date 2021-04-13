---
title: Método INapClientManagement GetSystemIsolationInfo (NapManagement. h)
description: Recupera informações sobre o estado de isolamento do NapClient.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Método GetSystemIsolationInfo NAP
- Método GetSystemIsolationInfo NAP, interface INapClientManagement
- INapClientManagement interface NAP, método GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369795"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a><span data-ttu-id="c841b-106">Método INapClientManagement:: GetSystemIsolationInfo</span><span class="sxs-lookup"><span data-stu-id="c841b-106">INapClientManagement::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="c841b-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="c841b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c841b-108">O método **GetSystemIsolationInfo** recupera informações sobre o estado de isolamento do NapClient.</span><span class="sxs-lookup"><span data-stu-id="c841b-108">The **GetSystemIsolationInfo** method retrieves information about the isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="c841b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c841b-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="c841b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c841b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c841b-111">*isolationInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c841b-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c841b-112">Um ponteiro para um ponteiro para uma estrutura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contém informações de estado de isolamento.</span><span class="sxs-lookup"><span data-stu-id="c841b-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="c841b-113">*unknownConnections* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c841b-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c841b-114">Um ponteiro para um sinalizador que indica se alguma das conexões está em um estado desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c841b-114">A pointer to a flag that indicates whether any of the connections are in an unknown state.</span></span> <span data-ttu-id="c841b-115">Se qualquer um deles for, o sinalizador será definido como **true**; caso contrário, o sinalizador será definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="c841b-115">If any of them are, the flag is set to **TRUE**; otherwise the flag is set to **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c841b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c841b-116">Return value</span></span>

<span data-ttu-id="c841b-117">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="c841b-117">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="c841b-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c841b-118">Return code</span></span>                                                                                         | <span data-ttu-id="c841b-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="c841b-119">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c841b-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c841b-120"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="c841b-121">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="c841b-121">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c841b-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c841b-122"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="c841b-123">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c841b-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c841b-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c841b-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="c841b-125">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="c841b-125">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c841b-126"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="c841b-126"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c841b-127">O NapAgent não está em execução.</span><span class="sxs-lookup"><span data-stu-id="c841b-127">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c841b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c841b-128">Remarks</span></span>

<span data-ttu-id="c841b-129">As informações de isolamento que são recuperadas não refletem Estados desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="c841b-129">The isolation information that is retrieved does not reflect unknown states.</span></span>

## <a name="requirements"></a><span data-ttu-id="c841b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c841b-130">Requirements</span></span>



| <span data-ttu-id="c841b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c841b-131">Requirement</span></span> | <span data-ttu-id="c841b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c841b-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c841b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c841b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c841b-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c841b-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c841b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c841b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c841b-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c841b-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c841b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c841b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c841b-138"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="c841b-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="c841b-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="c841b-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c841b-140"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c841b-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="c841b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c841b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c841b-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c841b-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="c841b-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c841b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c841b-144">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="c841b-144">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





