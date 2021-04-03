---
title: Classe MDM_DeviceStatus_Antispyware01
description: A \_ classe MDM DeviceStatus \_ Antispyware01 é usada pela empresa para consultar o estado da conformidade de AntiSpyware de dispositivos com suas políticas corporativas.
ms.assetid: 53275aa1-ff7d-4630-b6c5-aedce3f4665a
keywords:
- Classe MDM_DeviceStatus_Antispyware01
- Classe MDM_DeviceStatus_Antispyware01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Antispyware01
- MDM_DeviceStatus_Antispyware01.InstanceID
- MDM_DeviceStatus_Antispyware01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91468c98981c93e211b3e3bee99564574f7a56cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824605"
---
# <a name="mdm_devicestatus_antispyware01-class"></a><span data-ttu-id="28293-105">\_ \_ Classe ANTISPYWARE01 do MDM DeviceStatus</span><span class="sxs-lookup"><span data-stu-id="28293-105">MDM\_DeviceStatus\_Antispyware01 class</span></span>

<span data-ttu-id="28293-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="28293-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="28293-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="28293-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="28293-108">A classe **MDM \_ DeviceStatus \_ Antispyware01** é usada pela empresa para consultar o estado da conformidade de AntiSpyware de dispositivos com suas políticas corporativas.</span><span class="sxs-lookup"><span data-stu-id="28293-108">The **MDM\_DeviceStatus\_Antispyware01** class is used by the enterprise to query the state of antispyware compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="28293-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="28293-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="28293-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28293-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Antispyware01
{
  string InstanceID;
  string ParentID;
  sint32 SignatureStatus;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="28293-111">Membros</span><span class="sxs-lookup"><span data-stu-id="28293-111">Members</span></span>

<span data-ttu-id="28293-112">A **classe \_ \_ Antispyware01 de MDM DeviceStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="28293-112">The **MDM\_DeviceStatus\_Antispyware01** class has these types of members:</span></span>

-   [<span data-ttu-id="28293-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="28293-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28293-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="28293-114">Properties</span></span>

<span data-ttu-id="28293-115">A **classe \_ \_ Antispyware01 do MDM DeviceStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="28293-115">The **MDM\_DeviceStatus\_Antispyware01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28293-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="28293-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28293-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="28293-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28293-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="28293-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28293-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="28293-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="28293-120">Nó para a consulta de AntiSpyware.</span><span class="sxs-lookup"><span data-stu-id="28293-120">Node for the antispyware query.</span></span>

</dd> <dt>

<span data-ttu-id="28293-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="28293-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28293-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="28293-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28293-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="28293-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28293-124">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="28293-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="28293-125">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="28293-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="28293-126">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="28293-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="28293-127">SignatureStatus</span><span class="sxs-lookup"><span data-stu-id="28293-127">SignatureStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-antivirus-signaturestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="28293-128">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="28293-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="28293-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="28293-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="28293-130">Status</span><span class="sxs-lookup"><span data-stu-id="28293-130">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="28293-131">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="28293-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="28293-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="28293-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28293-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28293-133">Requirements</span></span>



| <span data-ttu-id="28293-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="28293-134">Requirement</span></span> | <span data-ttu-id="28293-135">Valor</span><span class="sxs-lookup"><span data-stu-id="28293-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28293-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28293-136">Minimum supported client</span></span><br/> | <span data-ttu-id="28293-137">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="28293-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28293-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28293-138">Minimum supported server</span></span><br/> | <span data-ttu-id="28293-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="28293-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="28293-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="28293-140">Namespace</span></span><br/>                | <span data-ttu-id="28293-141">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="28293-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="28293-142">MOF</span><span class="sxs-lookup"><span data-stu-id="28293-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28293-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28293-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="28293-144">DLL</span><span class="sxs-lookup"><span data-stu-id="28293-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28293-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28293-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

