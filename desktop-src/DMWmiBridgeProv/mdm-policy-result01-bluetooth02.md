---
title: Classe MDM_Policy_Result01_Bluetooth02
description: A \_ classe MDM Policy \_ Result01 \_ Bluetooth02 representa as políticas de gerenciamento de Bluetooth disponíveis.
ms.assetid: 629f2323-f6f6-4d4f-8558-9553f4dbe871
keywords:
- Classe MDM_Policy_Result01_Bluetooth02
- Classe MDM_Policy_Result01_Bluetooth02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Bluetooth02
- MDM_Policy_Result01_Bluetooth02.InstanceID
- MDM_Policy_Result01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ceb0a3b7a3d2440f9769fde72c01ce4d68c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009736"
---
# <a name="mdm_policy_result01_bluetooth02-class"></a><span data-ttu-id="a232e-105">\_Classe MDM \_ Result01 \_ Bluetooth02</span><span class="sxs-lookup"><span data-stu-id="a232e-105">MDM\_Policy\_Result01\_Bluetooth02 class</span></span>

<span data-ttu-id="a232e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="a232e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a232e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="a232e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a232e-108">A classe **MDM \_ Policy \_ Result01 \_ Bluetooth02** representa as políticas de gerenciamento de Bluetooth disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a232e-108">The **MDM\_Policy\_Result01\_Bluetooth02** class represents the Bluetooth management policies available.</span></span>

<span data-ttu-id="a232e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a232e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a232e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a232e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Bluetooth02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiscoverableMode;
  string LocalDeviceName;
  sint32 AllowAdvertising;
  string ServicesAllowedList;
  sint32 AllowPrepairing;
};
```

## <a name="members"></a><span data-ttu-id="a232e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="a232e-111">Members</span></span>

<span data-ttu-id="a232e-112">A **classe \_ \_ Result01 \_ Bluetooth02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a232e-112">The **MDM\_Policy\_Result01\_Bluetooth02** class has these types of members:</span></span>

-   [<span data-ttu-id="a232e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a232e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a232e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a232e-114">Properties</span></span>

<span data-ttu-id="a232e-115">A **classe \_ \_ Result01 \_ Bluetooth02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a232e-115">The **MDM\_Policy\_Result01\_Bluetooth02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a232e-116">AllowAdvertising</span><span class="sxs-lookup"><span data-stu-id="a232e-116">AllowAdvertising</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a232e-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a232e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a232e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a232e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a232e-119">AllowDiscoverableMode</span><span class="sxs-lookup"><span data-stu-id="a232e-119">AllowDiscoverableMode</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a232e-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a232e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a232e-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a232e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a232e-122">AllowPrepairing</span><span class="sxs-lookup"><span data-stu-id="a232e-122">AllowPrepairing</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a232e-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a232e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a232e-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a232e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a232e-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a232e-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a232e-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a232e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a232e-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a232e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a232e-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a232e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a232e-129">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="a232e-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="a232e-130">Para essa classe, a cadeia de caracteres é "Bluetooth".</span><span class="sxs-lookup"><span data-stu-id="a232e-130">For this class, the string is "Bluetooth".</span></span>

</dd> <dt>

[<span data-ttu-id="a232e-131">LocalDeviceName</span><span class="sxs-lookup"><span data-stu-id="a232e-131">LocalDeviceName</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a232e-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a232e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a232e-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a232e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a232e-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a232e-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a232e-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a232e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a232e-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a232e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a232e-137">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a232e-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a232e-138">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="a232e-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="a232e-139">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="a232e-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="a232e-140">ServicesAllowedList</span><span class="sxs-lookup"><span data-stu-id="a232e-140">ServicesAllowedList</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a232e-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a232e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a232e-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a232e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a232e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a232e-143">Requirements</span></span>



| <span data-ttu-id="a232e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="a232e-144">Requirement</span></span> | <span data-ttu-id="a232e-145">Valor</span><span class="sxs-lookup"><span data-stu-id="a232e-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a232e-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a232e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a232e-147">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a232e-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a232e-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a232e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a232e-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a232e-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a232e-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="a232e-150">Namespace</span></span><br/>                | <span data-ttu-id="a232e-151">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="a232e-151">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a232e-152">MOF</span><span class="sxs-lookup"><span data-stu-id="a232e-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a232e-153"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a232e-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a232e-154">DLL</span><span class="sxs-lookup"><span data-stu-id="a232e-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a232e-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a232e-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a232e-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="a232e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a232e-157">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="a232e-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

