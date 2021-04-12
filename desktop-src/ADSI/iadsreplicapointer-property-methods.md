---
title: Métodos de propriedade IADsReplicaPointer (IADs. h)
description: O método Property da interface IADsReplicaPointer define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: fc520ea4-b2c2-44c0-8bec-25f8d4a77074
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsReplicaPointer
topic_type:
- apiref
api_name:
- IADsReplicaPointer Property Methods
- IADsReplicaPointer.ServerName
- IADsReplicaPointer.get_ServerName
- IADsReplicaPointer.put_ServerName
- IADsReplicaPointer.ReplicaType
- IADsReplicaPointer.get_ReplicaType
- IADsReplicaPointer.put_ReplicaType
- IADsReplicaPointer.ReplicaNumber
- IADsReplicaPointer.get_ReplicaNumber
- IADsReplicaPointer.put_ReplicaNumber
- IADsReplicaPointer.Count
- IADsReplicaPointer.get_Count
- IADsReplicaPointer.put_Count
- IADsReplicaPointer.ReplicaAddressHints
- IADsReplicaPointer.get_ReplicaAddressHints
- IADsReplicaPointer.put_ReplicaAddressHints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044d5a5f1b87d42accb7e8e6e6c83eeda69eb5e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499336"
---
# <a name="iadsreplicapointer-property-methods"></a><span data-ttu-id="80566-105">Métodos de propriedade IADsReplicaPointer</span><span class="sxs-lookup"><span data-stu-id="80566-105">IADsReplicaPointer Property Methods</span></span>

<span data-ttu-id="80566-106">O método Property da interface [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="80566-106">The property method of the [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer) interface sets the property described in the following table.</span></span> <span data-ttu-id="80566-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="80566-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="80566-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="80566-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="80566-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="80566-109">**Count**</span></span>
<span data-ttu-id="80566-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="80566-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="80566-111">O número de réplicas existentes.</span><span class="sxs-lookup"><span data-stu-id="80566-111">The number of existing replicas.</span></span>

<dt>

<span data-ttu-id="80566-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="80566-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80566-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="80566-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* retval
);
HRESULT put_Count(
  [in] LONG lnCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="80566-114">**ReplicaAddressHints**</span><span class="sxs-lookup"><span data-stu-id="80566-114">**ReplicaAddressHints**</span></span>
<span data-ttu-id="80566-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="80566-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="80566-116">Um endereço de rede Sugerido como uma referência provável a um nó que leva ao servidor de nomes.</span><span class="sxs-lookup"><span data-stu-id="80566-116">A network address suggested as a likely reference to a node leading to the name server.</span></span>

<dt>

<span data-ttu-id="80566-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="80566-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80566-118">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="80566-118">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaAddressHints(
  [out] VARIANT* retval
);
HRESULT put_ReplicaAddressHints(
  [in] VARIANT vReplicaAddressHints
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="80566-119">**ReplicaNumber**</span><span class="sxs-lookup"><span data-stu-id="80566-119">**ReplicaNumber**</span></span>
<span data-ttu-id="80566-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="80566-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="80566-121">Número de identificação da réplica.</span><span class="sxs-lookup"><span data-stu-id="80566-121">Identification number of the replica.</span></span>

<dt>

<span data-ttu-id="80566-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="80566-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80566-123">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="80566-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaNumber(
  [out] LONG* retval
);
HRESULT put_ReplicaNumber(
  [in] LONG lnReplicaNumber
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="80566-124">**Réplicatype**</span><span class="sxs-lookup"><span data-stu-id="80566-124">**ReplicaType**</span></span>
<span data-ttu-id="80566-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="80566-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="80566-126">Tipo de réplica (Mestre, secundário ou somente leitura.)</span><span class="sxs-lookup"><span data-stu-id="80566-126">Type of replica (master, secondary, or read-only.)</span></span>

<dt>

<span data-ttu-id="80566-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="80566-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80566-128">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="80566-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ReplicaType(
  [out] LONG* retval
);
HRESULT put_ReplicaType(
  [in] LONG lnType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="80566-129">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="80566-129">**ServerName**</span></span>
<span data-ttu-id="80566-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="80566-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="80566-131">Nome do servidor de nomes que contém a réplica.</span><span class="sxs-lookup"><span data-stu-id="80566-131">Name of the name server holding the replica.</span></span>

<dt>

<span data-ttu-id="80566-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="80566-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="80566-133">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="80566-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServerName(
  [out] BSTR* retVal
);
HRESULT put_ServerName(
  [in] BSTR bstrServerName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="80566-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80566-134">Requirements</span></span>



| <span data-ttu-id="80566-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="80566-135">Requirement</span></span> | <span data-ttu-id="80566-136">Valor</span><span class="sxs-lookup"><span data-stu-id="80566-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80566-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80566-137">Minimum supported client</span></span><br/> | <span data-ttu-id="80566-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80566-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80566-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80566-139">Minimum supported server</span></span><br/> | <span data-ttu-id="80566-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80566-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80566-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80566-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="80566-142"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="80566-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="80566-143">DLL</span><span class="sxs-lookup"><span data-stu-id="80566-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80566-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80566-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="80566-145">IID</span><span class="sxs-lookup"><span data-stu-id="80566-145">IID</span></span><br/>                      | <span data-ttu-id="80566-146">IID \_ IADsReplicaPointer é definido como F60FB803-4080-11D1-A3AC-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="80566-146">IID\_IADsReplicaPointer is defined as F60FB803-4080-11D1-A3AC-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="80566-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="80566-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80566-148">**IADsReplicaPointer**</span><span class="sxs-lookup"><span data-stu-id="80566-148">**IADsReplicaPointer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)
</dt> <dt>

[<span data-ttu-id="80566-149">**\_REPLICAPOINTER ADS**</span><span class="sxs-lookup"><span data-stu-id="80566-149">**ADS\_REPLICAPOINTER**</span></span>](/windows/win32/api/iads/ns-iads-ads_replicapointer)
</dt> </dl>

 

 





