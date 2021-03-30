---
title: Métodos de propriedade IADsPropertyValue (IADs. h)
description: Os métodos de propriedade da interface IADsPropertyValue fornecem acesso às propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 1039d4a9-bef8-457d-9a32-3743c14adef1
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPropertyValue
topic_type:
- apiref
api_name:
- IADsPropertyValue Property Methods
- IADsPropertyValue.ADsType
- IADsPropertyValue.get_ADsType
- IADsPropertyValue.put_ADsType
- IADsPropertyValue.DNString
- IADsPropertyValue.get_DNString
- IADsPropertyValue.put_DNString
- IADsPropertyValue.CaseExactString
- IADsPropertyValue.get_CaseExactString
- IADsPropertyValue.put_CaseExactString
- IADsPropertyValue.CaseIgnoreString
- IADsPropertyValue.get_CaseIgnoreString
- IADsPropertyValue.put_CaseIgnoreString
- IADsPropertyValue.PrintableString
- IADsPropertyValue.get_PrintableString
- IADsPropertyValue.put_PrintableString
- IADsPropertyValue.NumericString
- IADsPropertyValue.get_NumericString
- IADsPropertyValue.put_NumericString
- IADsPropertyValue.Boolean
- IADsPropertyValue.get_Boolean
- IADsPropertyValue.put_Boolean
- IADsPropertyValue.Integer
- IADsPropertyValue.get_Integer
- IADsPropertyValue.put_Integer
- IADsPropertyValue.OctetString
- IADsPropertyValue.get_OctetString
- IADsPropertyValue.put_OctetString
- IADsPropertyValue.SecurityDescriptor
- IADsPropertyValue.get_SecurityDescriptor
- IADsPropertyValue.put_SecurityDescriptor
- IADsPropertyValue.LargeInteger
- IADsPropertyValue.get_LargeInteger
- IADsPropertyValue.put_LargeInteger
- IADsPropertyValue.UTCTime
- IADsPropertyValue.get_UTCTime
- IADsPropertyValue.put_UTCTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196e8097e5beaa5350738971be29de89b43c17a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455025"
---
# <a name="iadspropertyvalue-property-methods"></a><span data-ttu-id="1b826-105">Métodos de propriedade IADsPropertyValue</span><span class="sxs-lookup"><span data-stu-id="1b826-105">IADsPropertyValue Property Methods</span></span>

<span data-ttu-id="1b826-106">Os métodos de propriedade da interface [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) fornecem acesso às propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b826-106">The property methods of the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface provide access to the properties described in the following table.</span></span> <span data-ttu-id="1b826-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1b826-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1b826-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b826-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="1b826-109">**ADsType**</span><span class="sxs-lookup"><span data-stu-id="1b826-109">**ADsType**</span></span>
<span data-ttu-id="1b826-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-111">O tipo de dados do valor da propriedade, extraído da enumeração [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) , da propriedade Value.</span><span class="sxs-lookup"><span data-stu-id="1b826-111">The data type of the value of the property, taken from the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration, of the value property.</span></span>

<dt>

