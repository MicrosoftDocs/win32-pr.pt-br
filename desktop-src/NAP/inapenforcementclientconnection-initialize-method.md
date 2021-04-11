---
title: Método de inicialização de INapEnforcementClientConnection (NapEnforcementClient. h)
description: Inicializa a conexão do cliente.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454905"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a><span data-ttu-id="13ba9-106">Método INapEnforcementClientConnection:: Initialize</span><span class="sxs-lookup"><span data-stu-id="13ba9-106">INapEnforcementClientConnection::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="13ba9-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="13ba9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="13ba9-108">O método **INapEnforcementClientConnection:: Initialize** Inicializa a conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="13ba9-108">The **INapEnforcementClientConnection::Initialize** method initializes the client connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ba9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13ba9-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="13ba9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13ba9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ba9-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="13ba9-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ba9-112">Um ponteiro para um [**EnforementEntityId**](nap-datatypes.md) que identifica o cliente de imposição que solicita a conexão.</span><span class="sxs-lookup"><span data-stu-id="13ba9-112">A pointer to an [**EnforementEntityId**](nap-datatypes.md) that identifies the enforcement client requesting the connection.</span></span> <span data-ttu-id="13ba9-113">Esse valor é definido pelo NapAgent durante a criação da conexão.</span><span class="sxs-lookup"><span data-stu-id="13ba9-113">This value is set by the NapAgent during connection creation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ba9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13ba9-114">Return value</span></span>

<span data-ttu-id="13ba9-115">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="13ba9-115">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="13ba9-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="13ba9-116">Return code</span></span>                                                                                     | <span data-ttu-id="13ba9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="13ba9-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="13ba9-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="13ba9-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="13ba9-119">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="13ba9-119">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="13ba9-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="13ba9-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="13ba9-121">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="13ba9-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="13ba9-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13ba9-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="13ba9-123">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="13ba9-123">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="13ba9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ba9-124">Requirements</span></span>



| <span data-ttu-id="13ba9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="13ba9-125">Requirement</span></span> | <span data-ttu-id="13ba9-126">Valor</span><span class="sxs-lookup"><span data-stu-id="13ba9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ba9-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13ba9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="13ba9-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13ba9-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13ba9-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13ba9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="13ba9-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13ba9-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13ba9-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13ba9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="13ba9-132"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="13ba9-132"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="13ba9-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="13ba9-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13ba9-134"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13ba9-134"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="13ba9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="13ba9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13ba9-136"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13ba9-136"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="13ba9-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="13ba9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ba9-138">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="13ba9-138">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





