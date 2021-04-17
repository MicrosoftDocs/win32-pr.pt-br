---
description: Exporte os dados de configuração a serem passados para o método ExportReferencePoint da \_ classe Msvm CollectionReferencePointService.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Classe Msvm_CollectionReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759408"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a><span data-ttu-id="b83d9-103">\_Classe Msvm CollectionReferencePointExportSettingData</span><span class="sxs-lookup"><span data-stu-id="b83d9-103">Msvm\_CollectionReferencePointExportSettingData class</span></span>

<span data-ttu-id="b83d9-104">Exporte os dados de configuração a serem passados para o método [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) da classe [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b83d9-104">Export setting data to be passed in to the [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="b83d9-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b83d9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b83d9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b83d9-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="b83d9-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b83d9-107">Members</span></span>

<span data-ttu-id="b83d9-108">A classe **Msvm \_ CollectionReferencePointExportSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b83d9-108">The **Msvm\_CollectionReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b83d9-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b83d9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b83d9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b83d9-110">Properties</span></span>

<span data-ttu-id="b83d9-111">A classe **Msvm \_ CollectionReferencePointExportSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b83d9-111">The **Msvm\_CollectionReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b83d9-112">**BaseReferencePointCollection**</span><span class="sxs-lookup"><span data-stu-id="b83d9-112">**BaseReferencePointCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d9-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b83d9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d9-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b83d9-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b83d9-115">Caminho para uma instância de [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) que representa a coleção de pontos de referência base a ser usada para exportação diferencial.</span><span class="sxs-lookup"><span data-stu-id="b83d9-115">Path to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the base reference point collection to be used for differential export.</span></span>

</dd> <dt>

<span data-ttu-id="b83d9-116">**VirtualMachinesToDisksToExport**</span><span class="sxs-lookup"><span data-stu-id="b83d9-116">**VirtualMachinesToDisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d9-117">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b83d9-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b83d9-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b83d9-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b83d9-119">Qualificadores: **HyperVEmbeddedInstance** ("Msvm \_ VirtualMachineToDisks")</span><span class="sxs-lookup"><span data-stu-id="b83d9-119">Qualifiers: **HyperVEmbeddedInstance** ("Msvm\_VirtualMachineToDisks")</span></span>
</dt> </dl>

<span data-ttu-id="b83d9-120">Lista de "VirtualMachines para DisksToExport" informações de mapa para as quais os dados precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="b83d9-120">List of "VirtualMachines To DisksToExport" map information for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b83d9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b83d9-121">Requirements</span></span>



| <span data-ttu-id="b83d9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b83d9-122">Requirement</span></span> | <span data-ttu-id="b83d9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b83d9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b83d9-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b83d9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b83d9-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b83d9-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b83d9-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b83d9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b83d9-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b83d9-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b83d9-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="b83d9-128">Namespace</span></span><br/>                | <span data-ttu-id="b83d9-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b83d9-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b83d9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b83d9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b83d9-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b83d9-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b83d9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b83d9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b83d9-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b83d9-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b83d9-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b83d9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b83d9-135">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="b83d9-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




