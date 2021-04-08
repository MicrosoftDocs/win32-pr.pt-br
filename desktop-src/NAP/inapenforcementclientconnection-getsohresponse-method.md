---
title: Método INapEnforcementClientConnection GetSoHResponse (NapEnforcementClient. h)
description: Obtém o SoH-Response recebido pelo cliente de imposição.
ms.assetid: fc0084a3-a668-435e-8390-f322941c5cd4
keywords:
- Método GetSoHResponse NAP
- Método GetSoHResponse NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método GetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4d65135d6e4ce606a83eb08fdeed036cc62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824286"
---
# <a name="inapenforcementclientconnectiongetsohresponse-method"></a><span data-ttu-id="29d47-106">Método INapEnforcementClientConnection:: GetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="29d47-106">INapEnforcementClientConnection::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="29d47-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="29d47-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="29d47-108">O método **INapEnforcementClientConnection:: GetSoHResponse** obtém o SoH-Response recebido pelo cliente de imposição.</span><span class="sxs-lookup"><span data-stu-id="29d47-108">The **INapEnforcementClientConnection::GetSoHResponse** method gets the SoH-Response received by the enforcement client.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d47-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29d47-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] NetworkSoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="29d47-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29d47-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29d47-111">*sohResponse* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="29d47-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29d47-112">Um ponteiro para um ponteiro para uma estrutura [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) exclusiva, que é um blob de dados opaco para o aplicador.</span><span class="sxs-lookup"><span data-stu-id="29d47-112">A pointer to a pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29d47-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29d47-113">Return value</span></span>

<span data-ttu-id="29d47-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="29d47-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="29d47-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="29d47-115">Return code</span></span>                                                                                     | <span data-ttu-id="29d47-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="29d47-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="29d47-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="29d47-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="29d47-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="29d47-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="29d47-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="29d47-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="29d47-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="29d47-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="29d47-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="29d47-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="29d47-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="29d47-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29d47-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="29d47-123">Remarks</span></span>

<span data-ttu-id="29d47-124">Um pacote de tamanho de zero byte é válido.</span><span class="sxs-lookup"><span data-stu-id="29d47-124">A zero-byte sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="29d47-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29d47-125">Requirements</span></span>



| <span data-ttu-id="29d47-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="29d47-126">Requirement</span></span> | <span data-ttu-id="29d47-127">Valor</span><span class="sxs-lookup"><span data-stu-id="29d47-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29d47-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29d47-128">Minimum supported client</span></span><br/> | <span data-ttu-id="29d47-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29d47-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="29d47-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29d47-130">Minimum supported server</span></span><br/> | <span data-ttu-id="29d47-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29d47-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="29d47-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29d47-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="29d47-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="29d47-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="29d47-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="29d47-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="29d47-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="29d47-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="29d47-136">DLL</span><span class="sxs-lookup"><span data-stu-id="29d47-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29d47-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29d47-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="29d47-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="29d47-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d47-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="29d47-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





