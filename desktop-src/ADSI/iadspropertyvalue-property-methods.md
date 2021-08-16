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
ms.openlocfilehash: aaa64ef7d7802306902060a9eb0e2423f3155ba032115c831212403cda658784
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427612"
---
# <a name="iadspropertyvalue-property-methods"></a>Métodos de propriedade IADsPropertyValue

Os métodos de propriedade da interface [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) fornecem acesso às propriedades descritas na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**ADsType**
</dt> <dd> <dl>

O tipo de dados do valor da propriedade, extraído da enumeração [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) , da propriedade Value.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
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

**Booliano**
</dt> <dd> <dl>

$True.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
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

**CaseExactString**
</dt> <dd> <dl>

Cadeia de caracteres a ser interpretada. Diferenciar maiúsculas de minúsculas.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
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

**CaseIgnoreString**
</dt> <dd> <dl>

Cadeia de caracteres a ser interpretada. Não diferencia maiúsculas de minúsculas.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
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

**DNString**
</dt> <dd> <dl>

Cadeia de caracteres que identifica o nome distinto (caminho) de um objeto de valor do serviço de diretório.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
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

**Inteiro**
</dt> <dd> <dl>

Valor inteiro.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
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

**LargeInteger**
</dt> <dd> <dl>

Ponteiro para a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) do objeto que implementa [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) para esse valor.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **IDispatch**
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

**NumericString**
</dt> <dd> <dl>

Texto a ser interpretado. Tipo numérico.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
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

**Octetstring**
</dt> <dd> <dl>

Matriz variante de caracteres de um byte.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
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

**Imenablestring**
</dt> <dd> <dl>

Exibir ou imprimir cadeia de caracteres.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
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

**SecurityDescriptor**
</dt> <dd> <dl>

Ponteiro para a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) do objeto que implementa [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) para esse valor.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **IDispatch**
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

**UTCTime**
</dt> <dd> <dl>

Uma data do tipo **de \_ Data VT** expresso no formato UTC (tempo Universal Coordenado).

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Data**
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

 

## <a name="remarks"></a>Comentários

As propriedades [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) só definirão ou recuperarão um valor de Propriedade do tipo especificado. Por exemplo, a propriedade **CaseIgnoreString** em um atributo do tipo **cadeia \_ de \_ caracteres de DN ADSTYPE**, como o atributo **distinguishedName** , resultará em um erro. A propriedade **CaseIgnoreString** só funcionará em atributos do tipo **ADS, \_ caso ignore a cadeia de \_ \_ caracteres**. A tabela a seguir mapeia o valor [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) para a propriedade **IADsPropertyValue** correspondente que pode ser usada para acessar esse tipo de atributo. Se um valor de **ADSTYPEENUM** não estiver listado nesta tabela, ele não estará disponível na interface **IADsPropertyValue** . A interface [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) deve ser usada para obter dados nos outros formatos.



| Valor de [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) | Propriedade [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) |
|------------------------------------------|---------------------------------------------------------|
| **\_cadeia de \_ caracteres DN ADSTYPE**                  | **DNString**                                            |
| **\_cadeia de \_ caracteres exata do caso de ADSTYPE \_**         | **CaseExactString**                                     |
| **\_cadeia de \_ caracteres de ignorar caso de ADSTYPE \_**        | **CaseIgnoreString**                                    |
| **\_cadeia de caracteres imprimível do ADSTYPE \_**           | **Imenablestring**                                     |
| **\_cadeia de \_ caracteres numérica ADSTYPE**             | **NumericString**                                       |
| **ADSTYPE \_ booliano**                     | **Booliano**                                             |
| **ADSTYPE \_ inteiro**                     | **Inteiro**                                             |
| **Cadeia de caracteres de \_ OCTETO ADSTYPE \_**               | **Octetstring**                                         |
| **ADSTYPE \_ \_ hora UTC**                   | **UTCTime**                                             |
| **\_inteiro grande \_ ADSTYPE**              | **LargeInteger**                                        |
| **\_ \_ descritor de segurança do ADSTYPE NT \_**    | **SecurityDescriptor**                                  |



 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como recuperar uma propriedade da lista de propriedades.


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



O código a seguir mostra como usar **IADsPropertyValue:: get \_ CaseIgnoreString** para recuperar o valor da Propriedade Description de uma lista de propriedades.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPropertyValue é definido como 79FA9AD0-A97C-11D0-8534-00C04FD8D503<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

