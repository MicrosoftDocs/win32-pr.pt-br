---
title: Classe MDM_DeviceStatus_OS01
description: A \_ classe MDM DeviceStatus \_ OS01 é usada pela empresa para consultar o sistema operacional em dispositivos com suas políticas corporativas.
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- Classe MDM_DeviceStatus_OS01
- Classe MDM_DeviceStatus_OS01, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01bff7a57d71b3d651ea2b97a0eac5b2ccd94255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085996"
---
# <a name="mdm_devicestatus_os01-class"></a><span data-ttu-id="58eb2-105">\_ \_ Classe OS01 do MDM DeviceStatus</span><span class="sxs-lookup"><span data-stu-id="58eb2-105">MDM\_DeviceStatus\_OS01 class</span></span>

<span data-ttu-id="58eb2-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="58eb2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="58eb2-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="58eb2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="58eb2-108">A classe **MDM \_ DeviceStatus \_ OS01** é usada pela empresa para consultar o sistema operacional em dispositivos com suas políticas corporativas.</span><span class="sxs-lookup"><span data-stu-id="58eb2-108">The **MDM\_DeviceStatus\_OS01** class is used by the enterprise to query the operating system on devices with their enterprise policies.</span></span>

<span data-ttu-id="58eb2-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="58eb2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58eb2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58eb2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a><span data-ttu-id="58eb2-111">Membros</span><span class="sxs-lookup"><span data-stu-id="58eb2-111">Members</span></span>

<span data-ttu-id="58eb2-112">A **classe \_ \_ OS01 de MDM DeviceStatus** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58eb2-112">The **MDM\_DeviceStatus\_OS01** class has these types of members:</span></span>

-   [<span data-ttu-id="58eb2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58eb2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58eb2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="58eb2-114">Properties</span></span>

<span data-ttu-id="58eb2-115">A **classe \_ \_ OS01 do MDM DeviceStatus** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="58eb2-115">The **MDM\_DeviceStatus\_OS01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="58eb2-116">Edição</span><span class="sxs-lookup"><span data-stu-id="58eb2-116">Edition</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
</dt> <dd> <dl> <dt>

<span data-ttu-id="58eb2-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58eb2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58eb2-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="58eb2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58eb2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="58eb2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58eb2-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58eb2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58eb2-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58eb2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58eb2-122">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58eb2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="58eb2-123">Nó para a consulta do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="58eb2-123">Node for the OS query.</span></span>

</dd> <dt>

<span data-ttu-id="58eb2-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="58eb2-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58eb2-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="58eb2-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58eb2-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="58eb2-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58eb2-127">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58eb2-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="58eb2-128">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="58eb2-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="58eb2-129">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/DeviceStatus"</span><span class="sxs-lookup"><span data-stu-id="58eb2-129">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58eb2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58eb2-130">Requirements</span></span>



| <span data-ttu-id="58eb2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="58eb2-131">Requirement</span></span> | <span data-ttu-id="58eb2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="58eb2-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58eb2-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58eb2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="58eb2-134">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="58eb2-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58eb2-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58eb2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="58eb2-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="58eb2-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="58eb2-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="58eb2-137">Namespace</span></span><br/>                | <span data-ttu-id="58eb2-138">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="58eb2-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="58eb2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="58eb2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58eb2-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58eb2-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="58eb2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="58eb2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58eb2-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58eb2-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

