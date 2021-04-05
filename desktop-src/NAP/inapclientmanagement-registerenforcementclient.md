---
title: Método INapClientManagement RegisterEnforcementClient (NapManagement. h)
description: Registra um cliente de imposição com o sistema NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Método RegisterEnforcementClient NAP
- Método RegisterEnforcementClient NAP, interface INapClientManagement
- INapClientManagement interface NAP, método RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085894"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a><span data-ttu-id="708cd-106">Método INapClientManagement:: RegisterEnforcementClient</span><span class="sxs-lookup"><span data-stu-id="708cd-106">INapClientManagement::RegisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="708cd-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="708cd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="708cd-108">O método **RegisterEnforcementClient** registra um cliente de imposição com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="708cd-108">The **RegisterEnforcementClient** method registers an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="708cd-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="708cd-109">Syntax</span></span>


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a><span data-ttu-id="708cd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="708cd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708cd-111">*aplicar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="708cd-111">*enforcer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708cd-112">Um ponteiro para uma estrutura de dados [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contém as informações de registro associadas ao cliente de imposição.</span><span class="sxs-lookup"><span data-stu-id="708cd-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structure that contains the registration information that is associated with the enforcement client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="708cd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="708cd-113">Return value</span></span>

<span data-ttu-id="708cd-114">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="708cd-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="708cd-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="708cd-115">Return code</span></span>                                                                                            | <span data-ttu-id="708cd-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="708cd-116">Description</span></span>                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="708cd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="708cd-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="708cd-118">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="708cd-118">Operation successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="708cd-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="708cd-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="708cd-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="708cd-120">Permissions error, access denied.</span></span><br/>                                      |
| <dl> <span data-ttu-id="708cd-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="708cd-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="708cd-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="708cd-122">System resource limit, could not perform the operation.</span></span><br/>                |
| <dl> <span data-ttu-id="708cd-123"><dt>**NAP \_ E \_ ID conflitante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="708cd-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="708cd-124">Um agente de imposição usando o identificador fornecido já está registrado.</span><span class="sxs-lookup"><span data-stu-id="708cd-124">An enforcement agent using the given identifier is already registered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="708cd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="708cd-125">Requirements</span></span>



| <span data-ttu-id="708cd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="708cd-126">Requirement</span></span> | <span data-ttu-id="708cd-127">Valor</span><span class="sxs-lookup"><span data-stu-id="708cd-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="708cd-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="708cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="708cd-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="708cd-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="708cd-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="708cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="708cd-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="708cd-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="708cd-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="708cd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="708cd-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="708cd-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="708cd-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="708cd-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="708cd-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="708cd-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="708cd-136">DLL</span><span class="sxs-lookup"><span data-stu-id="708cd-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="708cd-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="708cd-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="708cd-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="708cd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708cd-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="708cd-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





