---
description: Fornece informações adicionais a serem usadas com o método CreateReferencePoint da classe Msvm \_ CollectionReferencePointService.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Classe Msvm_CollectionReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091145"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a><span data-ttu-id="749e7-103">\_Classe Msvm CollectionReferencePointSettingData</span><span class="sxs-lookup"><span data-stu-id="749e7-103">Msvm\_CollectionReferencePointSettingData class</span></span>

<span data-ttu-id="749e7-104">Fornece informações adicionais a serem usadas com o método [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) da classe [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="749e7-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="749e7-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="749e7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="749e7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="749e7-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="749e7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="749e7-107">Members</span></span>

<span data-ttu-id="749e7-108">A classe **Msvm \_ CollectionReferencePointSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="749e7-108">The **Msvm\_CollectionReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="749e7-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="749e7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="749e7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="749e7-110">Properties</span></span>

<span data-ttu-id="749e7-111">A classe **Msvm \_ CollectionReferencePointSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="749e7-111">The **Msvm\_CollectionReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="749e7-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="749e7-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="749e7-113">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="749e7-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="749e7-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="749e7-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="749e7-115">Nível de consistência do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="749e7-115">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="749e7-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="749e7-116"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="749e7-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Consistente** com o aplicativo (1)</span><span class="sxs-lookup"><span data-stu-id="749e7-117"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="749e7-118">O ponto de referência indica um ponto no tempo em que o sistema virtual estava em estado de falha consistente.</span><span class="sxs-lookup"><span data-stu-id="749e7-118">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="749e7-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Falha consistente** (2)</span><span class="sxs-lookup"><span data-stu-id="749e7-119"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="749e7-120">O ponto de referência indica um ponto no tempo em que o sistema virtual estava no estado consistente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="749e7-120">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="749e7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="749e7-121">Requirements</span></span>



| <span data-ttu-id="749e7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="749e7-122">Requirement</span></span> | <span data-ttu-id="749e7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="749e7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="749e7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="749e7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="749e7-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="749e7-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="749e7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="749e7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="749e7-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="749e7-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="749e7-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="749e7-128">Namespace</span></span><br/>                | <span data-ttu-id="749e7-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="749e7-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="749e7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="749e7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="749e7-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="749e7-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="749e7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="749e7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="749e7-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="749e7-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="749e7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="749e7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="749e7-135">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="749e7-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