<span data-ttu-id="1b826-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="1b826-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* ADsType
);
HRESULT put_ADsType(
  [in] LONG ADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-114">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="1b826-114">**Boolean**</span></span>
<span data-ttu-id="1b826-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-116">$True.</span><span class="sxs-lookup"><span data-stu-id="1b826-116">Boolean value.</span></span>

<dt>

<span data-ttu-id="1b826-117">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-118">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="1b826-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Boolean(
  [out] LONG* lnBoolean
);
HRESULT put_Boolean(
  [in] LONG lnBoolean
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-119">**CaseExactString**</span><span class="sxs-lookup"><span data-stu-id="1b826-119">**CaseExactString**</span></span>
<span data-ttu-id="1b826-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-121">Cadeia de caracteres a ser interpretada.</span><span class="sxs-lookup"><span data-stu-id="1b826-121">String to be interpreted.</span></span> <span data-ttu-id="1b826-122">Diferenciar maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1b826-122">Case-sensitive.</span></span>

<dt>

<span data-ttu-id="1b826-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-124">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b826-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseExactString(
  [out] BSTR* bstrCaseExactString
);
HRESULT put_CaseExactString(
  [in] BSTR bstrCaseExactString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-125">**CaseIgnoreString**</span><span class="sxs-lookup"><span data-stu-id="1b826-125">**CaseIgnoreString**</span></span>
<span data-ttu-id="1b826-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-127">Cadeia de caracteres a ser interpretada.</span><span class="sxs-lookup"><span data-stu-id="1b826-127">String to be interpreted.</span></span> <span data-ttu-id="1b826-128">Não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1b826-128">Case insensitive.</span></span>

<dt>

<span data-ttu-id="1b826-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-130">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b826-130">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreString(
  [out] BSTR* bstrCaseIgnoreString
);
HRESULT put_CaseIgnoreString(
  [in] BSTR bstrCaseIgnoreString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-131">**DNString**</span><span class="sxs-lookup"><span data-stu-id="1b826-131">**DNString**</span></span>
<span data-ttu-id="1b826-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-133">Cadeia de caracteres que identifica o nome distinto (caminho) de um objeto de valor do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="1b826-133">String that identifies the distinguished name (path) of a directory service value object.</span></span>

<dt>

<span data-ttu-id="1b826-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-135">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b826-135">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* bstrDNString
);
HRESULT put_DNString(
  [in] BSTR bstrDNString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-136">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="1b826-136">**Integer**</span></span>
<span data-ttu-id="1b826-137"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-137"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-138">Valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="1b826-138">Integer value.</span></span>

<dt>

<span data-ttu-id="1b826-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-140">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="1b826-140">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Integer(
  [out] LONG* lnInteger
);
HRESULT put_Integer(
  [in] LONG lnInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-141">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="1b826-141">**LargeInteger**</span></span>
<span data-ttu-id="1b826-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-143">Ponteiro para a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) do objeto que implementa [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) para esse valor.</span><span class="sxs-lookup"><span data-stu-id="1b826-143">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) for this value.</span></span>

<dt>

<span data-ttu-id="1b826-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-145">Tipo de dados de script: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1b826-145">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LargeInteger(
  [out] IDispatch** ppLargeInteger
);
HRESULT put_LargeInteger(
  [in] IDispatch* pLargeInteger
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-146">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="1b826-146">**NumericString**</span></span>
<span data-ttu-id="1b826-147"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-147"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-148">Texto a ser interpretado.</span><span class="sxs-lookup"><span data-stu-id="1b826-148">Text to be interpreted.</span></span> <span data-ttu-id="1b826-149">Tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="1b826-149">Numeric type.</span></span>

<dt>

<span data-ttu-id="1b826-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-151">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b826-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NumericString(
  [out] BSTR* bstrNumericString
);
HRESULT put_NumericString(
  [in] BSTR bstrNumericString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-152">**Octetstring**</span><span class="sxs-lookup"><span data-stu-id="1b826-152">**OctetString**</span></span>
<span data-ttu-id="1b826-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-154">Matriz variante de caracteres de um byte.</span><span class="sxs-lookup"><span data-stu-id="1b826-154">Variant array of one-byte characters.</span></span>

<dt>

<span data-ttu-id="1b826-155">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-156">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1b826-156">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetString(
  [in] VARIANT* vOctetString
);
HRESULT put_OctetString(
  [in] VARIANT* vOctetString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-157">**Imenablestring**</span><span class="sxs-lookup"><span data-stu-id="1b826-157">**PrintableString**</span></span>
<span data-ttu-id="1b826-158"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-158"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-159">Exibir ou imprimir cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1b826-159">Display or print string.</span></span>

<dt>

<span data-ttu-id="1b826-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-161">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1b826-161">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintableString(
  [out] BSTR* bstrPrintableString
);
HRESULT put_PrintableString(
  [in] BSTR bstrPrintableString
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-162">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1b826-162">**SecurityDescriptor**</span></span>
<span data-ttu-id="1b826-163"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-163"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-164">Ponteiro para a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) do objeto que implementa [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) para esse valor.</span><span class="sxs-lookup"><span data-stu-id="1b826-164">Pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface of the object implementing [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) for this value.</span></span>

<dt>

<span data-ttu-id="1b826-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-166">Tipo de dados de script: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1b826-166">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SecurityDescriptor(
  [out] IDispatch** ppSecurityDescriptor
);
HRESULT put_SecurityDescriptor(
  [in] IDispatch* pSecurityDescriptor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1b826-167">**UTCTime**</span><span class="sxs-lookup"><span data-stu-id="1b826-167">**UTCTime**</span></span>
<span data-ttu-id="1b826-168"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1b826-168"></dt> <dd> <dl></span></span>

<span data-ttu-id="1b826-169">Uma data do tipo **de \_ Data VT** expresso no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="1b826-169">A date of the **VT\_DATE** type expressed in Coordinated Universal Time (UTC) format.</span></span>

<dt>

<span data-ttu-id="1b826-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b826-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b826-171">Tipo de dados de script: **Data**</span><span class="sxs-lookup"><span data-stu-id="1b826-171">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UTCTime(
  [out] DATE* daUTCTime
);
HRESULT put_UTCTime(
  [in] DATE daUTCTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="1b826-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b826-172">Remarks</span></span>

<span data-ttu-id="1b826-173">As propriedades [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) só definirão ou recuperarão um valor de Propriedade do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="1b826-173">The [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) properties will only set or retrieve a property value of the specified type.</span></span> <span data-ttu-id="1b826-174">Por exemplo, a propriedade **CaseIgnoreString** em um atributo do tipo **cadeia \_ de \_ caracteres de DN ADSTYPE**, como o atributo **distinguishedName** , resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="1b826-174">For example, the **CaseIgnoreString** property on an attribute of type **ADSTYPE\_DN\_STRING**, like the **distinguishedName** attribute, will result in an error.</span></span> <span data-ttu-id="1b826-175">A propriedade **CaseIgnoreString** só funcionará em atributos do tipo **ADS, \_ caso ignore a cadeia de \_ \_ caracteres**.</span><span class="sxs-lookup"><span data-stu-id="1b826-175">The **CaseIgnoreString** property will only work on attributes of type **ADS\_CASE\_IGNORE\_STRING**.</span></span> <span data-ttu-id="1b826-176">A tabela a seguir mapeia o valor [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) para a propriedade **IADsPropertyValue** correspondente que pode ser usada para acessar esse tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="1b826-176">The following table maps the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value to the corresponding **IADsPropertyValue** property that can be used to access that attribute type.</span></span> <span data-ttu-id="1b826-177">Se um valor de **ADSTYPEENUM** não estiver listado nesta tabela, ele não estará disponível na interface **IADsPropertyValue** .</span><span class="sxs-lookup"><span data-stu-id="1b826-177">If an **ADSTYPEENUM** value is not listed in this table, it is not available from the **IADsPropertyValue** interface.</span></span> <span data-ttu-id="1b826-178">A interface [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) deve ser usada para obter dados nos outros formatos.</span><span class="sxs-lookup"><span data-stu-id="1b826-178">The [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interface should be used to obtain data in the other formats.</span></span>



| <span data-ttu-id="1b826-179">Valor de [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)</span><span class="sxs-lookup"><span data-stu-id="1b826-179">[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) value</span></span> | <span data-ttu-id="1b826-180">Propriedade [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)</span><span class="sxs-lookup"><span data-stu-id="1b826-180">[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) property</span></span> |
|------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1b826-181">**\_cadeia de \_ caracteres DN ADSTYPE**</span><span class="sxs-lookup"><span data-stu-id="1b826-181">**ADSTYPE\_DN\_STRING**</span></span>                  | <span data-ttu-id="1b826-182">**DNString**</span><span class="sxs-lookup"><span data-stu-id="1b826-182">**DNString**</span></span>                                            |
| <span data-ttu-id="1b826-183">**\_cadeia de \_ caracteres exata do caso de ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="1b826-183">**ADSTYPE\_CASE\_EXACT\_STRING**</span></span>         | <span data-ttu-id="1b826-184">**CaseExactString**</span><span class="sxs-lookup"><span data-stu-id="1b826-184">**CaseExactString**</span></span>                                     |
| <span data-ttu-id="1b826-185">**\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="1b826-185">**ADSTYPE\_CASE\_IGNORE\_STRING**</span></span>        | <span data-ttu-id="1b826-186">**CaseIgnoreString**</span><span class="sxs-lookup"><span data-stu-id="1b826-186">**CaseIgnoreString**</span></span>                                    |
| <span data-ttu-id="1b826-187">**\_cadeia de caracteres imprimível do ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="1b826-187">**ADSTYPE\_PRINTABLE\_STRING**</span></span>           | <span data-ttu-id="1b826-188">**Imenablestring**</span><span class="sxs-lookup"><span data-stu-id="1b826-188">**PrintableString**</span></span>                                     |
| <span data-ttu-id="1b826-189">**\_cadeia de \_ caracteres numérica ADSTYPE**</span><span class="sxs-lookup"><span data-stu-id="1b826-189">**ADSTYPE\_NUMERIC\_STRING**</span></span>             | <span data-ttu-id="1b826-190">**NumericString**</span><span class="sxs-lookup"><span data-stu-id="1b826-190">**NumericString**</span></span>                                       |
| <span data-ttu-id="1b826-191">**ADSTYPE \_ booliano**</span><span class="sxs-lookup"><span data-stu-id="1b826-191">**ADSTYPE\_BOOLEAN**</span></span>                     | <span data-ttu-id="1b826-192">**Booliano**</span><span class="sxs-lookup"><span data-stu-id="1b826-192">**Boolean**</span></span>                                             |
| <span data-ttu-id="1b826-193">**ADSTYPE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="1b826-193">**ADSTYPE\_INTEGER**</span></span>                     | <span data-ttu-id="1b826-194">**Inteiro**</span><span class="sxs-lookup"><span data-stu-id="1b826-194">**Integer**</span></span>                                             |
| <span data-ttu-id="1b826-195">**Cadeia de caracteres de \_ OCTETO ADSTYPE \_**</span><span class="sxs-lookup"><span data-stu-id="1b826-195">**ADSTYPE\_OCTET\_STRING**</span></span>               | <span data-ttu-id="1b826-196">**Octetstring**</span><span class="sxs-lookup"><span data-stu-id="1b826-196">**OctetString**</span></span>                                         |
| <span data-ttu-id="1b826-197">**ADSTYPE \_ \_ hora UTC**</span><span class="sxs-lookup"><span data-stu-id="1b826-197">**ADSTYPE\_UTC\_TIME**</span></span>                   | <span data-ttu-id="1b826-198">**UTCTime**</span><span class="sxs-lookup"><span data-stu-id="1b826-198">**UTCTime**</span></span>                                             |
| <span data-ttu-id="1b826-199">**\_inteiro grande \_ ADSTYPE**</span><span class="sxs-lookup"><span data-stu-id="1b826-199">**ADSTYPE\_LARGE\_INTEGER**</span></span>              | <span data-ttu-id="1b826-200">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="1b826-200">**LargeInteger**</span></span>                                        |
| <span data-ttu-id="1b826-201">**\_ \_ descritor de segurança do ADSTYPE NT \_**</span><span class="sxs-lookup"><span data-stu-id="1b826-201">**ADSTYPE\_NT\_SECURITY\_DESCRIPTOR**</span></span>    | <span data-ttu-id="1b826-202">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1b826-202">**SecurityDescriptor**</span></span>                                  |



 

## <a name="examples"></a><span data-ttu-id="1b826-203">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1b826-203">Examples</span></span>

<span data-ttu-id="1b826-204">O exemplo de código a seguir mostra como recuperar uma propriedade da lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1b826-204">The following code example shows how to retrieve a property from the property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Retrieve the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Retrieve a property entry. If you are certain of the property type,
' replace ADSTYPE_UNKNOWN with the actual property type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Print the property entry values.
For Each v In propEntry.Values
    Set propVal = v
    Select Case propVal.ADsType
        Case ADSTYPE_CASE_EXACT_STRING
            Debug.Print propVal.CaseExactString
        Case ADSTYPE_CASE_IGNORE_STRING
            Debug.Print propVal.CaseIgnoreString
        Case Else
            Debug.Print "Unable to handle a property of type: " & propVal.ADsType
    End Select
    
Next

Cleanup:
    If (Err.Number<>0) Then
       Debug.Print "An error has occurred. " & Err.Number
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="1b826-205">O código a seguir mostra como usar **IADsPropertyValue:: get \_ CaseIgnoreString** para recuperar o valor da Propriedade Description de uma lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1b826-205">The following code shows how to use **IADsPropertyValue::get\_CaseIgnoreString** to retrieve the value of the description property from a property list.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart = 0;
LONG lend = 0;
LONG lADsType = ADSTYPE_UNKNOWN;
 
VariantInit(&var);
VariantInit(&varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);

if(FAILED(hr)){goto Cleanup;}

// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}

pObj->GetInfo();
pObj->Release();
 
// Retrieve the property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), ADSTYPE_CASE_IGNORE_STRING, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}

hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Retrieve the value array of the property entry.
hr = pEntry->get_Values(&var);
if(FAILED(hr)){goto Cleanup;}

SAFEARRAY *sa = V_ARRAY( &var );
 
// Retrieve the lower and upper bound. Iterate and print the values.
hr = SafeArrayGetLBound( sa, 1, &lstart );
hr = SafeArrayGetUBound( sa, 1, &lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx < lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &idx, &varItem );
    hr = V_DISPATCH(&varItem)->QueryInterface(IID_IADsPropertyValue,
                                              (void**)&pVal);
    if(FAILED(hr)){goto Cleanup;}

    pVal->get_ADsType(&lADsType);

    switch(lADsType)
    {
        case ADSTYPE_CASE_IGNORE_STRING:
        {
            hr = pVal->get_CaseIgnoreString(&valStr);
            break;
        }
        case ADSTYPE_CASE_EXACT_STRING:
        {
            hr = pVal->get_CaseExactString(&valStr);
            break;
        }
        default:
        {
            valStr = SysAllocString(L"Unable to handle a property of this type");
            break;
        }
    }

    if(FAILED(hr)){goto Cleanup;}
    printf(" %S ", valStr);
    SysFreeString(valStr);
    VariantClear(&varItem);
}
printf("\n");

Cleanup:
    if(pList)
        pList = NULL;

    if(pEntry)
        pEntry = NULL;

    if(pVal)
        pVal = NULL;

    if(pObj)
        pObj = NULL;

    if(pEnum)
        pEnum = NULL;

    SysFreeString(valStr);
    VariantClear(&varItem);
    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="1b826-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b826-206">Requirements</span></span>



| <span data-ttu-id="1b826-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b826-207">Requirement</span></span> | <span data-ttu-id="1b826-208">Valor</span><span class="sxs-lookup"><span data-stu-id="1b826-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b826-209">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b826-209">Minimum supported client</span></span><br/> | <span data-ttu-id="1b826-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b826-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b826-211">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b826-211">Minimum supported server</span></span><br/> | <span data-ttu-id="1b826-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b826-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b826-213">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1b826-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b826-214"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b826-214"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="1b826-215">DLL</span><span class="sxs-lookup"><span data-stu-id="1b826-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b826-216"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b826-216"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="1b826-217">IID</span><span class="sxs-lookup"><span data-stu-id="1b826-217">IID</span></span><br/>                      | <span data-ttu-id="1b826-218">IID \_ IADsPropertyValue é definido como 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="1b826-218">IID\_IADsPropertyValue is defined as 79FA9AD0-A97C-11D0-8534-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="1b826-219">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1b826-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b826-220">**IADsPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="1b826-220">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="1b826-221">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="1b826-221">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="1b826-222">**IADsPropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="1b826-222">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="1b826-223">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="1b826-223">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="1b826-224">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="1b826-224">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="1b826-225">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1b826-225">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="1b826-226">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1b826-226">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

