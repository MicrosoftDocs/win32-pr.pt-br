---
description: Contém um evento de arquitetura de verificação de máquina (MCA). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: Classe MSMCAInfo_RawMCAEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922420"
---
# <a name="msmcainfo_rawmcaevent-class"></a><span data-ttu-id="c38a8-104">\_Classe MSMCAInfo RawMCAEvent</span><span class="sxs-lookup"><span data-stu-id="c38a8-104">MSMCAInfo\_RawMCAEvent class</span></span>

<span data-ttu-id="c38a8-105">A classe **MSMCAInfo \_ RawMCAEvent** contém um evento de arquitetura de verificação de máquina (MCA).</span><span class="sxs-lookup"><span data-stu-id="c38a8-105">The **MSMCAInfo\_RawMCAEvent** class contains a Machine Check Architecture (MCA) event.</span></span> <span data-ttu-id="c38a8-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c38a8-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="c38a8-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c38a8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c38a8-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="c38a8-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c38a8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c38a8-109">Syntax</span></span>

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a><span data-ttu-id="c38a8-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c38a8-110">Members</span></span>

<span data-ttu-id="c38a8-111">A classe **MSMCAInfo \_ RawMCAEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c38a8-111">The **MSMCAInfo\_RawMCAEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c38a8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c38a8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c38a8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c38a8-113">Properties</span></span>

<span data-ttu-id="c38a8-114">A classe **MSMCAInfo \_ RawMCAEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c38a8-114">The **MSMCAInfo\_RawMCAEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c38a8-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="c38a8-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38a8-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c38a8-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c38a8-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c38a8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c38a8-118">TRUE, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="c38a8-118">TRUE, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c38a8-119">**Count**</span><span class="sxs-lookup"><span data-stu-id="c38a8-119">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38a8-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c38a8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c38a8-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c38a8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c38a8-122">Número de registros de erro.</span><span class="sxs-lookup"><span data-stu-id="c38a8-122">Number of error records.</span></span>

</dd> <dt>

<span data-ttu-id="c38a8-123">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="c38a8-123">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38a8-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c38a8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c38a8-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c38a8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c38a8-126">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c38a8-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c38a8-127">Cadeia de caracteres que identifica exclusivamente essa instância da classe **MSMCAInfo \_ RawMCAEvent** .</span><span class="sxs-lookup"><span data-stu-id="c38a8-127">String that uniquely identifies this instance of the **MSMCAInfo\_RawMCAEvent** class.</span></span>

</dd> <dt>

<span data-ttu-id="c38a8-128">**Registros**</span><span class="sxs-lookup"><span data-stu-id="c38a8-128">**Records**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c38a8-129">Tipo de dados: matriz de **\_ entrada MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="c38a8-129">Data type: **MSMCAInfo\_Entry** array</span></span>
</dt> <dt>

<span data-ttu-id="c38a8-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c38a8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c38a8-131">Matriz de registros de erro de MCA.</span><span class="sxs-lookup"><span data-stu-id="c38a8-131">Array of MCA error records.</span></span> <span data-ttu-id="c38a8-132">O número de registros de erro MCA na matriz é especificado pela propriedade **Count** .</span><span class="sxs-lookup"><span data-stu-id="c38a8-132">The number of MCA error records in the array is specified by the **Count** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c38a8-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="c38a8-133">Remarks</span></span>

<span data-ttu-id="c38a8-134">A classe **MSMCAInfo \_ RawMCAEvent** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="c38a8-134">The **MSMCAInfo\_RawMCAEvent** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c38a8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c38a8-135">Requirements</span></span>



| <span data-ttu-id="c38a8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c38a8-136">Requirement</span></span> | <span data-ttu-id="c38a8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c38a8-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c38a8-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c38a8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c38a8-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c38a8-139">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="c38a8-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c38a8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c38a8-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c38a8-141">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c38a8-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="c38a8-142">Namespace</span></span><br/>                | <span data-ttu-id="c38a8-143">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="c38a8-143">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="c38a8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c38a8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c38a8-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c38a8-145"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="c38a8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c38a8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c38a8-147"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c38a8-147"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c38a8-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="c38a8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c38a8-149">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="c38a8-149">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="c38a8-150">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="c38a8-150">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

