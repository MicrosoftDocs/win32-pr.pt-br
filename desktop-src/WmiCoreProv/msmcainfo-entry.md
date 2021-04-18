---
description: Indica uma entrada de informações do MCA, correção de máquina corrigida (CMC) ou erro de plataforma corrigido (CPE). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: Classe MSMCAInfo_Entry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764260"
---
# <a name="msmcainfo_entry-class"></a><span data-ttu-id="e0ab0-104">\_Classe de entrada MSMCAInfo</span><span class="sxs-lookup"><span data-stu-id="e0ab0-104">MSMCAInfo\_Entry class</span></span>

<span data-ttu-id="e0ab0-105">A classe de **\_ entrada MSMCAInfo** indica uma entrada de informações de MCA, verificação de máquina corrigida (CMC) ou erro de plataforma corrigido (CPE).</span><span class="sxs-lookup"><span data-stu-id="e0ab0-105">The **MSMCAInfo\_Entry** class indicates an MCA, corrected machine check (CMC), or corrected platform error (CPE) information entry.</span></span> <span data-ttu-id="e0ab0-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="e0ab0-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e0ab0-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ab0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0ab0-109">Syntax</span></span>

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a><span data-ttu-id="e0ab0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e0ab0-110">Members</span></span>

<span data-ttu-id="e0ab0-111">A classe de **\_ entrada MSMCAInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e0ab0-111">The **MSMCAInfo\_Entry** class has these types of members:</span></span>

-   [<span data-ttu-id="e0ab0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e0ab0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0ab0-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e0ab0-113">Properties</span></span>

<span data-ttu-id="e0ab0-114">A classe de **\_ entrada MSMCAInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-114">The **MSMCAInfo\_Entry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0ab0-115">**Dados**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-115">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ab0-116">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-116">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e0ab0-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0ab0-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ab0-118">Matriz de inteiros que contém um registro de erro MCA completo, conforme relatado pela camada de abstração do sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="e0ab0-118">Integer array that contains a complete MCA error record as reported by the system abstraction layer (SAL).</span></span> <span data-ttu-id="e0ab0-119">O SAL é o código gravado na ROM que o sistema operacional chama para executar operações dependentes da plataforma.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-119">The SAL is code burned into ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="e0ab0-120">É semelhante ao BIOS em uma plataforma x86.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-120">It is similar to the BIOS on an x86 platform.</span></span>

</dd> <dt>

<span data-ttu-id="e0ab0-121">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-121">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ab0-122">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0ab0-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0ab0-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ab0-124">Número de bytes no registro de erros.</span><span class="sxs-lookup"><span data-stu-id="e0ab0-124">Number of bytes in the error record.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0ab0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0ab0-125">Remarks</span></span>

<span data-ttu-id="e0ab0-126">A classe de **\_ entrada MSMCAInfo** é derivada de [**MSMCAInfo**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="e0ab0-126">The **MSMCAInfo\_Entry** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ab0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0ab0-127">Requirements</span></span>



| <span data-ttu-id="e0ab0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0ab0-128">Requirement</span></span> | <span data-ttu-id="e0ab0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e0ab0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ab0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0ab0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ab0-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0ab0-131">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="e0ab0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0ab0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ab0-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0ab0-133">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="e0ab0-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0ab0-134">Namespace</span></span><br/>                | <span data-ttu-id="e0ab0-135">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="e0ab0-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="e0ab0-136">MOF</span><span class="sxs-lookup"><span data-stu-id="e0ab0-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0ab0-137"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0ab0-137"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0ab0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e0ab0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0ab0-139"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0ab0-139"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0ab0-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0ab0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0ab0-141">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="e0ab0-141">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="e0ab0-142">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="e0ab0-142">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

 




