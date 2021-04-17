---
title: Classe MDM_RemoteFind_Location01
description: A \_ classe MDM RemoteFind \_ Location01 recupera as informações de local de um dispositivo específico.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- Classe MDM_RemoteFind_Location01
- Classe MDM_RemoteFind_Location01, descrita
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e1b46a7b4a0c3439f78f38a5fb6cd5b865275c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454670"
---
# <a name="mdm_remotefind_location01-class"></a><span data-ttu-id="3173d-105">\_ \_ Classe LOCATION01 do MDM RemoteFind</span><span class="sxs-lookup"><span data-stu-id="3173d-105">MDM\_RemoteFind\_Location01 class</span></span>

<span data-ttu-id="3173d-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="3173d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3173d-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="3173d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3173d-108">A classe **MDM \_ RemoteFind \_ Location01** recupera as informações de local de um dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="3173d-108">The **MDM\_RemoteFind\_Location01** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="3173d-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3173d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3173d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3173d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a><span data-ttu-id="3173d-111">Membros</span><span class="sxs-lookup"><span data-stu-id="3173d-111">Members</span></span>

<span data-ttu-id="3173d-112">A **classe \_ \_ Location01 de MDM RemoteFind** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3173d-112">The **MDM\_RemoteFind\_Location01** class has these types of members:</span></span>

-   [<span data-ttu-id="3173d-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3173d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3173d-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3173d-114">Properties</span></span>

<span data-ttu-id="3173d-115">A **classe \_ \_ Location01 do MDM RemoteFind** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3173d-115">The **MDM\_RemoteFind\_Location01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3173d-116">Correta</span><span class="sxs-lookup"><span data-stu-id="3173d-116">Accuracy</span></span>](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3173d-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3173d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3173d-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3173d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3173d-119">Age</span><span class="sxs-lookup"><span data-stu-id="3173d-119">Age</span></span>](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3173d-120">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3173d-120">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3173d-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3173d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3173d-122">Altitude</span><span class="sxs-lookup"><span data-stu-id="3173d-122">Altitude</span></span>](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3173d-123">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="3173d-123">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3173d-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3173d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3173d-125">AltitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="3173d-125">AltitudeAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3173d-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3173d-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3173d-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3173d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3173d-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3173d-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3173d-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3173d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3173d-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3173d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3173d-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3173d-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3173d-132">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="3173d-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="3173d-133">Para essa classe, a cadeia de caracteres é "local".</span><span class="sxs-lookup"><span data-stu-id="3173d-133">For this class, the string is "Location".</span></span>

</dd> <dt>

[<span data-ttu-id="3173d-134">Latitude</span><span class="sxs-lookup"><span data-stu-id="3173d-134">Latitude</span></span>](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3173d-135">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="3173d-135">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3173d-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3173d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3173d-137">Longitude</span><span class="sxs-lookup"><span data-stu-id="3173d-137">Longitude</span></span>](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3173d-138">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="3173d-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3173d-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3173d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3173d-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3173d-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3173d-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3173d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3173d-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3173d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3173d-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3173d-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3173d-144">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="3173d-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="3173d-145">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/RemoteFind"</span><span class="sxs-lookup"><span data-stu-id="3173d-145">For this class, the string is "./Vendor/MSFT/RemoteFind"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3173d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3173d-146">Requirements</span></span>



| <span data-ttu-id="3173d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="3173d-147">Requirement</span></span> | <span data-ttu-id="3173d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="3173d-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3173d-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3173d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3173d-150">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3173d-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3173d-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3173d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3173d-152">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3173d-152">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="3173d-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="3173d-153">Namespace</span></span><br/>                | <span data-ttu-id="3173d-154">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="3173d-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="3173d-155">MOF</span><span class="sxs-lookup"><span data-stu-id="3173d-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3173d-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3173d-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="3173d-157">DLL</span><span class="sxs-lookup"><span data-stu-id="3173d-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3173d-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3173d-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3173d-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="3173d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3173d-160">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="3173d-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

