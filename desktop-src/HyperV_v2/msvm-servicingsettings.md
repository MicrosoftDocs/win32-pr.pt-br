---
description: Contém as configurações usadas durante as operações de manutenção.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Classe Msvm_ServicingSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461197"
---
# <a name="msvm_servicingsettings-class"></a><span data-ttu-id="3fd81-103">\_Classe Msvm ServicingSettings</span><span class="sxs-lookup"><span data-stu-id="3fd81-103">Msvm\_ServicingSettings class</span></span>

<span data-ttu-id="3fd81-104">Contém as configurações usadas durante as operações de manutenção.</span><span class="sxs-lookup"><span data-stu-id="3fd81-104">Contains settings used during servicing operations.</span></span>

<span data-ttu-id="3fd81-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3fd81-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd81-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fd81-106">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="3fd81-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3fd81-107">Members</span></span>

<span data-ttu-id="3fd81-108">A classe **Msvm \_ ServicingSettings** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3fd81-108">The **Msvm\_ServicingSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="3fd81-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3fd81-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fd81-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3fd81-110">Properties</span></span>

<span data-ttu-id="3fd81-111">A classe **Msvm \_ ServicingSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3fd81-111">The **Msvm\_ServicingSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fd81-112">**Versão**</span><span class="sxs-lookup"><span data-stu-id="3fd81-112">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fd81-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="3fd81-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3fd81-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3fd81-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3fd81-115">Contém a versão da definição de classe.</span><span class="sxs-lookup"><span data-stu-id="3fd81-115">Contains the class definition's version.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3fd81-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd81-116">Requirements</span></span>



| <span data-ttu-id="3fd81-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd81-117">Requirement</span></span> | <span data-ttu-id="3fd81-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3fd81-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd81-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fd81-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd81-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3fd81-120">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3fd81-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fd81-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd81-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3fd81-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fd81-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fd81-123">Namespace</span></span><br/>                | <span data-ttu-id="3fd81-124">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3fd81-124">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3fd81-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3fd81-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fd81-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fd81-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fd81-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3fd81-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fd81-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fd81-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




