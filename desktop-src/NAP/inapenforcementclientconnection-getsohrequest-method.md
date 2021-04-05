---
title: Método INapEnforcementClientConnection GetSoHRequest (NapEnforcementClient. h)
description: Obtém a solicitação SoH atual.
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6115e607f810aef67911ec7d7800d35207368e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918237"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a><span data-ttu-id="4da4e-106">Método INapEnforcementClientConnection:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="4da4e-106">INapEnforcementClientConnection::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="4da4e-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="4da4e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4da4e-108">O método **INapEnforcementClientConnection:: GetSoHRequest** Obtém a solicitação soh atual.</span><span class="sxs-lookup"><span data-stu-id="4da4e-108">The **INapEnforcementClientConnection::GetSoHRequest** method gets the current SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da4e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4da4e-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="4da4e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4da4e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da4e-111">*sohRequest* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4da4e-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4da4e-112">Um ponteiro para um ponteiro para uma estrutura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , que é um blob de dados opaco para o aplicador.</span><span class="sxs-lookup"><span data-stu-id="4da4e-112">A pointer to a pointer to a [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da4e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4da4e-113">Return value</span></span>

<span data-ttu-id="4da4e-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="4da4e-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4da4e-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4da4e-115">Return code</span></span>                                                                                     | <span data-ttu-id="4da4e-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4da4e-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4da4e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4da4e-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4da4e-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4da4e-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4da4e-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4da4e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4da4e-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="4da4e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4da4e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4da4e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4da4e-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="4da4e-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4da4e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="4da4e-123">Remarks</span></span>

<span data-ttu-id="4da4e-124">Isso é definido pelo NapAgent e consultado pelos imforçadores para envio na conexão.</span><span class="sxs-lookup"><span data-stu-id="4da4e-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="4da4e-125">Um pacote SoH de comprimento de byte zero é inválido.</span><span class="sxs-lookup"><span data-stu-id="4da4e-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da4e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4da4e-126">Requirements</span></span>



| <span data-ttu-id="4da4e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da4e-127">Requirement</span></span> | <span data-ttu-id="4da4e-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4da4e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da4e-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4da4e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4da4e-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4da4e-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4da4e-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4da4e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4da4e-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4da4e-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4da4e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4da4e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da4e-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da4e-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4da4e-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="4da4e-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4da4e-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4da4e-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="4da4e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4da4e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4da4e-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4da4e-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4da4e-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="4da4e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da4e-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="4da4e-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





