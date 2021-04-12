---
title: Método INapClientManagement RegisterSystemHealthAgent (NapManagement. h)
description: Registra um SHA com o sistema NAP.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Método RegisterSystemHealthAgent NAP
- Método RegisterSystemHealthAgent NAP, interface INapClientManagement
- INapClientManagement interface NAP, método RegisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455513"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a><span data-ttu-id="19348-106">Método INapClientManagement:: RegisterSystemHealthAgent</span><span class="sxs-lookup"><span data-stu-id="19348-106">INapClientManagement::RegisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="19348-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="19348-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19348-108">O método **RegisterSystemHealthAgent** registra um Sha com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="19348-108">The **RegisterSystemHealthAgent** method registers an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="19348-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19348-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a><span data-ttu-id="19348-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19348-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19348-111">*agente* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="19348-111">*agent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19348-112">Um ponteiro para uma estrutura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contém as informações de registro para o Sha.</span><span class="sxs-lookup"><span data-stu-id="19348-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the registration information for the SHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19348-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="19348-113">Return value</span></span>

<span data-ttu-id="19348-114">O método retorna um código de status HRESULT, incluindo, mas não se limitando a um dos itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="19348-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="19348-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="19348-115">Return code</span></span>                                                                                            | <span data-ttu-id="19348-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="19348-116">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="19348-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19348-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="19348-118">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="19348-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="19348-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="19348-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="19348-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="19348-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="19348-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="19348-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="19348-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="19348-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="19348-123"><dt>**NAP \_ E \_ ID conflitante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="19348-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="19348-124">Um SHA que usa essa ID já está registrado.</span><span class="sxs-lookup"><span data-stu-id="19348-124">An SHA that uses this ID is already registered.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="19348-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19348-125">Requirements</span></span>



| <span data-ttu-id="19348-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="19348-126">Requirement</span></span> | <span data-ttu-id="19348-127">Valor</span><span class="sxs-lookup"><span data-stu-id="19348-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19348-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19348-128">Minimum supported client</span></span><br/> | <span data-ttu-id="19348-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19348-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="19348-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19348-130">Minimum supported server</span></span><br/> | <span data-ttu-id="19348-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19348-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="19348-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19348-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="19348-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="19348-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="19348-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="19348-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19348-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19348-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="19348-136">DLL</span><span class="sxs-lookup"><span data-stu-id="19348-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19348-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19348-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="19348-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="19348-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19348-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="19348-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





