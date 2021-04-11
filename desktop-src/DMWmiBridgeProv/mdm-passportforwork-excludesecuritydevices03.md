---
title: Classe MDM_PassportForWork_ExcludeSecurityDevices03
description: A \_ classe MDM PassportForWork \_ ExcludeSecurityDevices03 define os módulos de plataforma confiável que podem ser usados com o Windows Hello para empresas.
ms.assetid: ca8fba3a-736b-4bd3-ac93-e0d44d54798d
keywords:
- Classe MDM_PassportForWork_ExcludeSecurityDevices03
- Classe MDM_PassportForWork_ExcludeSecurityDevices03, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03.InstanceID
- MDM_PassportForWork_ExcludeSecurityDevices03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cc0374a3c313a118e5ee72791380225cc760
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009187"
---
# <a name="mdm_passportforwork_excludesecuritydevices03-class"></a><span data-ttu-id="b2600-105">\_ \_ Classe EXCLUDESECURITYDEVICES03 do MDM PassportForWork</span><span class="sxs-lookup"><span data-stu-id="b2600-105">MDM\_PassportForWork\_ExcludeSecurityDevices03 class</span></span>

<span data-ttu-id="b2600-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="b2600-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b2600-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="b2600-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b2600-108">A \_ classe MDM PassportForWork \_ ExcludeSecurityDevices03 define os módulos de plataforma confiável que podem ser usados com o Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="b2600-108">The MDM\_PassportForWork\_ExcludeSecurityDevices03 class defines the Trusted Platform Modules allowed to use with Windows Hello for Business.</span></span>

<span data-ttu-id="b2600-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b2600-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2600-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2600-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_ExcludeSecurityDevices03
{
  string  InstanceID;
  string  ParentID;
  boolean TPM12;
};
```

## <a name="members"></a><span data-ttu-id="b2600-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b2600-111">Members</span></span>

<span data-ttu-id="b2600-112">A **classe \_ \_ ExcludeSecurityDevices03 de MDM PassportForWork** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b2600-112">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these types of members:</span></span>

-   [<span data-ttu-id="b2600-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b2600-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2600-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b2600-114">Properties</span></span>

<span data-ttu-id="b2600-115">A **classe \_ \_ ExcludeSecurityDevices03 do MDM PassportForWork** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b2600-115">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2600-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b2600-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2600-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b2600-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2600-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2600-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2600-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2600-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2600-120">Nó raiz.</span><span class="sxs-lookup"><span data-stu-id="b2600-120">Root node.</span></span>

</dd> <dt>

<span data-ttu-id="b2600-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b2600-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2600-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b2600-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2600-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2600-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2600-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2600-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2600-125">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="b2600-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="b2600-126">Para obter mais informações, consulte [PASSPORTFORWORK CSP](/windows/client-management/mdm/passportforwork-csp).</span><span class="sxs-lookup"><span data-stu-id="b2600-126">For more information, see [PassportForWork CSP](/windows/client-management/mdm/passportforwork-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b2600-127">TPM12</span><span class="sxs-lookup"><span data-stu-id="b2600-127">TPM12</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2600-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b2600-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b2600-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b2600-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2600-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2600-130">Requirements</span></span>



| <span data-ttu-id="b2600-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2600-131">Requirement</span></span> | <span data-ttu-id="b2600-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b2600-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2600-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2600-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b2600-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b2600-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2600-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2600-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b2600-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b2600-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b2600-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2600-137">Namespace</span></span><br/>                | <span data-ttu-id="b2600-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="b2600-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b2600-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b2600-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2600-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2600-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2600-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b2600-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2600-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2600-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

