---
title: Métodos de propriedade IADs (IADs. h)
description: Os métodos de propriedade da interface IADs obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADs ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499259"
---
# <a name="iads-property-methods"></a>Métodos de propriedade IADs

Os métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**ADsPath**
</dt> <dd> <dl>

A cadeia de caracteres ADsPath deste objeto. A cadeia de caracteres identifica exclusivamente esse objeto em um ambiente de rede. O objeto sempre pode ser recuperado usando esse caminho.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

**Classe**
</dt> <dd> <dl>

O nome da classe de esquema de objeto.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

**GUID**
</dt> <dd> <dl>

O identificador global exclusivo do objeto de diretório. A interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) converte o **GUID** de uma cadeia de caracteres de octeto, como armazenado em um servidor de diretório, em um formato de cadeia de caracteres.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

**Nome**
</dt> <dd> <dl>

O nome relativo do objeto como nomeado no serviço de diretório subjacente. Esse nome distingue esse objeto de seus irmãos.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

**Pai**
</dt> <dd> <dl>

A cadeia de caracteres ADsPath do contêiner pai. Active Directory não permite a formação do ADsPath de um determinado objeto concatenando as propriedades **pai** e **nome** . Embora essa operação possa funcionar em alguns provedores, não há garantia de que ele funcione para todas as implementações. É garantido que o ADsPath seja válido e sempre deve ser usado para recuperar o ponteiro de interface de um objeto.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

**Esquema**
</dt> <dd> <dl>

A cadeia de caracteres ADsPath do objeto de classe de esquema deste objeto.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentários

Em Active Directory, o **GUID** RETORNADO de GUID é uma cadeia de caracteres hexadecimais. Use o **GUID** resultante para associar diretamente ao objeto.


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



em que xxx é o valor retornado da propriedade GUID. Para obter mais informações, consulte [usando objectGUID para associar a um objeto](/windows/desktop/AD/using-objectguid-to-bind-to-an-object). Lembre-se de que, se você usar um GUID para associar a um objeto, o método de propriedade **ADsPath** retornará valores diferentes dos valores normais que seriam retornados se você usava um DN (nome distinto) para ligar ao mesmo objeto. Por exemplo, a tabela a seguir lista os valores retornados ao usar os dois métodos de associação diferentes para associar ao mesmo objeto de usuário.



|             | Associar usando DN                                           | Associar usando GUID                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| **Nome**    | CN = Jeff Smith                                           | CN = Jeff Smith                                               |
| **Pai**  | LDAP://server/CN=Users,DC=Fabrikam,DC=com               | LDAP://server/CN=Users,DC=Fabrikam,DC=com                   |
| **ADsPath** | LDAP://server/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com | LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7> |



 

> [!Note]  
> O provedor WinNT não dá suporte à vinculação usando o **GUID** do objeto e retorna a propriedade **GUID** em um formato de cadeia de caracteres ligeiramente diferente.

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como recuperar dados de objeto usando métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



O exemplo de código a seguir mostra como recuperar dados de objeto usando métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



O exemplo de código a seguir mostra como trabalhar com os métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADs é definido como FD8256D0-FD15-11CE-ABC4-02608C9E7553<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

