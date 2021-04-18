---
title: Classe Win32_TSVmMetadataAssociation
description: Representa uma associação entre uma máquina virtual Área de Trabalho Remota e suas propriedades de metadados.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSVmMetadataAssociation Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSVmMetadataAssociation classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770443"
---
# <a name="win32_tsvmmetadataassociation-class"></a><span data-ttu-id="37488-105">\_Classe Win32 TSVmMetadataAssociation</span><span class="sxs-lookup"><span data-stu-id="37488-105">Win32\_TSVmMetadataAssociation class</span></span>

<span data-ttu-id="37488-106">Representa uma associação entre uma máquina virtual Área de Trabalho Remota e suas propriedades de metadados.</span><span class="sxs-lookup"><span data-stu-id="37488-106">Represents an association between a Remote Desktop virtual machine and its metadata properties.</span></span>

<span data-ttu-id="37488-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="37488-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37488-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37488-108">Syntax</span></span>

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a><span data-ttu-id="37488-109">Membros</span><span class="sxs-lookup"><span data-stu-id="37488-109">Members</span></span>

<span data-ttu-id="37488-110">A classe **Win32 \_ TSVmMetadataAssociation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="37488-110">The **Win32\_TSVmMetadataAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="37488-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="37488-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37488-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="37488-112">Properties</span></span>

<span data-ttu-id="37488-113">A classe **Win32 \_ TSVmMetadataAssociation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="37488-113">The **Win32\_TSVmMetadataAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="37488-114">**MetadataItem**</span><span class="sxs-lookup"><span data-stu-id="37488-114">**MetadataItem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37488-115">Tipo de dados: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span><span class="sxs-lookup"><span data-stu-id="37488-115">Data type: **[**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="37488-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="37488-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="37488-117">Uma instância da classe [**Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md) que representa os metadados para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="37488-117">An instance of the [**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md) class that represents the metadata for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="37488-118">**TSVm**</span><span class="sxs-lookup"><span data-stu-id="37488-118">**TSVm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37488-119">Tipo de dados: **[ **Win32 \_ TSVm**](win32-tsvm.md)**</span><span class="sxs-lookup"><span data-stu-id="37488-119">Data type: **[**Win32\_TSVm**](win32-tsvm.md)**</span></span>
</dt> <dt>

<span data-ttu-id="37488-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="37488-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37488-121">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37488-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="37488-122">Uma instância da classe [**Win32 \_ TSVm**](win32-tsvm.md) que representa a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="37488-122">An instance of the [**Win32\_TSVm**](win32-tsvm.md) class that represents the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37488-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37488-123">Requirements</span></span>



| <span data-ttu-id="37488-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="37488-124">Requirement</span></span> | <span data-ttu-id="37488-125">Valor</span><span class="sxs-lookup"><span data-stu-id="37488-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="37488-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37488-126">Minimum supported client</span></span><br/> | <span data-ttu-id="37488-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="37488-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="37488-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37488-128">Minimum supported server</span></span><br/> | <span data-ttu-id="37488-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37488-129">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="37488-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="37488-130">Namespace</span></span><br/>                | <span data-ttu-id="37488-131">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="37488-131">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="37488-132">MOF</span><span class="sxs-lookup"><span data-stu-id="37488-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37488-133"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37488-133"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="37488-134">DLL</span><span class="sxs-lookup"><span data-stu-id="37488-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37488-135"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37488-135"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

