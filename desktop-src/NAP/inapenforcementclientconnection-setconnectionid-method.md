---
title: Método setconnectionid INapEnforcementClientConnection (NapEnforcementClient. h)
description: É usado para definir a ID exclusiva da conexão e deve ser definido pelo cliente de imposição assim que a conexão é criada.
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- Método setconnectionid NAP
- Método setconnectionid NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método setconnectionid
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9749be304170ec7706b637429f577e77411ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918236"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a><span data-ttu-id="f25dd-106">Método INapEnforcementClientConnection:: setconnectionid</span><span class="sxs-lookup"><span data-stu-id="f25dd-106">INapEnforcementClientConnection::SetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="f25dd-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="f25dd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f25dd-108">O método **INapEnforcementClientConnection:: Setconnectionid** é usado para definir a ID exclusiva da conexão e deve ser definido pelo cliente de imposição assim que a conexão é criada.</span><span class="sxs-lookup"><span data-stu-id="f25dd-108">The **INapEnforcementClientConnection::SetConnectionId** method is used to set the unique ID of the connection and must be set by the enforcement client as soon as the connection is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="f25dd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f25dd-109">Syntax</span></span>


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="f25dd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f25dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f25dd-111">*ConnectionID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f25dd-111">*connectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f25dd-112">Um ponteiro para uma [**ConnectionID**](nap-datatypes.md) que identifica exclusivamente uma conexão.</span><span class="sxs-lookup"><span data-stu-id="f25dd-112">A pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f25dd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f25dd-113">Return value</span></span>

<span data-ttu-id="f25dd-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="f25dd-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f25dd-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f25dd-115">Return code</span></span>                                                                                     | <span data-ttu-id="f25dd-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f25dd-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f25dd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f25dd-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f25dd-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f25dd-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f25dd-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f25dd-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f25dd-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="f25dd-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f25dd-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f25dd-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f25dd-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="f25dd-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f25dd-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f25dd-123">Remarks</span></span>

<span data-ttu-id="f25dd-124">Essa ConnectionID é usada principalmente para fins de log.</span><span class="sxs-lookup"><span data-stu-id="f25dd-124">This ConnectionID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f25dd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f25dd-125">Requirements</span></span>



| <span data-ttu-id="f25dd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f25dd-126">Requirement</span></span> | <span data-ttu-id="f25dd-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f25dd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f25dd-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f25dd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f25dd-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f25dd-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f25dd-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f25dd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f25dd-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f25dd-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f25dd-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f25dd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f25dd-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f25dd-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f25dd-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="f25dd-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f25dd-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f25dd-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f25dd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f25dd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f25dd-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f25dd-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f25dd-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f25dd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f25dd-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="f25dd-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





