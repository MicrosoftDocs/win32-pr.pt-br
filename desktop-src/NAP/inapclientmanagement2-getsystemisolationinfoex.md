---
title: Método INapClientManagement2 GetSystemIsolationInfoEx (NapManagement. h)
description: Recupera informações sobre o estado de isolamento e o estado de isolamento estendido do NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Método GetSystemIsolationInfoEx NAP
- Método GetSystemIsolationInfoEx NAP, interface INapClientManagement2
- INapClientManagement2 interface NAP, método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009166"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a><span data-ttu-id="2a2bf-106">Método INapClientManagement2:: GetSystemIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="2a2bf-106">INapClientManagement2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="2a2bf-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="2a2bf-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2a2bf-108">O método **GetSystemIsolationInfoEx** recupera informações sobre o estado de isolamento e o estado de isolamento estendido do NapClient.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-108">The **GetSystemIsolationInfoEx** method retrieves information about the isolation state and extended isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a2bf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2a2bf-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="2a2bf-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a2bf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a2bf-111">*isolationInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2a2bf-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a2bf-112">Um ponteiro para um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém informações de estado de isolamento.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="2a2bf-113">*unknownConnections* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2a2bf-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a2bf-114">Um ponteiro para um BOOL que será **verdadeiro** se qualquer uma das conexões estiver em um estado desconhecido e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-114">A pointer to a BOOL that is **TRUE** if any of the connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a2bf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a2bf-115">Return value</span></span>

<span data-ttu-id="2a2bf-116">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="2a2bf-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2a2bf-117">Return code</span></span>                                                                                         | <span data-ttu-id="2a2bf-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a2bf-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a2bf-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a2bf-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="2a2bf-120">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2a2bf-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2a2bf-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="2a2bf-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2a2bf-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2a2bf-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="2a2bf-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2a2bf-125"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="2a2bf-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="2a2bf-126">O NapAgent não está em execução.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="2a2bf-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a2bf-127">Remarks</span></span>

<span data-ttu-id="2a2bf-128">As informações de isolamento que são recuperadas não refletem Estados desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="2a2bf-128">The isolation information that is retrieved does not reflect unknown states.</span></span>

<span data-ttu-id="2a2bf-129">O SHA deve liberar a estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="2a2bf-129">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a2bf-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a2bf-130">Requirements</span></span>



| <span data-ttu-id="2a2bf-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a2bf-131">Requirement</span></span> | <span data-ttu-id="2a2bf-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2a2bf-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a2bf-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a2bf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2a2bf-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a2bf-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2a2bf-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a2bf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2a2bf-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a2bf-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2a2bf-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a2bf-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a2bf-138"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a2bf-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a2bf-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="2a2bf-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a2bf-140"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a2bf-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="2a2bf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2a2bf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a2bf-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a2bf-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="2a2bf-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a2bf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a2bf-144">**INapClientManagement2**</span><span class="sxs-lookup"><span data-stu-id="2a2bf-144">**INapClientManagement2**</span></span>](inapclientmanagement2.md)
</dt> </dl>

 

 





