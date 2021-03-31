---
title: Método INapEnforcementClientConnection SetSoHRequest (NapEnforcementClient. h)
description: Define a solicitação SoH.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Método SetSoHRequest NAP
- Método SetSoHRequest NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método SetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644502"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a><span data-ttu-id="733e5-106">Método INapEnforcementClientConnection:: SetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="733e5-106">INapEnforcementClientConnection::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="733e5-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="733e5-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="733e5-108">O método **INapEnforcementClientConnection:: SetSoHRequest** define a solicitação soh-Request.</span><span class="sxs-lookup"><span data-stu-id="733e5-108">The **INapEnforcementClientConnection::SetSoHRequest** method sets the SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="733e5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="733e5-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="733e5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="733e5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733e5-111">*sohRequest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="733e5-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733e5-112">Um ponteiro para uma estrutura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) exclusiva, que é um blob de dados opaco para o aplicador.</span><span class="sxs-lookup"><span data-stu-id="733e5-112">A pointer to a unique [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733e5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="733e5-113">Return value</span></span>

<span data-ttu-id="733e5-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="733e5-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="733e5-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="733e5-115">Return code</span></span>                                                                                     | <span data-ttu-id="733e5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="733e5-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="733e5-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="733e5-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="733e5-118">O pacote SoH é válido.</span><span class="sxs-lookup"><span data-stu-id="733e5-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="733e5-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="733e5-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="733e5-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="733e5-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="733e5-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="733e5-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="733e5-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="733e5-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="733e5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="733e5-123">Remarks</span></span>

<span data-ttu-id="733e5-124">Isso é definido pelo NapAgent e consultado pelos imforçadores para envio na conexão.</span><span class="sxs-lookup"><span data-stu-id="733e5-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="733e5-125">Um pacote SoH de comprimento de byte zero é inválido.</span><span class="sxs-lookup"><span data-stu-id="733e5-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="733e5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="733e5-126">Requirements</span></span>



| <span data-ttu-id="733e5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="733e5-127">Requirement</span></span> | <span data-ttu-id="733e5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="733e5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="733e5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="733e5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="733e5-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="733e5-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="733e5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="733e5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="733e5-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="733e5-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="733e5-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="733e5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="733e5-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="733e5-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="733e5-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="733e5-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="733e5-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="733e5-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="733e5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="733e5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="733e5-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="733e5-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="733e5-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="733e5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733e5-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="733e5-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





