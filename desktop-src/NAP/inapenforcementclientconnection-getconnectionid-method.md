---
title: Método GetConnectionID INapEnforcementClientConnection (NapEnforcementClient. h)
description: É usado para obter a ID de conexão exclusiva do cliente.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- Método GetConnectionID NAP
- Método GetConnectionID NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método GetConnectionID
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086471"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a><span data-ttu-id="a3c2d-106">Método INapEnforcementClientConnection:: GetConnectionID</span><span class="sxs-lookup"><span data-stu-id="a3c2d-106">INapEnforcementClientConnection::GetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="a3c2d-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="a3c2d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a3c2d-108">O método **INapEnforcementClientConnection:: GetConnectionID** é usado para obter a ID de conexão exclusiva do cliente.</span><span class="sxs-lookup"><span data-stu-id="a3c2d-108">The **INapEnforcementClientConnection::GetConnectionId** method is used to get the unique connection ID of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3c2d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3c2d-109">Syntax</span></span>


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="a3c2d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3c2d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3c2d-111">*ConnectionID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3c2d-111">*connectionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3c2d-112">Um ponteiro para um ponteiro para uma [**ConnectionID**](nap-datatypes.md) que identifica exclusivamente essa conexão.</span><span class="sxs-lookup"><span data-stu-id="a3c2d-112">A pointer to a pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies this connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3c2d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3c2d-113">Return value</span></span>

<span data-ttu-id="a3c2d-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="a3c2d-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a3c2d-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a3c2d-115">Return code</span></span>                                                                                     | <span data-ttu-id="a3c2d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3c2d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3c2d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a3c2d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a3c2d-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a3c2d-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a3c2d-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a3c2d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a3c2d-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="a3c2d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a3c2d-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a3c2d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a3c2d-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="a3c2d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3c2d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3c2d-123">Remarks</span></span>

<span data-ttu-id="a3c2d-124">A ID de conexão é usada principalmente para fins de log.</span><span class="sxs-lookup"><span data-stu-id="a3c2d-124">The connection ID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3c2d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3c2d-125">Requirements</span></span>



| <span data-ttu-id="a3c2d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3c2d-126">Requirement</span></span> | <span data-ttu-id="a3c2d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a3c2d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c2d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3c2d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a3c2d-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3c2d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3c2d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3c2d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a3c2d-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3c2d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3c2d-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3c2d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3c2d-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3c2d-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3c2d-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="a3c2d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3c2d-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3c2d-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a3c2d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a3c2d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3c2d-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3c2d-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a3c2d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3c2d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3c2d-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a3c2d-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





