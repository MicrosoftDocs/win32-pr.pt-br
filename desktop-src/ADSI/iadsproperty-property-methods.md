---
title: Métodos da propriedade IADsproperty (IADs. h)
description: Leia e grave as propriedades descritas na tabela a seguir.
ms.assetid: dd348a3c-0386-4fa2-984d-cdea6f09bd72
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADsproperty ADSI
topic_type:
- apiref
api_name:
- IADsProperty Property Methods
- IADsProperty.OID
- IADsProperty.get_OID
- IADsProperty.put_OID
- IADsProperty.Syntax
- IADsProperty.get_Syntax
- IADsProperty.put_Syntax
- IADsProperty.MaxRange
- IADsProperty.get_MaxRange
- IADsProperty.put_MaxRange
- IADsProperty.MinRange
- IADsProperty.get_MinRange
- IADsProperty.put_MinRange
- IADsProperty.MultiValued
- IADsProperty.get_MultiValued
- IADsProperty.put_MultiValued
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233bd5411e1c82956ef745255418a1b176af5900
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771761"
---
# <a name="iadsproperty-property-methods"></a>Métodos da propriedade IADsproperty

Os métodos de propriedade da interface [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) lêem e gravam as propriedades descritas na tabela a seguir. Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**MaxRange**
</dt> <dd> <dl>

Limite superior de valores.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxRange(
  [out] LONG* lnMaxRange
);
HRESULT put_MaxRange(
  [in] LONG lnMaxRange
);
```


</dt> </dl> </dd> <dt>

**MinRange**
</dt> <dd> <dl>

Limite inferior de valores.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinRange(
  [out] LONG* lnMinRange
);
HRESULT put_MinRange(
  [in] LONG lnMinRange
);
```


</dt> </dl> </dd> <dt>

**Múltiplos valores**
</dt> <dd> <dl>

Se a propriedade oferece suporte a valores únicos ou múltiplos.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados Scripting: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MultiValued(
  [out] VARIANT_BOOL* fMultivalued
);
HRESULT put_MultiValued(
  [in] VARIANT_BOOL fMultivalued
);
```


</dt> </dl> </dd> <dt>

**OIDs**
</dt> <dd> <dl>

Identificador de objeto específico do diretório.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* bstrOID
);
HRESULT put_OID(
  [out] BSTR* bstrOID
);
```


</dt> </dl> </dd> <dt>

**Sintaxe**
</dt> <dd> <dl>

Caminho relativo do objeto de sintaxe.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Syntax(
  [out] BSTR* bstrSyntax
);
HRESULT put_Syntax(
  [in] BSTR* bstrSyntax
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir examina o atributo **OperatingSystem** de um computador em uma rede por meio do provedor Winnt.


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sc As IADsContainer

On Error GoTo Cleanup
 
Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystem")
 
MsgBox "Attribute:  " & pr.Name
MsgBox "Syntax:     " & pr.Syntax
MsgBox "MaxRange:   " & pr.MaxRange
MsgBox "MinRange:   " & pr.MinRange
MsgBox "Multivalued:" & pr.Multivalued

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sc = Nothing
```



O exemplo de código a seguir examina o atributo **OperatingSystem** de um computador em uma rede por meio do provedor Winnt. Para brevidade, a verificação de erros é omitida.


```C++
IADs *pADs = NULL;
IADsClass *pCls = NULL;
IADsProperty* pProp = NULL;
IADsContainer *pCont = NULL;
long lval;
short bval;
HRESULT hr = CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine,computer",
                  IID_IADs, (void**)&pADs);
if(FAILED(hr))
    goto Cleanup;

BSTR bstr;
hr = pADs->get_Schema(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsClass, (void**)&pCls);
hr = pCls->get_Parent(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr))
    goto Cleanup;
SysFreeString(bstr);

hr = pCont->GetObject(CComBSTR("Property"), CComBSTR("OperatingSystem"), (IDispatch**)&pProp);
if(FAILED(hr))
    goto Cleanup;

hr = pProp->get_Name(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Name : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_Syntax(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Syntax : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_MaxRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MaxRange : %d\n",lval);
SysFreeString(bstr);

hr = pProp->get_MinRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MinRange : %d\n", lval);
SysFreeString(bstr);

hr = pProp->get_Multivalued(&bval);
if(FAILED(hr))
    goto Cleanup;
printf(" MultiValued : %b\n",bval);
SysFreeString(bstr);

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    if(pCont)
        pCont->Release();

    if(pProp)
        pProp->Release(); 
 
CoUninitialize();
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsproperty é definido como C8F93DD3-4AE0-11CF-9E73-00AA004A5691<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





