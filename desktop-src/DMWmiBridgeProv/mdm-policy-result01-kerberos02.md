---
title: Classe MDM_Policy_Result01_Kerberos02
description: A \_ classe MDM Policy \_ Result01 \_ Kerberos02 representa as políticas de Kerberos.
ms.assetid: a628272d-723f-491a-a6a1-70514e5096ef
keywords:
- Classe MDM_Policy_Result01_Kerberos02
- Classe MDM_Policy_Result01_Kerberos02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Kerberos02
- MDM_Policy_Result01_Kerberos02.InstanceID
- MDM_Policy_Result01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713d7747fe45fa72cb7dcf44a02aa57526161c17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455000"
---
# <a name="mdm_policy_result01_kerberos02-class"></a><span data-ttu-id="90f05-105">\_Classe MDM \_ Result01 \_ Kerberos02</span><span class="sxs-lookup"><span data-stu-id="90f05-105">MDM\_Policy\_Result01\_Kerberos02 class</span></span>

<span data-ttu-id="90f05-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="90f05-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="90f05-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="90f05-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="90f05-108">A \_ classe MDM Policy \_ Result01 \_ Kerberos02 representa as políticas de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="90f05-108">The MDM\_Policy\_Result01\_Kerberos02 class represents the Kerberos policies.</span></span>

<span data-ttu-id="90f05-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="90f05-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="90f05-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90f05-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a><span data-ttu-id="90f05-111">Membros</span><span class="sxs-lookup"><span data-stu-id="90f05-111">Members</span></span>

<span data-ttu-id="90f05-112">A **classe \_ \_ Result01 \_ Kerberos02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="90f05-112">The **MDM\_Policy\_Result01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="90f05-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="90f05-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90f05-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="90f05-114">Properties</span></span>

<span data-ttu-id="90f05-115">A **classe \_ \_ Result01 \_ Kerberos02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="90f05-115">The **MDM\_Policy\_Result01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="90f05-116">AllowForestSearchOrder</span><span class="sxs-lookup"><span data-stu-id="90f05-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f05-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90f05-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90f05-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="90f05-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90f05-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="90f05-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f05-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90f05-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90f05-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90f05-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90f05-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90f05-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90f05-123">KerberosClientSupportsClaimsCompoundArmor</span><span class="sxs-lookup"><span data-stu-id="90f05-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f05-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90f05-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90f05-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="90f05-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="90f05-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="90f05-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f05-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90f05-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90f05-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="90f05-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90f05-129">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="90f05-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90f05-130">RequireKerberosArmoring</span><span class="sxs-lookup"><span data-stu-id="90f05-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f05-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90f05-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90f05-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="90f05-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90f05-133">RequireStrictKDCValidation</span><span class="sxs-lookup"><span data-stu-id="90f05-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f05-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90f05-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90f05-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="90f05-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="90f05-136">SetMaximumContextTokenSize</span><span class="sxs-lookup"><span data-stu-id="90f05-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="90f05-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="90f05-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90f05-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="90f05-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="90f05-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90f05-139">Requirements</span></span>



| <span data-ttu-id="90f05-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="90f05-140">Requirement</span></span> | <span data-ttu-id="90f05-141">Valor</span><span class="sxs-lookup"><span data-stu-id="90f05-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90f05-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90f05-142">Minimum supported client</span></span><br/> | <span data-ttu-id="90f05-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="90f05-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="90f05-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90f05-144">Minimum supported server</span></span><br/> | <span data-ttu-id="90f05-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="90f05-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="90f05-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="90f05-146">Namespace</span></span><br/>                | <span data-ttu-id="90f05-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="90f05-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="90f05-148">MOF</span><span class="sxs-lookup"><span data-stu-id="90f05-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90f05-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90f05-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="90f05-150">DLL</span><span class="sxs-lookup"><span data-stu-id="90f05-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90f05-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90f05-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

