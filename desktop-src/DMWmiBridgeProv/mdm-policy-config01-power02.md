---
title: Classe MDM_Policy_Config01_Power02
description: A \_ classe Config01 Power02 de política de MDM \_ \_ configura as políticas de energia.
ms.assetid: 8913c38c-0d8d-456f-a412-d47c2ccd5d13
keywords:
- Classe MDM_Policy_Config01_Power02
- Classe MDM_Policy_Config01_Power02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Power02
- MDM_Policy_Config01_Power02.InstanceID
- MDM_Policy_Config01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9bdda57bbd85100e8bccb87990d928f448a972
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085531"
---
# <a name="mdm_policy_config01_power02-class"></a><span data-ttu-id="2bdbf-105">\_Classe MDM \_ Config01 \_ Power02</span><span class="sxs-lookup"><span data-stu-id="2bdbf-105">MDM\_Policy\_Config01\_Power02 class</span></span>

<span data-ttu-id="2bdbf-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2bdbf-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2bdbf-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2bdbf-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2bdbf-108">A \_ classe Config01 Power02 de política de MDM \_ \_ configura as políticas de energia.</span><span class="sxs-lookup"><span data-stu-id="2bdbf-108">The MDM\_Policy\_Config01\_Power02 class configures the power policies.</span></span>

<span data-ttu-id="2bdbf-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2bdbf-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bdbf-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bdbf-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a><span data-ttu-id="2bdbf-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2bdbf-111">Members</span></span>

<span data-ttu-id="2bdbf-112">A **classe \_ \_ Config01 \_ Power02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2bdbf-112">The **MDM\_Policy\_Config01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="2bdbf-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2bdbf-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bdbf-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2bdbf-114">Properties</span></span>

<span data-ttu-id="2bdbf-115">A **classe \_ \_ Config01 \_ Power02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2bdbf-115">The **MDM\_Policy\_Config01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2bdbf-116">AllowStandbyWhenSleepingPluggedIn</span><span class="sxs-lookup"><span data-stu-id="2bdbf-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bdbf-119">DisplayOffTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="2bdbf-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bdbf-122">DisplayOffTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="2bdbf-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bdbf-125">HibernateTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="2bdbf-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bdbf-128">HibernateTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="2bdbf-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bdbf-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2bdbf-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bdbf-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bdbf-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-136">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2bdbf-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-138">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bdbf-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bdbf-139">RequirePasswordWhenComputerWakesOnBattery</span><span class="sxs-lookup"><span data-stu-id="2bdbf-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bdbf-142">RequirePasswordWhenComputerWakesPluggedIn</span><span class="sxs-lookup"><span data-stu-id="2bdbf-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bdbf-145">StandbyTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="2bdbf-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2bdbf-148">StandbyTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="2bdbf-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bdbf-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2bdbf-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bdbf-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2bdbf-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bdbf-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bdbf-151">Requirements</span></span>



| <span data-ttu-id="2bdbf-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bdbf-152">Requirement</span></span> | <span data-ttu-id="2bdbf-153">Valor</span><span class="sxs-lookup"><span data-stu-id="2bdbf-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bdbf-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bdbf-154">Minimum supported client</span></span><br/> | <span data-ttu-id="2bdbf-155">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2bdbf-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bdbf-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2bdbf-156">Minimum supported server</span></span><br/> | <span data-ttu-id="2bdbf-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2bdbf-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2bdbf-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="2bdbf-158">Namespace</span></span><br/>                | <span data-ttu-id="2bdbf-159">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2bdbf-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2bdbf-160">MOF</span><span class="sxs-lookup"><span data-stu-id="2bdbf-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bdbf-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bdbf-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bdbf-162">DLL</span><span class="sxs-lookup"><span data-stu-id="2bdbf-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bdbf-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bdbf-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

