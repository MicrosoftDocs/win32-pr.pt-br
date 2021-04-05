---
title: Classe MDM_Policy_Result01_DeviceInstallation02
description: A \_ classe MDM Policy \_ Result01 \_ DeviceInstallation02 representa as políticas de instalação de dispositivo disponíveis.
ms.assetid: a5c89661-16f1-42e7-a11d-2c3a7945dac3
keywords:
- Classe MDM_Policy_Result01_DeviceInstallation02
- Classe MDM_Policy_Result01_DeviceInstallation02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceInstallation02
- MDM_Policy_Result01_DeviceInstallation02.InstanceID
- MDM_Policy_Result01_DeviceInstallation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6ec11cbfc5b0b38aa5e7482507108204b8798d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918157"
---
# <a name="mdm_policy_result01_deviceinstallation02-class"></a><span data-ttu-id="09cb4-105">\_Classe MDM \_ Result01 \_ DeviceInstallation02</span><span class="sxs-lookup"><span data-stu-id="09cb4-105">MDM\_Policy\_Result01\_DeviceInstallation02 class</span></span>

<span data-ttu-id="09cb4-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="09cb4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="09cb4-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="09cb4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="09cb4-108">A \_ classe MDM Policy \_ Result01 \_ DeviceInstallation02 representa as políticas de instalação de dispositivo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="09cb4-108">The MDM\_Policy\_Result01\_DeviceInstallation02 class represents the available device installation policies.</span></span>

<span data-ttu-id="09cb4-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="09cb4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09cb4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09cb4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceInstallation02
{
  string InstanceID;
  string ParentID;
  string PreventInstallationOfMatchingDeviceIDs;
  string PreventInstallationOfMatchingDeviceSetupClasses;
};
```

## <a name="members"></a><span data-ttu-id="09cb4-111">Membros</span><span class="sxs-lookup"><span data-stu-id="09cb4-111">Members</span></span>

<span data-ttu-id="09cb4-112">A **classe \_ \_ Result01 \_ DeviceInstallation02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="09cb4-112">The **MDM\_Policy\_Result01\_DeviceInstallation02** class has these types of members:</span></span>

-   [<span data-ttu-id="09cb4-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09cb4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09cb4-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09cb4-114">Properties</span></span>

<span data-ttu-id="09cb4-115">A **classe \_ \_ Result01 \_ DeviceInstallation02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="09cb4-115">The **MDM\_Policy\_Result01\_DeviceInstallation02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09cb4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09cb4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09cb4-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09cb4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09cb4-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09cb4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09cb4-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09cb4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="09cb4-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="09cb4-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09cb4-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09cb4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09cb4-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="09cb4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09cb4-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="09cb4-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09cb4-124">PreventInstallationOfMatchingDeviceIDs</span><span class="sxs-lookup"><span data-stu-id="09cb4-124">PreventInstallationOfMatchingDeviceIDs</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdeviceids)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09cb4-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09cb4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09cb4-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="09cb4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="09cb4-127">PreventInstallationOfMatchingDeviceSetupClasses</span><span class="sxs-lookup"><span data-stu-id="09cb4-127">PreventInstallationOfMatchingDeviceSetupClasses</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdevicesetupclasses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="09cb4-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="09cb4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09cb4-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="09cb4-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09cb4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09cb4-130">Requirements</span></span>



| <span data-ttu-id="09cb4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="09cb4-131">Requirement</span></span> | <span data-ttu-id="09cb4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="09cb4-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09cb4-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09cb4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="09cb4-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="09cb4-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09cb4-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09cb4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="09cb4-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="09cb4-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="09cb4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="09cb4-137">Namespace</span></span><br/>                | <span data-ttu-id="09cb4-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="09cb4-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="09cb4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="09cb4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09cb4-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09cb4-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="09cb4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="09cb4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09cb4-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09cb4-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

