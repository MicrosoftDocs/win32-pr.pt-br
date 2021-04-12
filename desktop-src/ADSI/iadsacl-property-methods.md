---
title: Métodos de propriedade IADsAcl (IADs. h)
description: O método Property da interface IADsAcl define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsAcl
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d8afb1ba3cbf7749ad8e3d14fa970662715909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455616"
---
# <a name="iadsacl-property-methods"></a><span data-ttu-id="2db79-105">Métodos de propriedade IADsAcl</span><span class="sxs-lookup"><span data-stu-id="2db79-105">IADsAcl Property Methods</span></span>

<span data-ttu-id="2db79-106">O método Property da interface [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) define a propriedade descrita na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2db79-106">The property method of the [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) interface sets the property described in the following table.</span></span> <span data-ttu-id="2db79-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="2db79-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="2db79-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2db79-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="2db79-109">**Direitos**</span><span class="sxs-lookup"><span data-stu-id="2db79-109">**Privileges**</span></span>
<span data-ttu-id="2db79-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="2db79-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="2db79-111">Configurações de privilégio.</span><span class="sxs-lookup"><span data-stu-id="2db79-111">Privilege settings.</span></span>

<dt>

<span data-ttu-id="2db79-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2db79-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2db79-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="2db79-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="2db79-114">**ProtectedAttrName**</span><span class="sxs-lookup"><span data-stu-id="2db79-114">**ProtectedAttrName**</span></span>
<span data-ttu-id="2db79-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="2db79-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="2db79-116">Nome de um atributo protegido.</span><span class="sxs-lookup"><span data-stu-id="2db79-116">Name of a protected attribute.</span></span>

<dt>

<span data-ttu-id="2db79-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2db79-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2db79-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2db79-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="2db79-119">**SubjectName**</span><span class="sxs-lookup"><span data-stu-id="2db79-119">**SubjectName**</span></span>
<span data-ttu-id="2db79-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="2db79-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="2db79-121">Nome do assunto.</span><span class="sxs-lookup"><span data-stu-id="2db79-121">Name of the subject.</span></span>

<dt>

<span data-ttu-id="2db79-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="2db79-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2db79-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2db79-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="2db79-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2db79-124">Requirements</span></span>



| <span data-ttu-id="2db79-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2db79-125">Requirement</span></span> | <span data-ttu-id="2db79-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2db79-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2db79-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2db79-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2db79-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2db79-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2db79-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2db79-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2db79-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2db79-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2db79-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2db79-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2db79-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="2db79-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="2db79-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2db79-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2db79-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2db79-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="2db79-135">IID</span><span class="sxs-lookup"><span data-stu-id="2db79-135">IID</span></span><br/>                      | <span data-ttu-id="2db79-136">IID \_ IADsAcl é definido como 8452D3AB-0869-11D1-A377-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="2db79-136">IID\_IADsAcl is defined as 8452D3AB-0869-11D1-A377-00C04FB950DC</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="2db79-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="2db79-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db79-138">**IADsAcl**</span><span class="sxs-lookup"><span data-stu-id="2db79-138">**IADsAcl**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





