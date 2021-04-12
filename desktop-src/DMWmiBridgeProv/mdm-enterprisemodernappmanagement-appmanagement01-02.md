---
title: Classe MDM_EnterpriseModernAppManagement_AppManagement01_02
description: A \_ classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 02 especifica se você deseja impedir que um aplicativo específico seja atualizado por meio de atualizações automáticas.
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_02
- Classe MDM_EnterpriseModernAppManagement_AppManagement01_02, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11441e8700d10bc7b0d5bebd31c002802a857417
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455594"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a><span data-ttu-id="bbe8a-105">\_Classe MDM EnterpriseModernAppManagement \_ AppManagement01 \_ 02</span><span class="sxs-lookup"><span data-stu-id="bbe8a-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_02 class</span></span>

<span data-ttu-id="bbe8a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="bbe8a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bbe8a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="bbe8a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bbe8a-108">A classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** especifica se você deseja impedir que um aplicativo específico seja atualizado por meio de atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="bbe8a-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class specifies whether you want to block a specific app from being updated via auto-updates.</span></span>

<span data-ttu-id="bbe8a-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bbe8a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe8a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbe8a-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a><span data-ttu-id="bbe8a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="bbe8a-111">Members</span></span>

<span data-ttu-id="bbe8a-112">A classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bbe8a-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these types of members:</span></span>

-   [<span data-ttu-id="bbe8a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bbe8a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbe8a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bbe8a-114">Properties</span></span>

<span data-ttu-id="bbe8a-115">A classe **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bbe8a-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bbe8a-116">DoNotUpdate</span><span class="sxs-lookup"><span data-stu-id="bbe8a-116">DoNotUpdate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe8a-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bbe8a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbe8a-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bbe8a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bbe8a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bbe8a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe8a-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bbe8a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe8a-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bbe8a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe8a-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bbe8a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bbe8a-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="bbe8a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="bbe8a-124">Para essa classe, a cadeia de caracteres é a instância do nome da família de pacotes.</span><span class="sxs-lookup"><span data-stu-id="bbe8a-124">For this class, the string is the instance of the package family name.</span></span>

</dd> <dt>

<span data-ttu-id="bbe8a-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bbe8a-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbe8a-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bbe8a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbe8a-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bbe8a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbe8a-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bbe8a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bbe8a-129">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="bbe8a-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="bbe8a-130">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*enterpriseid*"</span><span class="sxs-lookup"><span data-stu-id="bbe8a-130">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bbe8a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbe8a-131">Requirements</span></span>



| <span data-ttu-id="bbe8a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbe8a-132">Requirement</span></span> | <span data-ttu-id="bbe8a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="bbe8a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe8a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbe8a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe8a-135">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bbe8a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bbe8a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bbe8a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe8a-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bbe8a-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bbe8a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="bbe8a-138">Namespace</span></span><br/>                | <span data-ttu-id="bbe8a-139">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="bbe8a-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bbe8a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bbe8a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbe8a-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbe8a-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbe8a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bbe8a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbe8a-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbe8a-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbe8a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbe8a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbe8a-145">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="bbe8a-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

