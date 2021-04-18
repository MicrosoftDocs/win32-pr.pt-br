---
description: Gera um conjunto de WWNs (World Wide Port Names).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Método GenerateWwpn da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767646"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="56cba-103">Método GenerateWwpn da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="56cba-103">GenerateWwpn method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="56cba-104">Gera um conjunto de WWNs (World Wide Port Names).</span><span class="sxs-lookup"><span data-stu-id="56cba-104">Generates a set of World Wide Port Names (WWPNs).</span></span> <span data-ttu-id="56cba-105">Os WWPNs são gerados de dentro do intervalo pré-configurado definido pelas propriedades **MinimumWWPNAddress** e **MaximumWWPNAddress** da classe [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="56cba-105">The WWPNs are generated from within the pre-configured range defined by the **MinimumWWPNAddress** and **MaximumWWPNAddress** properties of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span> <span data-ttu-id="56cba-106">Se o número válido de WWPNs que pode ser gerado for menor que o número solicitado, as entradas restantes na matriz *GeneratedWwpn* terão a entrada inválida de "0000000000000000" e o valor de retorno indicará êxito (0).</span><span class="sxs-lookup"><span data-stu-id="56cba-106">If the valid number of WWPNs that can be generated is less than the requested number, then the remaining entries in the *GeneratedWwpn* array will have the invalid entry of "0000000000000000" and the return value will indicate success (0).</span></span>

## <a name="syntax"></a><span data-ttu-id="56cba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56cba-107">Syntax</span></span>


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a><span data-ttu-id="56cba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56cba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56cba-109">*NumberOfWwpns* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56cba-109">*NumberOfWwpns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56cba-110">O número de WWPNs a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="56cba-110">The number of WWPNs to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="56cba-111">*GeneratedWwpn* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="56cba-111">*GeneratedWwpn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56cba-112">Uma matriz de cadeias de caracteres, cada uma delas conterá um WWPN gerado.</span><span class="sxs-lookup"><span data-stu-id="56cba-112">An array of strings, each of which will contain a generated WWPN.</span></span> <span data-ttu-id="56cba-113">Ele será formatado em formato de cadeia de caracteres como "01:23:45:67:89: AB: CD: EF".</span><span class="sxs-lookup"><span data-stu-id="56cba-113">It will be formatted in string form as "01:23:45:67:89:ab:cd:ef".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56cba-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56cba-114">Return value</span></span>

<span data-ttu-id="56cba-115">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="56cba-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="56cba-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="56cba-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="56cba-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="56cba-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="56cba-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="56cba-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="56cba-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="56cba-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="56cba-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="56cba-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="56cba-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="56cba-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="56cba-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="56cba-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="56cba-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56cba-128">Requirements</span></span>



| <span data-ttu-id="56cba-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="56cba-129">Requirement</span></span> | <span data-ttu-id="56cba-130">Valor</span><span class="sxs-lookup"><span data-stu-id="56cba-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56cba-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56cba-131">Minimum supported client</span></span><br/> | <span data-ttu-id="56cba-132">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="56cba-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="56cba-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56cba-133">Minimum supported server</span></span><br/> | <span data-ttu-id="56cba-134">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="56cba-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56cba-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="56cba-135">Namespace</span></span><br/>                | <span data-ttu-id="56cba-136">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="56cba-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="56cba-137">MOF</span><span class="sxs-lookup"><span data-stu-id="56cba-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56cba-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56cba-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56cba-139">DLL</span><span class="sxs-lookup"><span data-stu-id="56cba-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56cba-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56cba-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56cba-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="56cba-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56cba-142">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="56cba-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




