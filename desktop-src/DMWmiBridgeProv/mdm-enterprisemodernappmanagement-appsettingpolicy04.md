---
title: Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
description: A \_ classe MDM EnterpriseModernAppManagement \_ AppSettingPolicy04 especifica todos os valores de configuração de aplicativo gerenciado.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- Classe MDM_EnterpriseModernAppManagement_AppSettingPolicy04, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9003ea7c9106f177958f7a15def3c60393346b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009592"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a><span data-ttu-id="96da6-105">\_ \_ Classe APPSETTINGPOLICY04 do MDM EnterpriseModernAppManagement</span><span class="sxs-lookup"><span data-stu-id="96da6-105">MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04 class</span></span>

<span data-ttu-id="96da6-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="96da6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="96da6-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="96da6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="96da6-108">A classe **MDM \_ EnterpriseModernAppManagement \_ AppSettingPolicy04** especifica todos os valores de configuração de aplicativo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="96da6-108">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class specifies all managed app setting values.</span></span>

<span data-ttu-id="96da6-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="96da6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="96da6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96da6-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a><span data-ttu-id="96da6-111">Membros</span><span class="sxs-lookup"><span data-stu-id="96da6-111">Members</span></span>

<span data-ttu-id="96da6-112">A **classe \_ \_ AppSettingPolicy04 de MDM EnterpriseModernAppManagement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="96da6-112">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these types of members:</span></span>

-   [<span data-ttu-id="96da6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="96da6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96da6-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="96da6-114">Properties</span></span>

<span data-ttu-id="96da6-115">A **classe \_ \_ AppSettingPolicy04 do MDM EnterpriseModernAppManagement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="96da6-115">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96da6-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="96da6-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96da6-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96da6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96da6-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96da6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96da6-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="96da6-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="96da6-120">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="96da6-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="96da6-121">Para essa classe, a cadeia de caracteres "AppSettingPolicy".</span><span class="sxs-lookup"><span data-stu-id="96da6-121">For this class, the string "AppSettingPolicy".</span></span>

</dd> <dt>

[<span data-ttu-id="96da6-122">IsVariableLeaf</span><span class="sxs-lookup"><span data-stu-id="96da6-122">IsVariableLeaf</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="96da6-123">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="96da6-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="96da6-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96da6-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96da6-125">Adicionado no Windows 10, versão 1511.</span><span class="sxs-lookup"><span data-stu-id="96da6-125">Added in Windows 10, version 1511.</span></span> <span data-ttu-id="96da6-126">O **configurador** e os dados representam um par chave-valor a ser configurado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96da6-126">The **SettingValue** and data represent a key value pair to be configured for the app.</span></span> <span data-ttu-id="96da6-127">O nó representa o nome da chave e os dados representam o valor.</span><span class="sxs-lookup"><span data-stu-id="96da6-127">The node represents the name of the key and the data represents the value.</span></span> <span data-ttu-id="96da6-128">Você pode encontrar esse valor em LocalSettings no contêiner Managed. app. Settings.</span><span class="sxs-lookup"><span data-stu-id="96da6-128">You can find this value in LocalSettings in the Managed.App.Settings container.</span></span>

<span data-ttu-id="96da6-129">Essa configuração só funciona para aplicativos que dão suporte ao recurso e só tem suporte no contexto do usuário.</span><span class="sxs-lookup"><span data-stu-id="96da6-129">This setting only works for apps that support the feature and it is only supported in the user context.</span></span>

</dd> <dt>

<span data-ttu-id="96da6-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="96da6-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96da6-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96da6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96da6-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="96da6-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96da6-133">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="96da6-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="96da6-134">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="96da6-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="96da6-135">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"</span><span class="sxs-lookup"><span data-stu-id="96da6-135">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="96da6-136">**Valor**</span><span class="sxs-lookup"><span data-stu-id="96da6-136">**Value**</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="96da6-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="96da6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96da6-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="96da6-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96da6-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96da6-139">Requirements</span></span>



| <span data-ttu-id="96da6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="96da6-140">Requirement</span></span> | <span data-ttu-id="96da6-141">Valor</span><span class="sxs-lookup"><span data-stu-id="96da6-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96da6-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96da6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="96da6-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="96da6-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96da6-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96da6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="96da6-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="96da6-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="96da6-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="96da6-146">Namespace</span></span><br/>                | <span data-ttu-id="96da6-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="96da6-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="96da6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="96da6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96da6-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96da6-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="96da6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="96da6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96da6-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96da6-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96da6-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="96da6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96da6-153">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="96da6-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

