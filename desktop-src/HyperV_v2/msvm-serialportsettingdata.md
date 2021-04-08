---
description: Descreve os dados de configuração para uma porta serial virtual.
ms.assetid: 8b257bbf-495a-4eef-86a1-70e31e4a85a5
title: Classe Msvm_SerialPortSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortSettingData
- Msvm_SerialPortSettingData.DebuggerMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 21a1ab58608c5631a328795272d6a04aa56aedf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828586"
---
# <a name="msvm_serialportsettingdata-class"></a><span data-ttu-id="fcb74-103">\_Classe Msvm SerialPortSettingData</span><span class="sxs-lookup"><span data-stu-id="fcb74-103">Msvm\_SerialPortSettingData class</span></span>

<span data-ttu-id="fcb74-104">Descreve os dados de configuração para uma porta serial virtual.</span><span class="sxs-lookup"><span data-stu-id="fcb74-104">Describes the setting data for a virtual serial port.</span></span>

<span data-ttu-id="fcb74-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="fcb74-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb74-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fcb74-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortSettingData : CIM_ResourceAllocationSettingData
{
  boolean DebuggerMode;
};
```

## <a name="members"></a><span data-ttu-id="fcb74-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fcb74-107">Members</span></span>

<span data-ttu-id="fcb74-108">A classe **Msvm \_ SerialPortSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fcb74-108">The **Msvm\_SerialPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fcb74-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcb74-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcb74-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcb74-110">Properties</span></span>

<span data-ttu-id="fcb74-111">A classe **Msvm \_ SerialPortSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fcb74-111">The **Msvm\_SerialPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcb74-112">**DebuggerMode**</span><span class="sxs-lookup"><span data-stu-id="fcb74-112">**DebuggerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb74-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="fcb74-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fcb74-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fcb74-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fcb74-115">**true** se o modo do depurador estiver habilitado em uma porta serial virtual; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fcb74-115">**true** if the debugger mode is enabled on a virtual serial port; otherwise, **false**.</span></span> <span data-ttu-id="fcb74-116">O modo de depurador aprimora o uso de um depurador de kernel do Microsoft Windows em uma porta serial virtual.</span><span class="sxs-lookup"><span data-stu-id="fcb74-116">The debugger mode enhances the use of a Microsoft Windows kernel debugger over a virtual serial port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcb74-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcb74-117">Requirements</span></span>



| <span data-ttu-id="fcb74-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcb74-118">Requirement</span></span> | <span data-ttu-id="fcb74-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fcb74-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb74-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcb74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fcb74-121">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fcb74-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="fcb74-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcb74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fcb74-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fcb74-123">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="fcb74-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="fcb74-124">Namespace</span></span><br/>                | <span data-ttu-id="fcb74-125">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fcb74-125">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fcb74-126">MOF</span><span class="sxs-lookup"><span data-stu-id="fcb74-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcb74-127"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcb74-127"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcb74-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fcb74-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcb74-129"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fcb74-129"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fcb74-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcb74-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb74-131">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fcb74-131">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




