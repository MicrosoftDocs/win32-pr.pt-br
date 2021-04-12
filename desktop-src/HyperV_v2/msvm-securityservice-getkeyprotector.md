---
description: Recupera o protetor de chave para um sistema virtual.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Método GetKeyProtector da classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49f2479660d0402c7b3d428c76f9fe454ecf64cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297779"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="7a2ea-103">Método GetKeyProtector da \_ classe SecurityService Msvm</span><span class="sxs-lookup"><span data-stu-id="7a2ea-103">GetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="7a2ea-104">Recupera o protetor de chave para um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7a2ea-104">Retrieves the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a2ea-105">Syntax</span></span>


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a><span data-ttu-id="7a2ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a2ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a2ea-107">*SecuritySettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a2ea-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a2ea-108">A cadeia de caracteres contém uma instância inserida da classe [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) que representa as configurações de segurança de um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="7a2ea-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="7a2ea-109">*Keyprotector* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7a2ea-109">*KeyProtector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a2ea-110">Recebe a matriz de bytes brutos que contém o protetor de chave atualmente em uso.</span><span class="sxs-lookup"><span data-stu-id="7a2ea-110">Receives the raw byte array that contains the key protector currently in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a2ea-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a2ea-111">Return value</span></span>

<span data-ttu-id="7a2ea-112">Em caso de sucesso, retorna 0 ou 4096.</span><span class="sxs-lookup"><span data-stu-id="7a2ea-112">On success, returns a 0 or 4096.</span></span> <span data-ttu-id="7a2ea-113">Caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="7a2ea-113">Otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7a2ea-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7a2ea-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="7a2ea-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7a2ea-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a2ea-127">Requirements</span></span>



| <span data-ttu-id="7a2ea-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a2ea-128">Requirement</span></span> | <span data-ttu-id="7a2ea-129">Valor</span><span class="sxs-lookup"><span data-stu-id="7a2ea-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2ea-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a2ea-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a2ea-131">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="7a2ea-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7a2ea-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a2ea-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a2ea-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7a2ea-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7a2ea-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a2ea-134">Namespace</span></span><br/>                | <span data-ttu-id="7a2ea-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7a2ea-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7a2ea-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7a2ea-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a2ea-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a2ea-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a2ea-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7a2ea-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a2ea-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a2ea-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7a2ea-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a2ea-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2ea-141">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="7a2ea-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




