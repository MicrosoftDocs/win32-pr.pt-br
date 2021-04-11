---
title: Método INapSystemHealthAgentRequest GetSoHRequest (NapSystemHealthAgent. h)
description: Pode ser usado por SHAs Get SoHs anteriormente armazenado em cache pelo NapAgent.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009694"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a><span data-ttu-id="b6d83-106">Método INapSystemHealthAgentRequest:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="b6d83-106">INapSystemHealthAgentRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="b6d83-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="b6d83-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b6d83-108">O método **INapSystemHealthAgentRequest:: GetSoHRequest** pode ser usado por SHAs Get SoHs armazenado em cache anteriormente pelo NapAgent.</span><span class="sxs-lookup"><span data-stu-id="b6d83-108">The **INapSystemHealthAgentRequest::GetSoHRequest** method can be used by SHAs get SoHs previously cached by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6d83-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6d83-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="b6d83-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6d83-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6d83-111">*sohRequest* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6d83-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6d83-112">Um ponteiro para um ponteiro para um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="b6d83-112">A pointer to a pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6d83-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6d83-113">Return value</span></span>

<span data-ttu-id="b6d83-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="b6d83-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b6d83-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b6d83-115">Return code</span></span>                                                                                            | <span data-ttu-id="b6d83-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6d83-116">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6d83-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d83-117"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="b6d83-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b6d83-118">Operation succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="b6d83-119"><dt>**NAP \_ E \_ nenhum \_ soh armazenado em cache \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d83-119"><dt>**NAP\_E\_NO\_CACHED\_SOH**</dt></span></span> </dl> | <span data-ttu-id="b6d83-120">A SoH não foi encontrada; NapAgent não tem uma cópia armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="b6d83-120">The SoH is not found; NapAgent does not have a cached copy.</span></span><br/> |
| <dl> <span data-ttu-id="b6d83-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d83-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="b6d83-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="b6d83-122">Permissions error, access denied.</span></span><br/>                           |
| <dl> <span data-ttu-id="b6d83-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6d83-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="b6d83-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b6d83-124">System resource limit, could not perform the operation.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="b6d83-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6d83-125">Requirements</span></span>



| <span data-ttu-id="b6d83-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6d83-126">Requirement</span></span> | <span data-ttu-id="b6d83-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b6d83-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d83-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6d83-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b6d83-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6d83-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b6d83-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6d83-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b6d83-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6d83-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b6d83-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6d83-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6d83-133"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6d83-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6d83-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="b6d83-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6d83-135"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6d83-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="b6d83-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b6d83-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6d83-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6d83-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="b6d83-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6d83-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6d83-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="b6d83-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





