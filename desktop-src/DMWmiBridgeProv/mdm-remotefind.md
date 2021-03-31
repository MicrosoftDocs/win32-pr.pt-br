---
title: Classe MDM_RemoteFind
description: A \_ classe MDM RemoteFind recupera as informações de local de um dispositivo específico.
ms.assetid: 8dfbe951-b4ca-4709-bec9-0821571f9b0e
keywords:
- Classe MDM_RemoteFind
- Classe MDM_RemoteFind, descrita
topic_type:
- apiref
api_name:
- MDM_RemoteFind
- MDM_RemoteFind.InstanceID
- MDM_RemoteFind.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8930d80ede9daad5c721cd3b226c85e3d9918a19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644293"
---
# <a name="mdm_remotefind-class"></a><span data-ttu-id="2900e-105">\_Classe RemoteFind do MDM</span><span class="sxs-lookup"><span data-stu-id="2900e-105">MDM\_RemoteFind class</span></span>

<span data-ttu-id="2900e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2900e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2900e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2900e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2900e-108">A classe **MDM \_ RemoteFind** recupera as informações de local de um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="2900e-108">The **MDM\_RemoteFind** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="2900e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2900e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2900e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2900e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind
{
  string InstanceID;
  string ParentID;
  sint32 DesiredAccuracy;
  sint32 MaximumAge;
  sint32 Timeout;
};
```

## <a name="members"></a><span data-ttu-id="2900e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2900e-111">Members</span></span>

<span data-ttu-id="2900e-112">A classe **MDM \_ RemoteFind** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2900e-112">The **MDM\_RemoteFind** class has these types of members:</span></span>

-   [<span data-ttu-id="2900e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2900e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2900e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2900e-114">Properties</span></span>

<span data-ttu-id="2900e-115">A classe **MDM \_ RemoteFind** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2900e-115">The **MDM\_RemoteFind** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2900e-116">DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="2900e-116">DesiredAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#desiredaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2900e-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2900e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2900e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2900e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2900e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2900e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2900e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2900e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2900e-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2900e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2900e-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2900e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2900e-123">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="2900e-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="2900e-124">Para essa classe, a cadeia de caracteres é "RemoteFind".</span><span class="sxs-lookup"><span data-stu-id="2900e-124">For this class, the string is "RemoteFind".</span></span>

</dd> <dt>

[<span data-ttu-id="2900e-125">Máximo de</span><span class="sxs-lookup"><span data-stu-id="2900e-125">MaximumAge</span></span>](/windows/client-management/mdm/remotefind-csp#maximumage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2900e-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2900e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2900e-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2900e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2900e-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2900e-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2900e-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2900e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2900e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2900e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2900e-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2900e-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2900e-132">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="2900e-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="2900e-133">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="2900e-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="2900e-134">Tempo Limite</span><span class="sxs-lookup"><span data-stu-id="2900e-134">Timeout</span></span>](/windows/client-management/mdm/remotefind-csp#timeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2900e-135">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2900e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2900e-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2900e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2900e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2900e-137">Requirements</span></span>



| <span data-ttu-id="2900e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2900e-138">Requirement</span></span> | <span data-ttu-id="2900e-139">Valor</span><span class="sxs-lookup"><span data-stu-id="2900e-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2900e-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2900e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2900e-141">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2900e-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2900e-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2900e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2900e-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2900e-143">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="2900e-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="2900e-144">Namespace</span></span><br/>                | <span data-ttu-id="2900e-145">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2900e-145">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                              |
| <span data-ttu-id="2900e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="2900e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2900e-147"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2900e-147"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="2900e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2900e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2900e-149"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2900e-149"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2900e-150">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2900e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2900e-151">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="2900e-151">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

