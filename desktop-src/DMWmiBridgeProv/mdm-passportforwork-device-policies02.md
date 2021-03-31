---
title: Classe MDM_PassportForWork_Device_Policies02
description: A \_ \_ classe Policies02 do dispositivo MDM PassportForWork \_ define as configurações de política do Windows Hello para empresas.
ms.assetid: 7581ea7e-0360-4695-a4ad-566df24a8841
keywords:
- Classe MDM_PassportForWork_Device_Policies02
- Classe MDM_PassportForWork_Device_Policies02, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Device_Policies02
- MDM_PassportForWork_Device_Policies02.InstanceID
- MDM_PassportForWork_Device_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66d642fb796d3b7af009197580f1eda21ab0bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918258"
---
# <a name="mdm_passportforwork_device_policies02-class"></a><span data-ttu-id="b48e7-105">\_ \_ Classe Policies02 do dispositivo MDM PassportForWork \_</span><span class="sxs-lookup"><span data-stu-id="b48e7-105">MDM\_PassportForWork\_Device\_Policies02 class</span></span>

<span data-ttu-id="b48e7-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b48e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b48e7-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b48e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b48e7-108">A **classe \_ \_ \_ Policies02 do dispositivo MDM PassportForWork** define as configurações de política do Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="b48e7-108">The **MDM\_PassportForWork\_Device\_Policies02** class defines the Windows Hello for Business policy settings.</span></span>

<span data-ttu-id="b48e7-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b48e7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b48e7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b48e7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Device_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UseCertificateForOnPremAuth;
};
```

## <a name="members"></a><span data-ttu-id="b48e7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b48e7-111">Members</span></span>

<span data-ttu-id="b48e7-112">A **classe \_ \_ \_ Policies02 do dispositivo MDM PassportForWork** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b48e7-112">The **MDM\_PassportForWork\_Device\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="b48e7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b48e7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b48e7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b48e7-114">Properties</span></span>

<span data-ttu-id="b48e7-115">A **classe \_ \_ \_ Policies02 do dispositivo MDM PassportForWork** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b48e7-115">The **MDM\_PassportForWork\_Device\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b48e7-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b48e7-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48e7-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b48e7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b48e7-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b48e7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b48e7-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b48e7-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b48e7-120">Nó para as configurações de política do Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="b48e7-120">Node for the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

<span data-ttu-id="b48e7-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b48e7-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48e7-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b48e7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b48e7-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b48e7-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b48e7-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b48e7-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b48e7-125">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="b48e7-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="b48e7-126">Para essa classe, a cadeia de caracteres é "./Device/Vendor/MSFT/PassPortForWork/*tenantid*/"</span><span class="sxs-lookup"><span data-stu-id="b48e7-126">For this class, the string is "./Device/Vendor/MSFT/PassPortForWork/*TenantID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="b48e7-127">UseCertificateForOnPremAuth</span><span class="sxs-lookup"><span data-stu-id="b48e7-127">UseCertificateForOnPremAuth</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48e7-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b48e7-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b48e7-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b48e7-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b48e7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b48e7-130">Requirements</span></span>



| <span data-ttu-id="b48e7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b48e7-131">Requirement</span></span> | <span data-ttu-id="b48e7-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b48e7-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b48e7-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b48e7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b48e7-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b48e7-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b48e7-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b48e7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b48e7-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b48e7-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b48e7-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b48e7-137">Namespace</span></span><br/>                | <span data-ttu-id="b48e7-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b48e7-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b48e7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b48e7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b48e7-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b48e7-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b48e7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b48e7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b48e7-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b48e7-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

