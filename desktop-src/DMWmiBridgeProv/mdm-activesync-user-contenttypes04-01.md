---
title: Classe MDM_ActiveSync_User_ContentTypes04_01
description: A \_ \_ classe ContentTypes04 01 do usuário do MDM ActiveSync \_ \_ define o tipo de conteúdo a ser habilitado/desabilitado individualmente para sincronização.
ms.assetid: 82759cf9-ea2a-4d75-bb07-6832c3005074
keywords:
- Classe MDM_ActiveSync_User_ContentTypes04_01
- Classe MDM_ActiveSync_User_ContentTypes04_01, descrita
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_ContentTypes04_01
- MDM_ActiveSync_User_ContentTypes04_01.InstanceID
- MDM_ActiveSync_User_ContentTypes04_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef158daf25c6dc1c084966673f71c5907c4df1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749297"
---
# <a name="mdm_activesync_user_contenttypes04_01-class"></a><span data-ttu-id="7ad4a-105">\_ \_ \_ Classe ContentTypes04 01 do \_ usuário do MDM ActiveSync</span><span class="sxs-lookup"><span data-stu-id="7ad4a-105">MDM\_ActiveSync\_User\_ContentTypes04\_01 class</span></span>

<span data-ttu-id="7ad4a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7ad4a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ad4a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7ad4a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ad4a-108">A **classe \_ \_ \_ ContentTypes04 \_ 01 do usuário do MDM ActiveSync** define o tipo de conteúdo a ser habilitado/desabilitado individualmente para sincronização.</span><span class="sxs-lookup"><span data-stu-id="7ad4a-108">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class defines the type of content to be individually enabled/disabled for sync.</span></span>

<span data-ttu-id="7ad4a-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7ad4a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad4a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ad4a-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_ContentTypes04_01
{
  string InstanceID;
  string ParentID;
  string Enabled;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="7ad4a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7ad4a-111">Members</span></span>

<span data-ttu-id="7ad4a-112">A **classe \_ \_ \_ ContentTypes04 \_ 01 do usuário do MDM ActiveSync** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7ad4a-112">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="7ad4a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7ad4a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ad4a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7ad4a-114">Properties</span></span>

<span data-ttu-id="7ad4a-115">A classe **MDM \_ ActiveSync \_ user \_ ContentTypes04 \_ 01** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7ad4a-115">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7ad4a-116">Enabled</span><span class="sxs-lookup"><span data-stu-id="7ad4a-116">Enabled</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ad4a-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7ad4a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ad4a-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ad4a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ad4a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ad4a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ad4a-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7ad4a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ad4a-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7ad4a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ad4a-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ad4a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ad4a-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="7ad4a-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="7ad4a-124">Nome</span><span class="sxs-lookup"><span data-stu-id="7ad4a-124">Name</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ad4a-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7ad4a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ad4a-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ad4a-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ad4a-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7ad4a-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ad4a-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7ad4a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ad4a-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7ad4a-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ad4a-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ad4a-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ad4a-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="7ad4a-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="7ad4a-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/opties"</span><span class="sxs-lookup"><span data-stu-id="7ad4a-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ad4a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ad4a-133">Requirements</span></span>



| <span data-ttu-id="7ad4a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ad4a-134">Requirement</span></span> | <span data-ttu-id="7ad4a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="7ad4a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad4a-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ad4a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7ad4a-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7ad4a-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ad4a-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ad4a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7ad4a-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7ad4a-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7ad4a-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ad4a-140">Namespace</span></span><br/>                | <span data-ttu-id="7ad4a-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7ad4a-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7ad4a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7ad4a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ad4a-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ad4a-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ad4a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7ad4a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ad4a-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ad4a-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ad4a-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ad4a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad4a-147">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="7ad4a-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

