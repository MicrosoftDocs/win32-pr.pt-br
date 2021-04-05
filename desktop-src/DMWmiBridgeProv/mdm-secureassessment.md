---
title: Classe MDM_SecureAssessment
description: O SecureAssessmentclass de MDM \_ é usado para fornecer informações de configuração para o navegador de avaliação segura.
ms.assetid: ad456f01-c77d-428b-a8bf-03e9ae106e60
keywords:
- Classe MDM_SecureAssessment
- Classe MDM_SecureAssessment, descrita
topic_type:
- apiref
api_name:
- MDM_SecureAssessment
- MDM_SecureAssessment.InstanceID
- MDM_SecureAssessment.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deef2c8ee832a54775ae9dd51d85414a607ca8b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918018"
---
# <a name="mdm_secureassessment-class"></a><span data-ttu-id="5d937-105">\_Classe SecureAssessment do MDM</span><span class="sxs-lookup"><span data-stu-id="5d937-105">MDM\_SecureAssessment class</span></span>

<span data-ttu-id="5d937-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="5d937-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5d937-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="5d937-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5d937-108">A classe **MDM \_ SecureAssessment** é usada para fornecer informações de configuração para o navegador de avaliação segura.</span><span class="sxs-lookup"><span data-stu-id="5d937-108">The **MDM\_SecureAssessment** class is used to provide configuration information for the secure assessment browser.</span></span>

<span data-ttu-id="5d937-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5d937-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d937-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d937-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SecureAssessment
{
  string  InstanceID;
  string  ParentID;
  string  LaunchURI;
  string  TesterAccount;
  boolean AllowTextSuggestions;
  boolean RequirePrinting;
  boolean AllowScreenMonitoring;
};
```

## <a name="members"></a><span data-ttu-id="5d937-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5d937-111">Members</span></span>

<span data-ttu-id="5d937-112">A classe **MDM \_ SecureAssessment** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d937-112">The **MDM\_SecureAssessment** class has these types of members:</span></span>

-   [<span data-ttu-id="5d937-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d937-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d937-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d937-114">Properties</span></span>

<span data-ttu-id="5d937-115">A classe **MDM \_ SecureAssessment** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d937-115">The **MDM\_SecureAssessment** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5d937-116">AllowScreenMonitoring</span><span class="sxs-lookup"><span data-stu-id="5d937-116">AllowScreenMonitoring</span></span>](/windows/client-management/mdm/secureassessment-csp#allowscreenmonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d937-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d937-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d937-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5d937-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5d937-119">AllowTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="5d937-119">AllowTextSuggestions</span></span>](/windows/client-management/mdm/secureassessment-csp#AllowTextSuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d937-120">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d937-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d937-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5d937-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5d937-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5d937-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d937-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d937-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d937-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d937-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d937-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5d937-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5d937-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="5d937-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="5d937-127">Para essa classe, a cadeia de caracteres é "SecureAssessment".</span><span class="sxs-lookup"><span data-stu-id="5d937-127">For this class, the string is "SecureAssessment".</span></span>

</dd> <dt>

[<span data-ttu-id="5d937-128">LaunchURI</span><span class="sxs-lookup"><span data-stu-id="5d937-128">LaunchURI</span></span>](/windows/client-management/mdm/secureassessment-csp#launchuri)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d937-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d937-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d937-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5d937-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5d937-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5d937-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d937-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d937-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d937-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d937-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d937-134">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5d937-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5d937-135">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="5d937-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="5d937-136">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="5d937-136">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="5d937-137">RequirePrinting</span><span class="sxs-lookup"><span data-stu-id="5d937-137">RequirePrinting</span></span>](/windows/client-management/mdm/secureassessment-csp#requireprinting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d937-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5d937-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d937-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5d937-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5d937-140">TesterAccount</span><span class="sxs-lookup"><span data-stu-id="5d937-140">TesterAccount</span></span>](/windows/client-management/mdm/secureassessment-csp#testeraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d937-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5d937-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d937-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5d937-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d937-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d937-143">Requirements</span></span>



| <span data-ttu-id="5d937-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d937-144">Requirement</span></span> | <span data-ttu-id="5d937-145">Valor</span><span class="sxs-lookup"><span data-stu-id="5d937-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d937-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d937-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5d937-147">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5d937-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5d937-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d937-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5d937-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5d937-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="5d937-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d937-150">Namespace</span></span><br/>                | <span data-ttu-id="5d937-151">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="5d937-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="5d937-152">MOF</span><span class="sxs-lookup"><span data-stu-id="5d937-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d937-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d937-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="5d937-154">DLL</span><span class="sxs-lookup"><span data-stu-id="5d937-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d937-155"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="5d937-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

