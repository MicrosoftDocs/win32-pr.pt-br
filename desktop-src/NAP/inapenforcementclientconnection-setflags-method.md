---
title: Método SetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
description: É usado para diferenciar respostas de primeira vez de respostas devido a SoHRequests armazenados em cache pelos imforçadores. | Método SetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Método SetFlags NAP
- Método SetFlags NAP, interface INapEnforcementClientConnection
- Interface INapEnforcementClientConnection NAP, método SetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105749774"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a><span data-ttu-id="dfbf8-107">Método INapEnforcementClientConnection:: SetFlags</span><span class="sxs-lookup"><span data-stu-id="dfbf8-107">INapEnforcementClientConnection::SetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="dfbf8-108">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="dfbf8-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dfbf8-109">O método **INapEnforcementClientConnection:: SetFlags** é usado para diferenciar respostas de primeira vez de respostas devido ao SoHRequests armazenado em cache pelos imforçadores.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-109">The **INapEnforcementClientConnection::SetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbf8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfbf8-110">Syntax</span></span>


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a><span data-ttu-id="dfbf8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfbf8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfbf8-112">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="dfbf8-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfbf8-113">Sinalizadores que determinam se o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) é devido a um **SoHRequest** armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-113">Flags that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="dfbf8-114">Se *flags* tiver um valor de [**freshSoHRequest**](nap-type-constants.md), será uma nova solicitação; caso contrário, será uma solicitação armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfbf8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dfbf8-115">Return value</span></span>

<span data-ttu-id="dfbf8-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="dfbf8-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dfbf8-117">Return code</span></span>                                                                                     | <span data-ttu-id="dfbf8-118">Description</span><span class="sxs-lookup"><span data-stu-id="dfbf8-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfbf8-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf8-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="dfbf8-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dfbf8-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf8-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="dfbf8-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="dfbf8-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf8-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="dfbf8-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfbf8-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfbf8-125">Remarks</span></span>

<span data-ttu-id="dfbf8-126">Esse valor é definido pelo NapAgent.</span><span class="sxs-lookup"><span data-stu-id="dfbf8-126">This value is set by the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfbf8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfbf8-127">Requirements</span></span>



| <span data-ttu-id="dfbf8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfbf8-128">Requirement</span></span> | <span data-ttu-id="dfbf8-129">Valor</span><span class="sxs-lookup"><span data-stu-id="dfbf8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbf8-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfbf8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dfbf8-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfbf8-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dfbf8-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfbf8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dfbf8-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfbf8-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dfbf8-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfbf8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfbf8-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf8-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfbf8-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="dfbf8-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfbf8-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf8-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="dfbf8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="dfbf8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfbf8-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfbf8-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="dfbf8-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfbf8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfbf8-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="dfbf8-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





