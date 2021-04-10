---
title: Métodos de propriedade IADsClass (IADs. h)
description: Os métodos de propriedade da interface IADsClass obtêm ou definem as propriedades a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 191f6873-c4bd-4e71-9d23-478454b7cec2
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsClass
topic_type:
- apiref
api_name:
- IADsClass Property Methods
- IADsClass.Abstract
- IADsClass.get_Abstract
- IADsClass.put_Abstract
- IADsClass.AuxDerivedFrom
- IADsClass.get_AuxDerivedFrom
- IADsClass.put_AuxDerivedFrom
- IADsClass.Auxiliary
- IADsClass.get_Auxiliary
- IADsClass.put_Auxiliary
- IADsClass.CLSID
- IADsClass.get_CLSID
- IADsClass.put_CLSID
- IADsClass.Container
- IADsClass.get_Container
- IADsClass.put_Container
- IADsClass.Containment
- IADsClass.get_Containment
- IADsClass.put_Containment
- IADsClass.DerivedFrom
- IADsClass.get_DerivedFrom
- IADsClass.put_DerivedFrom
- IADsClass.HelpFileContext
- IADsClass.get_HelpFileContext
- IADsClass.put_HelpFileContext
- IADsClass.HelpFileName
- IADsClass.get_HelpFileName
- IADsClass.put_HelpFileName
- IADsClass.MandatoryProperties
- IADsClass.get_MandatoryProperties
- IADsClass.put_MandatoryProperties
- IADsClass.NamingProperties
- IADsClass.get_NamingProperties
- IADsClass.put_NamingProperties
- IADsClass.OID
- IADsClass.get_OID
- IADsClass.put_OID
- IADsClass.OptionalProperties
- IADsClass.get_OptionalProperties
- IADsClass.put_OptionalProperties
- IADsClass.PossibleSuperiors
- IADsClass.get_PossibleSuperiors
- IADsClass.put_PossibleSuperiors
- IADsClass.PrimaryInterface
- IADsClass.get_PrimaryInterface
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358bc33347f035af92303a4ce9879105cd247a3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086047"
---
# <a name="iadsclass-property-methods"></a>Métodos de propriedade IADsClass

Os métodos de propriedade da interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) obtêm ou definem as propriedades a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Resumo**
</dt> <dd> <dl>

Valor booliano que indica se essa classe é abstrata ou não abstrata. Quando **true**, essa classe é uma classe abstrata e não pode ser instanciada diretamente no serviço de diretório. Classes abstratas só podem ser usadas como superclasses.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **booliano**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Abstract(
  [out] BOOLEAN* pbAbstract
);
HRESULT put_Abstract(
  [in] BOOLEAN bAbstract
);
```


</dt> </dl> </dd> <dt>

**AuxDerivedFrom**
</dt> <dd> <dl>

Matriz de cadeias de caracteres ADsPath que indicam as classes superauxiliares das quais essa classe deriva.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AuxDerivedFrom(
  [out] VARIANT* pvAuxDerivedFrom
);
HRESULT put_AuxDerivedFrom(
  [in] VARIANT vAuxDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**Auxiliar**
</dt> <dd> <dl>

Valor booliano que indica se esta classe é auxiliar ou não. Quando **true**, essa classe é uma classe auxiliar e não pode ser instanciada diretamente no serviço de diretório. As classes auxiliares só podem ser usadas como superclasses de outras classes auxiliares ou como uma fonte de propriedades adicionais em classes estruturais.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **booliano**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Auxiliary(
  [out] BOOLEAN* pbAuxiliary
);
HRESULT put_Auxiliary(
  [in] BOOLEAN bAuxiliary
);
```


</dt> </dl> </dd> <dt>

**CLSID**
</dt> <dd> <dl>

CLSID opcional específico do provedor que identifica o objeto COM que implementa essa classe.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CLSID(
  [out] BSTR* pbstrCLSID
);
HRESULT put_CLSID(
  [in] BSTR bstrCLSID
);
```


</dt> </dl> </dd> <dt>

**Contêiner**
</dt> <dd> <dl>

Valor booliano que indica se essa classe pode ser um contêiner de outras classes de objeto. Se esse valor for **true**, você poderá chamar o método **Get \_ container** para obter uma matriz das classes de objeto que essa classe pode conter.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **booliano**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Container(
  [out] BOOLEAN* pbContainer
);
HRESULT put_Container(
  [in] BOOLEAN bContainer
);
```


</dt> </dl> </dd> <dt>

**Contenção**
</dt> <dd> <dl>

Uma matriz **BSTR** na qual cada elemento é o nome de uma classe de objeto que essa classe pode conter.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Containment(
  [out] VARIANT* pvContainment
);
HRESULT put_Containment(
  [in] VARIANT vContainment
);
```


</dt> </dl> </dd> <dt>

**DerivedFrom**
</dt> <dd> <dl>

Matriz de cadeias de caracteres ADsPath que indicam as classes das quais essa classe foi derivada.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DerivedFrom(
  [out] VARIANT* pvDerivedFrom
);
HRESULT put_DerivedFrom(
  [in] VARIANT vDerivedFrom
);
```


</dt> </dl> </dd> <dt>

**HelpFileContext**
</dt> <dd> <dl>

