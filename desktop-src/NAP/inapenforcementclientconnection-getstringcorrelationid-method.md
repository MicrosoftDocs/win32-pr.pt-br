---
title: Método INapEnforcementClientConnection GetStringCorrelationId (NapEnforcementClient. h)
description: Obtém a versão da cadeia de caracteres da ID usada para correlacionar solicitações e respostas.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Método GetStringCorrelationId NAP
- Método GetStringCorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499308"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a><span data-ttu-id="21246-106">Método INapEnforcementClientConnection:: GetStringCorrelationId</span><span class="sxs-lookup"><span data-stu-id="21246-106">INapEnforcementClientConnection::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="21246-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="21246-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="21246-108">O método **INapEnforcementClientConnection:: GetStringCorrelationId** Obtém a versão de cadeia de caracteres da ID usada para correlacionar solicitações e respostas.</span><span class="sxs-lookup"><span data-stu-id="21246-108">The **INapEnforcementClientConnection::GetStringCorrelationId** method gets the string version of the ID used to correlate requests and responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="21246-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21246-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="21246-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21246-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21246-111">*CorrelationId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="21246-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21246-112">Um ponteiro para uma estrutura de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a versão da cadeia de caracteres da [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)da conexão.</span><span class="sxs-lookup"><span data-stu-id="21246-112">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the string version of the connection's [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21246-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21246-113">Return value</span></span>

<span data-ttu-id="21246-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="21246-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="21246-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="21246-115">Return code</span></span>                                                                                     | <span data-ttu-id="21246-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="21246-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="21246-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21246-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="21246-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="21246-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="21246-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="21246-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="21246-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="21246-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="21246-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="21246-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="21246-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="21246-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21246-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21246-123">Requirements</span></span>



| <span data-ttu-id="21246-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="21246-124">Requirement</span></span> | <span data-ttu-id="21246-125">Valor</span><span class="sxs-lookup"><span data-stu-id="21246-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21246-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21246-126">Minimum supported client</span></span><br/> | <span data-ttu-id="21246-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21246-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="21246-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21246-128">Minimum supported server</span></span><br/> | <span data-ttu-id="21246-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21246-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="21246-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21246-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="21246-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="21246-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="21246-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="21246-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21246-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21246-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="21246-134">DLL</span><span class="sxs-lookup"><span data-stu-id="21246-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21246-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21246-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="21246-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="21246-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21246-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="21246-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





