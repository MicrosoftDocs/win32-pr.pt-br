---
title: Método CorrelationId INapEnforcementClientConnection (NapEnforcementClient. h)
description: Define a ID usada para correlacionar SoH-solicitações e as respostas SoH.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Método CorrelationId NAP
- Método CorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método CorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499307"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a><span data-ttu-id="522fa-106">Método INapEnforcementClientConnection:: CorrelationId</span><span class="sxs-lookup"><span data-stu-id="522fa-106">INapEnforcementClientConnection::SetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="522fa-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="522fa-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="522fa-108">O método **INapEnforcementClientConnection:: CorrelationId** define a ID usada para correlacionar soh-solicitações e as respostas soh.</span><span class="sxs-lookup"><span data-stu-id="522fa-108">The **INapEnforcementClientConnection::SetCorrelationId** method sets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="522fa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="522fa-109">Syntax</span></span>


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="522fa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="522fa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522fa-111">*CorrelationId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="522fa-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="522fa-112">Uma estrutura exclusiva de [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) que identifica uma troca de soh específica.</span><span class="sxs-lookup"><span data-stu-id="522fa-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies a specific SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="522fa-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="522fa-113">Return value</span></span>

<span data-ttu-id="522fa-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="522fa-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="522fa-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="522fa-115">Return code</span></span>                                                                                     | <span data-ttu-id="522fa-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="522fa-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="522fa-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="522fa-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="522fa-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="522fa-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="522fa-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="522fa-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="522fa-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="522fa-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="522fa-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="522fa-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="522fa-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="522fa-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="522fa-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="522fa-123">Remarks</span></span>

<span data-ttu-id="522fa-124">A ID de correlação é definida pelo NapAgent e com base na ID de conexão.</span><span class="sxs-lookup"><span data-stu-id="522fa-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="522fa-125">Essa ID é usada para correlacionar solicitações e respostas, ou seja, ela descreve exclusivamente uma troca SoH e sempre contém a ID da SoH mais recente definida no objeto de conexão.</span><span class="sxs-lookup"><span data-stu-id="522fa-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="522fa-126">Quando um SoH-Response é recebido, o NapAgent primeiro garante a correspondência de IDs; caso contrário, um erro será retornado e o aplicador deverá descartar o pacote.</span><span class="sxs-lookup"><span data-stu-id="522fa-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="522fa-127">Consulte [**INapEnforcementClientBinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="522fa-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="522fa-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="522fa-128">Requirements</span></span>



| <span data-ttu-id="522fa-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="522fa-129">Requirement</span></span> | <span data-ttu-id="522fa-130">Valor</span><span class="sxs-lookup"><span data-stu-id="522fa-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="522fa-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="522fa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="522fa-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="522fa-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="522fa-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="522fa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="522fa-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="522fa-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="522fa-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="522fa-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="522fa-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="522fa-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="522fa-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="522fa-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="522fa-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="522fa-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="522fa-139">DLL</span><span class="sxs-lookup"><span data-stu-id="522fa-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="522fa-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="522fa-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="522fa-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="522fa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522fa-142">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="522fa-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





