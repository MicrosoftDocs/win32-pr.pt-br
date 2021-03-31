---
description: Fornece informações sobre um instantâneo em um arquivo de conjunto de VHD.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Classe Msvm_VHDSnapshotInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827473"
---
# <a name="msvm_vhdsnapshotinformation-class"></a><span data-ttu-id="5f94f-103">\_Classe Msvm VHDSnapshotInformation</span><span class="sxs-lookup"><span data-stu-id="5f94f-103">Msvm\_VHDSnapshotInformation class</span></span>

<span data-ttu-id="5f94f-104">Fornece informações sobre um instantâneo em um arquivo de conjunto de VHD</span><span class="sxs-lookup"><span data-stu-id="5f94f-104">Provides information about a snapshot within a VHD Set file</span></span>

<span data-ttu-id="5f94f-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5f94f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f94f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f94f-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a><span data-ttu-id="5f94f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5f94f-107">Members</span></span>

<span data-ttu-id="5f94f-108">A classe **Msvm \_ VHDSnapshotInformation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f94f-108">The **Msvm\_VHDSnapshotInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="5f94f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f94f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f94f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f94f-110">Properties</span></span>

<span data-ttu-id="5f94f-111">A classe **Msvm \_ VHDSnapshotInformation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f94f-111">The **Msvm\_VHDSnapshotInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5f94f-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="5f94f-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f94f-113">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5f94f-113">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="5f94f-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f94f-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f94f-115">A data e a hora da criação do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5f94f-115">The date and time of this snapshot's creation.</span></span>

</dd> <dt>

<span data-ttu-id="5f94f-116">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="5f94f-116">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f94f-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f94f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f94f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f94f-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f94f-119">O caminho do arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="5f94f-119">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="5f94f-120">**ParentPathsList**</span><span class="sxs-lookup"><span data-stu-id="5f94f-120">**ParentPathsList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f94f-121">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f94f-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5f94f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f94f-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f94f-123">Uma lista de caminhos de arquivo que representa todos os arquivos dos quais esse instantâneo depende.</span><span class="sxs-lookup"><span data-stu-id="5f94f-123">A list of file paths representing all of the files on which this snapshot depends.</span></span> <span data-ttu-id="5f94f-124">Este campo estará vazio, a menos que solicitado especificamente.</span><span class="sxs-lookup"><span data-stu-id="5f94f-124">This field will be empty unless specifically requested.</span></span> <span data-ttu-id="5f94f-125">A primeira entrada é o pai imediato do arquivo, com a última entrada sendo a raiz.</span><span class="sxs-lookup"><span data-stu-id="5f94f-125">The first entry is the file's immediate parent, with the last entry being the root.</span></span>

</dd> <dt>

<span data-ttu-id="5f94f-126">**ResilientChangeTrackingId**</span><span class="sxs-lookup"><span data-stu-id="5f94f-126">**ResilientChangeTrackingId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f94f-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f94f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f94f-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f94f-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f94f-129">A ID de controle de alteração resiliente, se houver, associada a esse instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5f94f-129">The resilient change tracking ID, if any, associated with this snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="5f94f-130">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="5f94f-130">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f94f-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f94f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f94f-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f94f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f94f-133">Um GUID que identifica exclusivamente esse instantâneo dentro do arquivo de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="5f94f-133">A GUID that uniquely identifies this snapshot within the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="5f94f-134">**SnapshotPath**</span><span class="sxs-lookup"><span data-stu-id="5f94f-134">**SnapshotPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f94f-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5f94f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f94f-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f94f-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5f94f-137">O caminho do arquivo representado por esse instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5f94f-137">The path of the file represented by this snapshot.</span></span> <span data-ttu-id="5f94f-138">Esse campo pode estar vazio se não houver nenhum arquivo associado a esse instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5f94f-138">This field may be empty if there is no file associated with this snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f94f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f94f-139">Requirements</span></span>



| <span data-ttu-id="5f94f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f94f-140">Requirement</span></span> | <span data-ttu-id="5f94f-141">Valor</span><span class="sxs-lookup"><span data-stu-id="5f94f-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f94f-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f94f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5f94f-143">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5f94f-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5f94f-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f94f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5f94f-145">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5f94f-145">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5f94f-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f94f-146">Namespace</span></span><br/>                | <span data-ttu-id="5f94f-147">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5f94f-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5f94f-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5f94f-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f94f-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f94f-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f94f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5f94f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f94f-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5f94f-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




