---
title: Método setmaxsize INapEnforcementClientConnection (NapEnforcementClient. h)
description: Define o tamanho máximo do pacote SoH para esse cliente.
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- Método setmaxsize NAP
- Método setmaxsize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método setmaxsize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b10d7bc1a023371683f17bb3e6e12cd578fa964
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369480"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a><span data-ttu-id="1829f-106">Método INapEnforcementClientConnection:: setmaxsize</span><span class="sxs-lookup"><span data-stu-id="1829f-106">INapEnforcementClientConnection::SetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="1829f-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="1829f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1829f-108">O método **INapEnforcementClientConnection:: setmaxsize** define o tamanho máximo do pacote soh para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="1829f-108">The **INapEnforcementClientConnection::SetMaxSize** method sets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="1829f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1829f-109">Syntax</span></span>


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="1829f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1829f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1829f-111">*MaxSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1829f-111">*maxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1829f-112">Uma estrutura [**ProtocolMaxSize**](nap-datatypes.md) que indica o tamanho máximo, em bytes, do pacote soh.</span><span class="sxs-lookup"><span data-stu-id="1829f-112">A [**ProtocolMaxSize**](nap-datatypes.md) structure that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1829f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1829f-113">Return value</span></span>

<span data-ttu-id="1829f-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="1829f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1829f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1829f-115">Return code</span></span>                                                                                     | <span data-ttu-id="1829f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="1829f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1829f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1829f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1829f-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1829f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1829f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1829f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1829f-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="1829f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1829f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1829f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1829f-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1829f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1829f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1829f-123">Remarks</span></span>

<span data-ttu-id="1829f-124">Esse valor é definido pelo cliente de imposição.</span><span class="sxs-lookup"><span data-stu-id="1829f-124">This value is set by the enforcement client.</span></span>

## <a name="requirements"></a><span data-ttu-id="1829f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1829f-125">Requirements</span></span>



| <span data-ttu-id="1829f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1829f-126">Requirement</span></span> | <span data-ttu-id="1829f-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1829f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1829f-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1829f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1829f-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1829f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1829f-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1829f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1829f-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1829f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1829f-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1829f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1829f-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1829f-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1829f-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="1829f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1829f-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1829f-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="1829f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1829f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1829f-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1829f-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1829f-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1829f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1829f-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="1829f-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





