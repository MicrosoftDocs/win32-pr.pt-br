---
title: Classe MDM_VPNv2_PluginProfile02
description: A \_ classe MDM VPNv2 \_ PlugInProfile02 descreve as informações necessárias ao usar um plug-in de VPN baseado na Windows Store.
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- Classe MDM_VPNv2_PluginProfile02
- Classe MDM_VPNv2_PluginProfile02, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 008d60b28ec1d2cec9431cc63ac4d0c406d18060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918460"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a><span data-ttu-id="20d0f-105">\_ \_ Classe PLUGINPROFILE02 do MDM VPNv2</span><span class="sxs-lookup"><span data-stu-id="20d0f-105">MDM\_VPNv2\_PluginProfile02 class</span></span>

<span data-ttu-id="20d0f-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="20d0f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="20d0f-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="20d0f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="20d0f-108">A classe **MDM \_ VPNv2 \_ PlugInProfile02** descreve as informações necessárias ao usar um plug-in de VPN baseado na Windows Store.</span><span class="sxs-lookup"><span data-stu-id="20d0f-108">The **MDM\_VPNv2\_PlugInProfile02** class describes the information needed when using a Windows Store based VPN plugin.</span></span>

<span data-ttu-id="20d0f-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="20d0f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20d0f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20d0f-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a><span data-ttu-id="20d0f-111">Membros</span><span class="sxs-lookup"><span data-stu-id="20d0f-111">Members</span></span>

<span data-ttu-id="20d0f-112">A **classe \_ \_ PluginProfile02 de MDM VPNv2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="20d0f-112">The **MDM\_VPNv2\_PluginProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="20d0f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20d0f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20d0f-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20d0f-114">Properties</span></span>

<span data-ttu-id="20d0f-115">A **classe \_ \_ PluginProfile02 do MDM VPNv2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="20d0f-115">The **MDM\_VPNv2\_PluginProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="20d0f-116">CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="20d0f-116">CustomConfiguration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d0f-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d0f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d0f-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20d0f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="20d0f-119">CustomStoreUrl</span><span class="sxs-lookup"><span data-stu-id="20d0f-119">CustomStoreUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d0f-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d0f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d0f-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20d0f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="20d0f-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="20d0f-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d0f-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d0f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d0f-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d0f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20d0f-125">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="20d0f-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="20d0f-126">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="20d0f-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="20d0f-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="20d0f-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d0f-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d0f-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d0f-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="20d0f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20d0f-130">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="20d0f-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="20d0f-131">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="20d0f-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="20d0f-132">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="20d0f-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="20d0f-133">PluginPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="20d0f-133">PluginPackageFamilyName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d0f-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d0f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d0f-135">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20d0f-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="20d0f-136">ServerUrlList</span><span class="sxs-lookup"><span data-stu-id="20d0f-136">ServerUrlList</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="20d0f-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="20d0f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20d0f-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="20d0f-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20d0f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20d0f-139">Requirements</span></span>



| <span data-ttu-id="20d0f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="20d0f-140">Requirement</span></span> | <span data-ttu-id="20d0f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="20d0f-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20d0f-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20d0f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="20d0f-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="20d0f-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20d0f-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20d0f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="20d0f-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="20d0f-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="20d0f-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="20d0f-146">Namespace</span></span><br/>                | <span data-ttu-id="20d0f-147">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="20d0f-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="20d0f-148">MOF</span><span class="sxs-lookup"><span data-stu-id="20d0f-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20d0f-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20d0f-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="20d0f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="20d0f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20d0f-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20d0f-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20d0f-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="20d0f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20d0f-153">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="20d0f-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

