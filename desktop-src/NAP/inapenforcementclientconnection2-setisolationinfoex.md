---
title: Método INapEnforcementClientConnection2 SetIsolationInfoEx (NapEnforcementClient. h)
description: É usado pelo NapAgent para definir as informações de isolamento para o cliente.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- Método SetIsolationInfoEx NAP
- Método SetIsolationInfoEx NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, método SetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711b4bfd27c3bd92d48a78f4767f5ed452b2d4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812760"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a><span data-ttu-id="455c2-106">Método INapEnforcementClientConnection2:: SetIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="455c2-106">INapEnforcementClientConnection2::SetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="455c2-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="455c2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="455c2-108">O método **INapEnforcementClientConnection2:: SetIsolationInfoEx** é usado pelo NapAgent para definir as informações de isolamento para o cliente.</span><span class="sxs-lookup"><span data-stu-id="455c2-108">The **INapEnforcementClientConnection2::SetIsolationInfoEx** method is used by the NapAgent to set the isolation information for the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="455c2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="455c2-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="455c2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="455c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="455c2-111">*isolationInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="455c2-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="455c2-112">Um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém o estado de conectividade do cliente.</span><span class="sxs-lookup"><span data-stu-id="455c2-112">A pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="455c2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="455c2-113">Return value</span></span>

<span data-ttu-id="455c2-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="455c2-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="455c2-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="455c2-115">Return code</span></span>                                                                                     | <span data-ttu-id="455c2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="455c2-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="455c2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="455c2-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="455c2-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="455c2-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="455c2-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="455c2-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="455c2-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="455c2-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="455c2-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="455c2-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="455c2-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="455c2-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="455c2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="455c2-123">Remarks</span></span>

<span data-ttu-id="455c2-124">Essas informações são definidas pelo NapAgent após o processamento de um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) e não devem ser definidas pelo aplicador.</span><span class="sxs-lookup"><span data-stu-id="455c2-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="455c2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="455c2-125">Requirements</span></span>



| <span data-ttu-id="455c2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="455c2-126">Requirement</span></span> | <span data-ttu-id="455c2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="455c2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="455c2-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="455c2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="455c2-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="455c2-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="455c2-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="455c2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="455c2-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="455c2-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="455c2-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="455c2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="455c2-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="455c2-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="455c2-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="455c2-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="455c2-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="455c2-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="455c2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="455c2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="455c2-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="455c2-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="455c2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="455c2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455c2-139">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="455c2-139">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