ID de contexto dentro de **helpfilename** onde informações específicas para essa classe podem ser encontradas.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileContext(
  [out] long* plHelpContext
);
HRESULT put_HelpFileContext(
  [in] long lHelpContext
);
```


</dt> </dl> </dd> <dt>

**Arquivodeajudaname**
</dt> <dd> <dl>

Nome de um arquivo de ajuda que contém mais informações sobre objetos desta classe.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HelpFileName(
  [out] BSTR* pbstrHelpFileName
);
HRESULT put_HelpFileName(
  [in] BSTR bstrHelpFileName
);
```


</dt> </dl> </dd> <dt>

**Obrigatórioproperties**
</dt> <dd> <dl>

**SafeArray** de **Variant** s que lista as propriedades que devem ser definidas para essa classe a ser gravada no armazenamento. Se a classe contiver apenas uma propriedade, **obter \_ obrigatórioproperties** retornará um **BSTR**.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MandatoryProperties(
  [out] VARIANT* pvarMandatoryProperties
);
HRESULT put_MandatoryProperties(
  [in] VARIANT varMandatoryProperties
);
```


</dt> </dl> </dd> <dt>

**Nome da nomenclatura**
</dt> <dd> <dl>

**SafeArray** de **BSTR** s que lista as propriedades usadas para nomear atributos dessa classe de esquema.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NamingProperties(
  [out] VARIANT* pvarNamingProperties
);
HRESULT put_NamingProperties(
  [in] VARIANT varNamingProperties
);
```


</dt> </dl> </dd> <dt>

**OIDs**
</dt> <dd> <dl>

Identificador de objeto específico do provedor que define essa classe. Isso é fornecido para permitir a extensão do esquema, usando Active Directory, em serviços de diretório que exigem OIDs específicos do provedor para classes.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* pbstrOID
);
HRESULT put_OID(
  [in] BSTR bstrOID
);
```


</dt> </dl> </dd> <dt>

**OptionalProperties**
</dt> <dd> <dl>

**SafeArray** de **Variant** s que lista as propriedades opcionais para esta classe de esquema. Se a classe contiver apenas uma propriedade, então, **obter \_ OptionalProperties** retornará um **BSTR**.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OptionalProperties(
  [out] VARIANT* pvarOptionalProperties
);
HRESULT put_OptionalProperties(
  [in] VARIANT varOptionalProperties
);
```


</dt> </dl> </dd> <dt>

**PossibleSuperiors**
</dt> <dd> <dl>

Matriz de cadeias de caracteres ADsPath que indicam as classes de esquema que podem conter instâncias dessa classe.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PossibleSuperiors(
  [out] VARIANT* pvSuperiors
);
HRESULT put_PossibleSuperiors(
  [in] VARIANT vSuperiors
);
```


</dt> </dl> </dd> <dt>

**PrimaryInterface**
</dt> <dd> <dl>

GUID de identificador específico do provedor opcional que associa uma interface a objetos desta classe de esquema. Por exemplo, a classe "user" que dá suporte a [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) e **PrimaryInterface** é identificada pelo **IID \_ IADsUser**. Isso deve estar no formato de cadeia de caracteres padrão de um GUID, conforme definido pelo COM. Esse GUID é o valor que aparece na propriedade [**IADs:: get \_ GUID**](/windows/desktop/api/Iads/nn-iads-iads) em instâncias dessa classe para provedores que implementam essa propriedade. A identificação de uma classe de esquema por IID da interface primária do código de classe permite o uso de **QueryInterface** em tempo de execução para determinar se um objeto é da classe desejada.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrimaryInterface(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como usar a interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) para determinar se um objeto pode ser um contêiner e, em caso afirmativo, lista os nomes de quaisquer objetos contidos.


```VB
Dim ads As IADs
Dim cls As IADsClass

On Error GoTo Cleanup

Set ads = GetObject("WinNT://myComputer,computer")
Set cls = GetObject(ads.Schema)
if cls.Container = True Then
    MsgBox "This object contains the following children:"
    For Each o In cls.Containment
        MsgBox o
    Next
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ads = Nothing
    Set cls = Nothing
```



O exemplo de código a seguir mostra como usar a interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) para determinar se um objeto pode ser um contêiner e, em caso afirmativo, lista os nomes de quaisquer objetos contidos.


```C++
HRESULT hr = S_OK;
IADsClass *pCls = NULL;
IADs *pADs = NULL;
BSTR bstrSchema;
VARIANT var;
 
hr = CoInitialize(NULL);
hr = ADsGetObject(L"WinNT://myComputer,computer",
                  IID_IADs,
                  (void**)&pADs);
if (FAILED(hr)) {goto Cleanup;}
 
hr = pADs->get_Schema(&bstrSchema);
pADs->Release();
if(FAILED(hr)) {goto Cleanup;}
 
hr = ADsGetObject(bstrSchema, IID_IADsClass, (void**)&pCls);
if(FAILED(hr)) {goto Cleanup;}
 
VariantInit(&var);
VARIANT_BOOL bCont;
pCls->get_Container(&bCont);
if(bCont != false) {
    VariantClear(&var);
    pCls->get_Containment(&var);
    hr = printVarArray(var);
}

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    SysFreeString(bstrSchema);
    CoUninitialize();
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsClass é definido como C8F93DD0-4AE0-11CF-9E73-00AA004A5691<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[**IADsClass:: qualificadores**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers)
</dt> </dl>

 

 





