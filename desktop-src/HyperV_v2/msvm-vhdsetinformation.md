---
description: Fornece informações sobre um arquivo de conjunto VHD.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Classe Msvm_VHDSetInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 51f1371baea902627160c2c7a1fb31d156be8951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758634"
---
# <a name="msvm_vhdsetinformation-class"></a><span data-ttu-id="b7e8c-103">\_Classe Msvm VHDSetInformation</span><span class="sxs-lookup"><span data-stu-id="b7e8c-103">Msvm\_VHDSetInformation class</span></span>

<span data-ttu-id="b7e8c-104">Fornece informações sobre um arquivo de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-104">Provides information about a VHD Set file.</span></span>

<span data-ttu-id="b7e8c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7e8c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7e8c-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a><span data-ttu-id="b7e8c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b7e8c-107">Members</span></span>

<span data-ttu-id="b7e8c-108">A classe **Msvm \_ VHDSetInformation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b7e8c-108">The **Msvm\_VHDSetInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="b7e8c-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b7e8c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7e8c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b7e8c-110">Properties</span></span>

<span data-ttu-id="b7e8c-111">A classe **Msvm \_ VHDSetInformation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-111">The **Msvm\_VHDSetInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7e8c-112">**Todos os caminhos**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-112">**AllPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7e8c-113">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b7e8c-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7e8c-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7e8c-115">Uma lista de todos os arquivos abrangedos pelo arquivo de conjunto de VHD, incluindo quaisquer arquivos não referenciados e todos os pais do disco rígido virtual raiz.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-115">A list of all files encompassed by the VHD Set file, including any unreferenced files and any parents of the root virtual hard disk.</span></span> <span data-ttu-id="b7e8c-116">Todos os arquivos listados após o disco rígido virtual raiz não são gerenciados por este arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-116">All files listed after the root virtual hard disk are unmanaged by this VHD Set file.</span></span> <span data-ttu-id="b7e8c-117">Esse campo pode estar vazio se essas informações não foram solicitadas especificamente.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-117">This field may be empty if this information was not specifically requested.</span></span>

</dd> <dt>

<span data-ttu-id="b7e8c-118">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-118">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7e8c-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7e8c-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7e8c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7e8c-121">O caminho do arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-121">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="b7e8c-122">**SnapshotIdList**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-122">**SnapshotIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7e8c-123">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b7e8c-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b7e8c-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b7e8c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7e8c-125">Uma lista de GUIDs que representa todos os instantâneos contidos por este arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="b7e8c-125">A list of GUIDs representing all of the snapshots contained by this VHD Set file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7e8c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7e8c-126">Requirements</span></span>



| <span data-ttu-id="b7e8c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7e8c-127">Requirement</span></span> | <span data-ttu-id="b7e8c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b7e8c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e8c-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7e8c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e8c-130">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b7e8c-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b7e8c-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7e8c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e8c-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b7e8c-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b7e8c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7e8c-133">Namespace</span></span><br/>                | <span data-ttu-id="b7e8c-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b7e8c-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b7e8c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b7e8c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7e8c-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7e8c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7e8c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b7e8c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7e8c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7e8c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




