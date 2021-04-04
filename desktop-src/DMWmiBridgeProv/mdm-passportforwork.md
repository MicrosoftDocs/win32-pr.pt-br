---
title: Classe MDM_PassportForWork
description: O PassportForWork de MDM \_ é usado para provisionar o Windows Hello para empresas.
ms.assetid: 49bba780-e26f-463d-97ae-e095ea16be87
keywords:
- Classe MDM_PassportForWork
- Classe MDM_PassportForWork, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork
- MDM_PassportForWork.InstanceID
- MDM_PassportForWork.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7f061c0ab8f0405e8f0e6a6d43d8d896c62f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009183"
---
# <a name="mdm_passportforwork-class"></a><span data-ttu-id="80fd7-105">\_Classe PassportForWork do MDM</span><span class="sxs-lookup"><span data-stu-id="80fd7-105">MDM\_PassportForWork class</span></span>

<span data-ttu-id="80fd7-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="80fd7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="80fd7-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="80fd7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="80fd7-108">O **\_ PassportForWork de MDM** é usado para provisionar o Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="80fd7-108">The **MDM\_PassportForWork** is used to provision Windows Hello for Business.</span></span>

<span data-ttu-id="80fd7-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="80fd7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="80fd7-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80fd7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
};
```

## <a name="members"></a><span data-ttu-id="80fd7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="80fd7-111">Members</span></span>

<span data-ttu-id="80fd7-112">A classe **MDM \_ PassportForWork** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="80fd7-112">The **MDM\_PassportForWork** class has these types of members:</span></span>

-   [<span data-ttu-id="80fd7-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80fd7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80fd7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80fd7-114">Properties</span></span>

<span data-ttu-id="80fd7-115">A classe **MDM \_ PassportForWork** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="80fd7-115">The **MDM\_PassportForWork** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80fd7-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="80fd7-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fd7-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="80fd7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80fd7-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80fd7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80fd7-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80fd7-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80fd7-120">Especifica a ID do locatário no formato de um GUID (identificador global exclusivo) sem chaves ({,}), que será usado como parte do gerenciamento e provisionamento do Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="80fd7-120">Specifies the Tenant ID in the format of a Globally Unique Identifier (GUID) without curly braces ( { , } ), which will be used as part of Windows Hello for Business provisioning and management.</span></span>

</dd> <dt>

<span data-ttu-id="80fd7-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="80fd7-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fd7-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="80fd7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80fd7-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="80fd7-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80fd7-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="80fd7-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="80fd7-125">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="80fd7-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="80fd7-126">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/PassPortForWork/"</span><span class="sxs-lookup"><span data-stu-id="80fd7-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="80fd7-127">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="80fd7-127">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="80fd7-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="80fd7-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80fd7-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="80fd7-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80fd7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80fd7-130">Requirements</span></span>



| <span data-ttu-id="80fd7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="80fd7-131">Requirement</span></span> | <span data-ttu-id="80fd7-132">Valor</span><span class="sxs-lookup"><span data-stu-id="80fd7-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80fd7-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80fd7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="80fd7-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="80fd7-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80fd7-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80fd7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="80fd7-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="80fd7-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="80fd7-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="80fd7-137">Namespace</span></span><br/>                | <span data-ttu-id="80fd7-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="80fd7-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="80fd7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="80fd7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80fd7-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80fd7-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="80fd7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="80fd7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80fd7-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80fd7-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80fd7-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="80fd7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fd7-144">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="80fd7-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

