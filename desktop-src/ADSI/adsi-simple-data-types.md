---
title: Tipos de dados simples de ADSI (IADs. h)
description: As interfaces de serviço Active Directory (ADSI) definem e usam os seguintes tipos de dados simples.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5530fda2ca1f4fe967eaf376b668a0bedc29c4b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009006"
---
# <a name="adsi-simple-data-types"></a><span data-ttu-id="5f503-114">Tipos de dados simples de ADSI</span><span class="sxs-lookup"><span data-stu-id="5f503-114">ADSI Simple Data Types</span></span>

<span data-ttu-id="5f503-115">As interfaces de serviço Active Directory (ADSI) definem e usam os seguintes tipos de dados simples.</span><span class="sxs-lookup"><span data-stu-id="5f503-115">Active Directory Service Interfaces (ADSI) defines and uses the following simple data types.</span></span>


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

<span data-ttu-id="5f503-116">**\_booliano do ADS**</span><span class="sxs-lookup"><span data-stu-id="5f503-116">**ADS\_BOOLEAN**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-117">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f503-117">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="5f503-118">**\_cadeia de \_ caracteres exata do caso ADS \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-118">**ADS\_CASE\_EXACT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-119">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5f503-119">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5f503-120">**\_cadeia de \_ caracteres de ignorar caso de anúncios \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-120">**ADS\_CASE\_IGNORE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-121">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5f503-121">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5f503-122">**Cadeia de caracteres de \_ DN do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-122">**ADS\_DN\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-123">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5f503-123">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5f503-124">**\_número inteiro de ADS**</span><span class="sxs-lookup"><span data-stu-id="5f503-124">**ADS\_INTEGER**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-125">DWORD</span><span class="sxs-lookup"><span data-stu-id="5f503-125">DWORD</span></span>

</dd> <dt>

<span data-ttu-id="5f503-126">**\_inteiro grande do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-126">**ADS\_LARGE\_INTEGER**</span></span>
</dt> <dd>

[<span data-ttu-id="5f503-127">**\_inteiro grande**</span><span class="sxs-lookup"><span data-stu-id="5f503-127">**LARGE\_INTEGER**</span></span>](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

<span data-ttu-id="5f503-128">**\_cadeia de \_ caracteres numérica ADS**</span><span class="sxs-lookup"><span data-stu-id="5f503-128">**ADS\_NUMERIC\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-129">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5f503-129">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5f503-130">**\_classe de objeto ADS \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-130">**ADS\_OBJECT\_CLASS**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-131">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5f503-131">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5f503-132">**\_cadeia de caracteres imprimíveis do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-132">**ADS\_PRINTABLE\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-133">LPWSTR</span><span class="sxs-lookup"><span data-stu-id="5f503-133">LPWSTR</span></span>

</dd> <dt>

<span data-ttu-id="5f503-134">**\_identificador de pesquisa do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-134">**ADS\_SEARCH\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="5f503-135">PROCESSAMENTO</span><span class="sxs-lookup"><span data-stu-id="5f503-135">HANDLE</span></span>

</dd> <dt>

<span data-ttu-id="5f503-136">**\_hora UTC do ADS \_**</span><span class="sxs-lookup"><span data-stu-id="5f503-136">**ADS\_UTC\_TIME**</span></span>
</dt> <dd>

[<span data-ttu-id="5f503-137">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="5f503-137">**SYSTEMTIME**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f503-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f503-138">Remarks</span></span>

<span data-ttu-id="5f503-139">Quando a ADSI lê um atributo que foi definido como um **inteiro** no esquema LDAP, ele sempre tratará o inteiro como um valor de 32 bits e poderá truncar os dados.</span><span class="sxs-lookup"><span data-stu-id="5f503-139">When ADSI reads an attribute that has been defined as an **INTEGER** in the LDAP schema, it will always handle the integer as a 32-bit value and may truncate the data.</span></span> <span data-ttu-id="5f503-140">Isso é apenas uma preocupação para servidores LDAP que permitem valores inteiros de tamanho arbitrário.</span><span class="sxs-lookup"><span data-stu-id="5f503-140">This is only a concern for LDAP servers that allow arbitrary sized integer values.</span></span> <span data-ttu-id="5f503-141">Se o atributo for um atributo personalizado definido pela extensão do esquema, esse problema poderá ser evitado definindo o atributo personalizado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5f503-141">If the attribute is a custom attribute defined by extending the schema, this problem can be avoided by defining the custom attribute as a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f503-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f503-142">Requirements</span></span>



| <span data-ttu-id="5f503-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f503-143">Requirement</span></span> | <span data-ttu-id="5f503-144">Valor</span><span class="sxs-lookup"><span data-stu-id="5f503-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5f503-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f503-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5f503-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f503-146">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="5f503-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f503-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5f503-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f503-148">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="5f503-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f503-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f503-150"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f503-150"><dt>Iads.h</dt></span></span> </dl> |



 

