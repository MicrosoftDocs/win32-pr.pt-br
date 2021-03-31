---
description: Fornece informações adicionais a serem usadas com o método ExportReferencePoint da classe Msvm \_ VirtualSystemReferencePointService.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Classe Msvm_VirtualSystemReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011940"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a><span data-ttu-id="05c22-103">\_Classe Msvm VirtualSystemReferencePointExportSettingData</span><span class="sxs-lookup"><span data-stu-id="05c22-103">Msvm\_VirtualSystemReferencePointExportSettingData class</span></span>

<span data-ttu-id="05c22-104">Fornece informações adicionais a serem usadas com o método [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) da classe [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="05c22-104">Provides additional information to be used with the [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="05c22-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="05c22-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c22-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05c22-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="05c22-107">Membros</span><span class="sxs-lookup"><span data-stu-id="05c22-107">Members</span></span>

<span data-ttu-id="05c22-108">A classe **Msvm \_ VirtualSystemReferencePointExportSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="05c22-108">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="05c22-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05c22-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05c22-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05c22-110">Properties</span></span>

<span data-ttu-id="05c22-111">A classe **Msvm \_ VirtualSystemReferencePointExportSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="05c22-111">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="05c22-112">**BaseReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="05c22-112">**BaseReferencePoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05c22-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05c22-113">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="05c22-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05c22-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05c22-115">Caminho do ponto de referência base com relação ao qual a exportação deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="05c22-115">Path of the base reference point with respect to which export should be performed.</span></span>

</dd> <dt>

<span data-ttu-id="05c22-116">**DisksToExport**</span><span class="sxs-lookup"><span data-stu-id="05c22-116">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="05c22-117">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="05c22-117">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="05c22-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05c22-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="05c22-119">IDs da instância do WMI dos discos para os quais os dados precisam ser exportados.</span><span class="sxs-lookup"><span data-stu-id="05c22-119">WMI instance IDs of the disks for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05c22-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c22-120">Requirements</span></span>



| <span data-ttu-id="05c22-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c22-121">Requirement</span></span> | <span data-ttu-id="05c22-122">Valor</span><span class="sxs-lookup"><span data-stu-id="05c22-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c22-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c22-123">Minimum supported client</span></span><br/> | <span data-ttu-id="05c22-124">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="05c22-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="05c22-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05c22-125">Minimum supported server</span></span><br/> | <span data-ttu-id="05c22-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="05c22-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="05c22-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="05c22-127">Namespace</span></span><br/>                | <span data-ttu-id="05c22-128">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="05c22-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="05c22-129">MOF</span><span class="sxs-lookup"><span data-stu-id="05c22-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05c22-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05c22-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05c22-131">DLL</span><span class="sxs-lookup"><span data-stu-id="05c22-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05c22-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05c22-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05c22-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="05c22-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c22-134">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="05c22-134">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




