---
title: Método INapServerManagement RegisterSystemHealthValidator (NapServerManagement. h)
description: Registra um SHV.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Método RegisterSystemHealthValidator NAP
- Método RegisterSystemHealthValidator NAP, interface INapServerManagement
- INapServerManagement interface NAP, método RegisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163630"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a><span data-ttu-id="b908e-106">Método INapServerManagement:: RegisterSystemHealthValidator</span><span class="sxs-lookup"><span data-stu-id="b908e-106">INapServerManagement::RegisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="b908e-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="b908e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b908e-108">O método **INapServerManagement:: RegisterSystemHealthValidator** registra um SHV.</span><span class="sxs-lookup"><span data-stu-id="b908e-108">The **INapServerManagement::RegisterSystemHealthValidator** method registers an SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="b908e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b908e-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a><span data-ttu-id="b908e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b908e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b908e-111">*validador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b908e-111">*validator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b908e-112">Um ponteiro para uma estrutura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) que contém as informações de registro de SHV.</span><span class="sxs-lookup"><span data-stu-id="b908e-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="b908e-113">*validatorClsid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b908e-113">*validatorClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b908e-114">Um ponteiro para o CLSID da classe COM que implementa a interface [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) .</span><span class="sxs-lookup"><span data-stu-id="b908e-114">A pointer to the CLSID of the COM class that implements the [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b908e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b908e-115">Return value</span></span>

<span data-ttu-id="b908e-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="b908e-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b908e-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b908e-117">Return code</span></span>                                                                                            | <span data-ttu-id="b908e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b908e-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b908e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b908e-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="b908e-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b908e-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b908e-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b908e-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="b908e-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="b908e-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b908e-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b908e-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="b908e-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b908e-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b908e-125"><dt>**NAP \_ E \_ ID conflitante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b908e-125"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="b908e-126">A ID de SHV já está registrada.</span><span class="sxs-lookup"><span data-stu-id="b908e-126">SHV id is already registered.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="b908e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b908e-127">Requirements</span></span>



| <span data-ttu-id="b908e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b908e-128">Requirement</span></span> | <span data-ttu-id="b908e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b908e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b908e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b908e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b908e-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b908e-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="b908e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b908e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b908e-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b908e-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b908e-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b908e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b908e-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="b908e-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b908e-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="b908e-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b908e-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b908e-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b908e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b908e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b908e-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b908e-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="b908e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b908e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b908e-141">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="b908e-141">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





