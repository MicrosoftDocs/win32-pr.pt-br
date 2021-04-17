---
title: Método GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
description: É usado para diferenciar respostas de primeira vez de respostas devido a SoHRequests armazenados em cache pelos imforçadores. | Método GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Método GetFlags NAP
- Método GetFlags NAP, interface INapEnforcementClientConnection
- Interface INapEnforcementClientConnection NAP, método GetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105747307"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a><span data-ttu-id="3debf-107">Método INapEnforcementClientConnection:: GetFlags</span><span class="sxs-lookup"><span data-stu-id="3debf-107">INapEnforcementClientConnection::GetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="3debf-108">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="3debf-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3debf-109">O método **INapEnforcementClientConnection:: GetFlags** é usado para diferenciar respostas de primeira vez de respostas devido ao SoHRequests armazenado em cache pelos imforçadores.</span><span class="sxs-lookup"><span data-stu-id="3debf-109">The **INapEnforcementClientConnection::GetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="3debf-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3debf-110">Syntax</span></span>


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a><span data-ttu-id="3debf-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3debf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3debf-112">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="3debf-112">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3debf-113">Um ponteiro para um sinalizador que determina se o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) é devido a um **SoHRequest** armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="3debf-113">A pointer to a flag that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="3debf-114">Se *flags* tiver um valor de [**freshSoHRequest**](nap-type-constants.md), será uma nova solicitação; caso contrário, será uma solicitação armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="3debf-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3debf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3debf-115">Return value</span></span>

<span data-ttu-id="3debf-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="3debf-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3debf-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3debf-117">Return code</span></span>                                                                                     | <span data-ttu-id="3debf-118">Description</span><span class="sxs-lookup"><span data-stu-id="3debf-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3debf-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3debf-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3debf-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3debf-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3debf-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3debf-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3debf-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="3debf-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3debf-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3debf-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3debf-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="3debf-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3debf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3debf-125">Requirements</span></span>



| <span data-ttu-id="3debf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3debf-126">Requirement</span></span> | <span data-ttu-id="3debf-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3debf-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3debf-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3debf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3debf-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3debf-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3debf-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3debf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3debf-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3debf-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3debf-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3debf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3debf-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3debf-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3debf-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="3debf-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3debf-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3debf-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="3debf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3debf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3debf-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3debf-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3debf-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3debf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3debf-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="3debf-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





