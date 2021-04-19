---
description: Define o protetor de chave para um sistema virtual.
ms.assetid: 84c114cb-a3a0-44f2-b862-38b05b96bd46
title: Método SetKeyProtector da classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 404baf0a529a6e96869fbcd355a81308f5d1e966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753471"
---
# <a name="setkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="5ee7a-103">Método SetKeyProtector da \_ classe SecurityService Msvm</span><span class="sxs-lookup"><span data-stu-id="5ee7a-103">SetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="5ee7a-104">Define o protetor de chave para um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-104">Sets the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee7a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ee7a-105">Syntax</span></span>


```mof
uint32 SetKeyProtector(
  [in]  string              SecuritySettingData,
  [in]  uint8               KeyProtector[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5ee7a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ee7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ee7a-107">*SecuritySettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ee7a-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee7a-108">A cadeia de caracteres contém uma instância inserida da classe [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) que representa as configurações de segurança de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="5ee7a-109">*Keyprotector* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ee7a-109">*KeyProtector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee7a-110">A matriz de bytes brutos que contém o protetor de chave a ser definido.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-110">Raw byte array that contains the key protector to set.</span></span>

</dd> <dt>

<span data-ttu-id="5ee7a-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="5ee7a-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee7a-112">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-112">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="5ee7a-113">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-113">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ee7a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ee7a-114">Return value</span></span>

<span data-ttu-id="5ee7a-115">Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="5ee7a-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5ee7a-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="5ee7a-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5ee7a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ee7a-129">Requirements</span></span>



| <span data-ttu-id="5ee7a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee7a-130">Requirement</span></span> | <span data-ttu-id="5ee7a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee7a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee7a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ee7a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5ee7a-133">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="5ee7a-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5ee7a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ee7a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5ee7a-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5ee7a-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5ee7a-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ee7a-136">Namespace</span></span><br/>                | <span data-ttu-id="5ee7a-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5ee7a-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ee7a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5ee7a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ee7a-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ee7a-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ee7a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5ee7a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ee7a-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ee7a-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ee7a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ee7a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee7a-143">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="5ee7a-143">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




