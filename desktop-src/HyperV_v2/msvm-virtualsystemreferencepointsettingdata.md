---
description: Fornece informações adicionais a serem usadas com o método CreateReferencePoint da classe Msvm \_ VirtualSystemReferencePointService.
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Classe Msvm_VirtualSystemReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea36f9504d9c2d6b7e875f32bb7cd0a0efd167da
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105787519"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a><span data-ttu-id="de61e-103">\_Classe Msvm VirtualSystemReferencePointSettingData</span><span class="sxs-lookup"><span data-stu-id="de61e-103">Msvm\_VirtualSystemReferencePointSettingData class</span></span>

<span data-ttu-id="de61e-104">Fornece informações adicionais a serem usadas com o método [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) da classe [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="de61e-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="de61e-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="de61e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de61e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de61e-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="de61e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="de61e-107">Members</span></span>

<span data-ttu-id="de61e-108">A classe **Msvm \_ VirtualSystemReferencePointSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de61e-108">The **Msvm\_VirtualSystemReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="de61e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de61e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de61e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de61e-110">Properties</span></span>

<span data-ttu-id="de61e-111">A classe **Msvm \_ VirtualSystemReferencePointSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="de61e-111">The **Msvm\_VirtualSystemReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de61e-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="de61e-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de61e-113">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="de61e-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="de61e-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de61e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de61e-115">O nível de consistência do ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="de61e-115">The consistency level of the reference point.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de61e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de61e-116">Requirements</span></span>



| <span data-ttu-id="de61e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="de61e-117">Requirement</span></span> | <span data-ttu-id="de61e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="de61e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de61e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de61e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="de61e-120">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="de61e-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="de61e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de61e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="de61e-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="de61e-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="de61e-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="de61e-123">Namespace</span></span><br/>                | <span data-ttu-id="de61e-124">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="de61e-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="de61e-125">MOF</span><span class="sxs-lookup"><span data-stu-id="de61e-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de61e-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de61e-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="de61e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="de61e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de61e-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="de61e-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="de61e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="de61e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de61e-130">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="de61e-130">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




