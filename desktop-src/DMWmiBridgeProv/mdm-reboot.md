---
title: Classe MDM_Reboot
description: O Rebootclass de MDM \_ é usado para definir as configurações de reinicialização.
ms.assetid: 876ba854-1c26-49cf-915d-194be9f9c1d4
keywords:
- Classe MDM_Reboot
- Classe MDM_Reboot, descrita
topic_type:
- apiref
api_name:
- MDM_Reboot
- MDM_Reboot.InstanceID
- MDM_Reboot.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e078dfef883db5aad67e7ee834ceca4bd0a942
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008904"
---
# <a name="mdm_reboot-class"></a><span data-ttu-id="9bf77-105">\_Classe de reinicialização MDM</span><span class="sxs-lookup"><span data-stu-id="9bf77-105">MDM\_Reboot class</span></span>

<span data-ttu-id="9bf77-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="9bf77-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9bf77-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="9bf77-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9bf77-108">A classe de **\_ reinicialização do MDM** é usada para definir as configurações de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="9bf77-108">The **MDM\_Reboot** class is used to configure reboot settings.</span></span>

<span data-ttu-id="9bf77-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9bf77-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bf77-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bf77-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="9bf77-111">Membros</span><span class="sxs-lookup"><span data-stu-id="9bf77-111">Members</span></span>

<span data-ttu-id="9bf77-112">A classe de **\_ reinicialização de MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9bf77-112">The **MDM\_Reboot** class has these types of members:</span></span>

-   [<span data-ttu-id="9bf77-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9bf77-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="9bf77-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9bf77-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9bf77-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="9bf77-115">Methods</span></span>

<span data-ttu-id="9bf77-116">A classe de **\_ reinicialização de MDM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9bf77-116">The **MDM\_Reboot** class has these methods.</span></span>



| <span data-ttu-id="9bf77-117">Método</span><span class="sxs-lookup"><span data-stu-id="9bf77-117">Method</span></span>                                                | <span data-ttu-id="9bf77-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bf77-118">Description</span></span>                                             |
|:------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="9bf77-119">**RebootNowMethod**</span><span class="sxs-lookup"><span data-stu-id="9bf77-119">**RebootNowMethod**</span></span>](mdm-reboot-rebootnowmethod.md) | <span data-ttu-id="9bf77-120">Esse método executa uma reinicialização do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9bf77-120">This method executes a reboot of the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9bf77-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9bf77-121">Properties</span></span>

<span data-ttu-id="9bf77-122">A classe de **\_ reinicialização de MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9bf77-122">The **MDM\_Reboot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9bf77-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9bf77-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf77-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bf77-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bf77-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf77-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf77-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bf77-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9bf77-127">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="9bf77-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="9bf77-128">Para essa classe, a cadeia de caracteres é "reinicializar".</span><span class="sxs-lookup"><span data-stu-id="9bf77-128">For this class, the string is "Reboot".</span></span>

</dd> <dt>

<span data-ttu-id="9bf77-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9bf77-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bf77-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9bf77-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9bf77-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9bf77-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9bf77-132">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9bf77-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9bf77-133">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="9bf77-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="9bf77-134">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="9bf77-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bf77-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bf77-135">Requirements</span></span>



| <span data-ttu-id="9bf77-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bf77-136">Requirement</span></span> | <span data-ttu-id="9bf77-137">Valor</span><span class="sxs-lookup"><span data-stu-id="9bf77-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bf77-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bf77-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9bf77-139">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9bf77-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9bf77-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bf77-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9bf77-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9bf77-141">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="9bf77-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="9bf77-142">Namespace</span></span><br/>                | <span data-ttu-id="9bf77-143">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="9bf77-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="9bf77-144">MOF</span><span class="sxs-lookup"><span data-stu-id="9bf77-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9bf77-145"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9bf77-145"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="9bf77-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9bf77-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bf77-147"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="9bf77-147"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

