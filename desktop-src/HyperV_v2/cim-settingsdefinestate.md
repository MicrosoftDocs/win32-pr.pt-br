---
description: Associa dados de configurações a um elemento gerenciado.
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: Classe CIM_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1931b365108bb7b3df4269ae6acbb78292a0401d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760863"
---
# <a name="cim_settingsdefinestate-class"></a><span data-ttu-id="c413f-103">\_Classe CIM SettingsDefineState</span><span class="sxs-lookup"><span data-stu-id="c413f-103">CIM\_SettingsDefineState class</span></span>

<span data-ttu-id="c413f-104">Associa dados de configurações a um elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c413f-104">Associates settings data with a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="c413f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c413f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="c413f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c413f-106">Members</span></span>

<span data-ttu-id="c413f-107">A classe **CIM \_ SettingsDefineState** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c413f-107">The **CIM\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="c413f-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c413f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c413f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c413f-109">Properties</span></span>

<span data-ttu-id="c413f-110">A classe **CIM \_ SettingsDefineState** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c413f-110">The **CIM\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c413f-111">**Managedelement**</span><span class="sxs-lookup"><span data-stu-id="c413f-111">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c413f-112">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="c413f-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="c413f-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c413f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c413f-114">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c413f-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c413f-115">O elemento gerenciado na associação.</span><span class="sxs-lookup"><span data-stu-id="c413f-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="c413f-116">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="c413f-116">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c413f-117">Tipo de dados: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="c413f-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="c413f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c413f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c413f-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c413f-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c413f-120">Os dados de configurações na associação.</span><span class="sxs-lookup"><span data-stu-id="c413f-120">The settings data in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c413f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c413f-121">Requirements</span></span>



| <span data-ttu-id="c413f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c413f-122">Requirement</span></span> | <span data-ttu-id="c413f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c413f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c413f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c413f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c413f-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c413f-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c413f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c413f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c413f-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c413f-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c413f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c413f-128">Namespace</span></span><br/>                | <span data-ttu-id="c413f-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c413f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c413f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c413f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c413f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c413f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c413f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c413f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c413f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c413f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

