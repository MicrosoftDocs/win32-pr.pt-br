---
title: Classe MDM_AssignedAccess
description: A \_ classe MDM AssignedAccess é usada para definir o dispositivo a ser executado no modo de quiosque.
ms.assetid: b9837f91-3c13-4a80-bf6d-66d8b53dfa70
keywords:
- Classe MDM_AssignedAccess
- Classe MDM_AssignedAccess, descrita
topic_type:
- apiref
api_name:
- MDM_AssignedAccess
- MDM_AssignedAccess.InstanceID
- MDM_AssignedAccess.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5f03f99183400d4e7672323072415918e8e58e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455932"
---
# <a name="mdm_assignedaccess-class"></a><span data-ttu-id="84272-105">\_Classe AssignedAccess do MDM</span><span class="sxs-lookup"><span data-stu-id="84272-105">MDM\_AssignedAccess class</span></span>

<span data-ttu-id="84272-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="84272-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="84272-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="84272-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="84272-108">A classe **MDM \_ AssignedAccess** é usada para definir o dispositivo a ser executado no modo de quiosque.</span><span class="sxs-lookup"><span data-stu-id="84272-108">The **MDM\_AssignedAccess** class is used to set the device to run in kiosk mode.</span></span> <span data-ttu-id="84272-109">Depois que a classe tiver sido executada, o próximo logon de usuário associado ao modo de quiosque colocará o dispositivo no modo de quiosque que executa o aplicativo especificado no pacote de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="84272-109">Once the class has been executed, then the next user login that is associated with the kiosk mode puts the device in the kiosk mode running the application specified in the provisioning package.</span></span>

<span data-ttu-id="84272-110">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="84272-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84272-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84272-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AssignedAccess
{
  string InstanceID;
  string ParentID;
  string KioskModeApp;
  string Configuration;
};
```

## <a name="members"></a><span data-ttu-id="84272-112">Membros</span><span class="sxs-lookup"><span data-stu-id="84272-112">Members</span></span>

<span data-ttu-id="84272-113">A classe **MDM \_ AssignedAccess** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="84272-113">The **MDM\_AssignedAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="84272-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="84272-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84272-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="84272-115">Properties</span></span>

<span data-ttu-id="84272-116">A classe **MDM \_ AssignedAccess** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="84272-116">The **MDM\_AssignedAccess** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="84272-117">Configuration</span><span class="sxs-lookup"><span data-stu-id="84272-117">Configuration</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84272-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="84272-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84272-119">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="84272-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84272-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84272-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84272-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="84272-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84272-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="84272-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84272-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84272-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84272-124">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="84272-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="84272-125">Para essa classe, a cadeia de caracteres é "AssignedAccess".</span><span class="sxs-lookup"><span data-stu-id="84272-125">For this class, the string is "AssignedAccess".</span></span>

</dd> <dt>

[<span data-ttu-id="84272-126">KioskModeApp</span><span class="sxs-lookup"><span data-stu-id="84272-126">KioskModeApp</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-kioskmodeapp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="84272-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="84272-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84272-128">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="84272-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="84272-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="84272-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84272-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="84272-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84272-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="84272-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84272-132">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="84272-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="84272-133">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="84272-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="84272-134">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="84272-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84272-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84272-135">Requirements</span></span>



| <span data-ttu-id="84272-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="84272-136">Requirement</span></span> | <span data-ttu-id="84272-137">Valor</span><span class="sxs-lookup"><span data-stu-id="84272-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84272-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84272-138">Minimum supported client</span></span><br/> | <span data-ttu-id="84272-139">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="84272-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84272-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84272-140">Minimum supported server</span></span><br/> | <span data-ttu-id="84272-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="84272-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="84272-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="84272-142">Namespace</span></span><br/>                | <span data-ttu-id="84272-143">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="84272-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="84272-144">MOF</span><span class="sxs-lookup"><span data-stu-id="84272-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84272-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84272-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="84272-146">DLL</span><span class="sxs-lookup"><span data-stu-id="84272-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84272-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84272-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84272-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="84272-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84272-149">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="84272-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

