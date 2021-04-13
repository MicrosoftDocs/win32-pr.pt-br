---
description: Especifica os logs da arquitetura de verificação de máquina (MCA) brutos. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: Classe MSMCAInfo_RawMCAData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 6cafc16ddbc91181cc2114def07a193941988228
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501672"
---
# <a name="msmcainfo_rawmcadata-class"></a><span data-ttu-id="315b8-104">\_Classe MSMCAInfo RawMCAData</span><span class="sxs-lookup"><span data-stu-id="315b8-104">MSMCAInfo\_RawMCAData class</span></span>

<span data-ttu-id="315b8-105">O **MSMCAInfo \_ RawMCAData** especifica os logs da arquitetura de verificação de máquina (MCA) brutos.</span><span class="sxs-lookup"><span data-stu-id="315b8-105">The **MSMCAInfo\_RawMCAData** specifies the raw Machine Check Architecture (MCA) logs.</span></span> <span data-ttu-id="315b8-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="315b8-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="315b8-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="315b8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="315b8-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="315b8-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="315b8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="315b8-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="315b8-110">Membros</span><span class="sxs-lookup"><span data-stu-id="315b8-110">Members</span></span>

<span data-ttu-id="315b8-111">A classe **MSMCAInfo \_ RawMCAData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="315b8-111">The **MSMCAInfo\_RawMCAData** class has these types of members:</span></span>

-   [<span data-ttu-id="315b8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="315b8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="315b8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="315b8-113">Properties</span></span>

<span data-ttu-id="315b8-114">A classe **MSMCAInfo \_ RawMCAData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="315b8-114">The **MSMCAInfo\_RawMCAData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="315b8-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="315b8-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="315b8-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="315b8-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="315b8-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="315b8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="315b8-118">TRUE, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="315b8-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="315b8-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="315b8-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="315b8-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="315b8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="315b8-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="315b8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="315b8-122">Número de registros de erro.</span><span class="sxs-lookup"><span data-stu-id="315b8-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="315b8-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="315b8-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="315b8-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="315b8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="315b8-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="315b8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="315b8-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="315b8-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="315b8-127">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="315b8-127">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="315b8-128">**Registros**</span><span class="sxs-lookup"><span data-stu-id="315b8-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="315b8-129">Tipo de dados: matriz de **\_ entrada MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="315b8-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="315b8-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="315b8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="315b8-131">Matriz de registros de erro de MCA.</span><span class="sxs-lookup"><span data-stu-id="315b8-131">Array of MCA error records.</span></span> <span data-ttu-id="315b8-132">O número de registros de erro MCA na matriz é especificado pela propriedade **Count** .</span><span class="sxs-lookup"><span data-stu-id="315b8-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="315b8-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="315b8-133">Remarks</span></span>

<span data-ttu-id="315b8-134">A classe **MSMCAInfo \_ RawMCAData** é derivada de [**MSMCAInfo**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="315b8-134">The **MSMCAInfo\_RawMCAData** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="315b8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="315b8-135">Requirements</span></span>



| <span data-ttu-id="315b8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="315b8-136">Requirement</span></span> | <span data-ttu-id="315b8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="315b8-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="315b8-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="315b8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="315b8-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="315b8-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="315b8-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="315b8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="315b8-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="315b8-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="315b8-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="315b8-142">Namespace</span></span><br/>                | <span data-ttu-id="315b8-143">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="315b8-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="315b8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="315b8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="315b8-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="315b8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="315b8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="315b8-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315b8-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="315b8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315b8-149">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="315b8-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="315b8-150">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="315b8-150">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

