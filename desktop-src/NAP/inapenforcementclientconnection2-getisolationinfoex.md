---
title: Método INapEnforcementClientConnection2 GetIsolationInfoEx (NapEnforcementClient. h)
description: É usado para obter informações de isolamento sobre o cliente.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Método GetIsolationInfoEx NAP
- Método GetIsolationInfoEx NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, método GetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456023"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a><span data-ttu-id="a6ccb-106">Método INapEnforcementClientConnection2:: GetIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="a6ccb-106">INapEnforcementClientConnection2::GetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="a6ccb-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="a6ccb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a6ccb-108">O método **INapEnforcementClientConnection2:: GetIsolationInfoEx** é usado para obter informações de isolamento sobre o cliente.</span><span class="sxs-lookup"><span data-stu-id="a6ccb-108">The **INapEnforcementClientConnection2::GetIsolationInfoEx** method is used to get isolation information about the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ccb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6ccb-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a><span data-ttu-id="a6ccb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6ccb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ccb-111">*isolationInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a6ccb-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ccb-112">Um ponteiro para um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém a conectividade e as informações de estado estendido do cliente.</span><span class="sxs-lookup"><span data-stu-id="a6ccb-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity and extended state information of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ccb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6ccb-113">Return value</span></span>

<span data-ttu-id="a6ccb-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="a6ccb-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a6ccb-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a6ccb-115">Return code</span></span>                                                                                     | <span data-ttu-id="a6ccb-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6ccb-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6ccb-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ccb-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a6ccb-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a6ccb-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a6ccb-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ccb-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a6ccb-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="a6ccb-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a6ccb-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ccb-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a6ccb-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a6ccb-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6ccb-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6ccb-123">Remarks</span></span>

<span data-ttu-id="a6ccb-124">Essas informações são definidas pelo NapAgent após o processamento de um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) e não devem ser definidas pelo aplicador.</span><span class="sxs-lookup"><span data-stu-id="a6ccb-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

<span data-ttu-id="a6ccb-125">O SHA deve liberar a estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="a6ccb-125">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ccb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6ccb-126">Requirements</span></span>



| <span data-ttu-id="a6ccb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ccb-127">Requirement</span></span> | <span data-ttu-id="a6ccb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a6ccb-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ccb-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6ccb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ccb-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6ccb-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a6ccb-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6ccb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ccb-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6ccb-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a6ccb-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6ccb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ccb-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ccb-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6ccb-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="a6ccb-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6ccb-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6ccb-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6ccb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ccb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ccb-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ccb-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a6ccb-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6ccb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ccb-140">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="a6ccb-140">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





