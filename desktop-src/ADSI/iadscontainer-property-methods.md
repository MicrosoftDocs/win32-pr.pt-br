---
title: Métodos de propriedade IADsContainer (Iads.h)
description: Os métodos de propriedade da interface IADsContainer obterão ou definirão as propriedades descritas na tabela a seguir. Para obter mais informações e uma discussão geral sobre métodos de propriedade, consulte Métodos de propriedade de interface.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- ADSI (métodos de propriedade IADsContainer)
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13515bcf90c926db839aad60d49599967ee0d24bedbe0deb4b7d1d21c3c016e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428081"
---
# <a name="iadscontainer-property-methods"></a>Métodos de propriedade IADsContainer

Os métodos de propriedade da interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) obterão ou definirão as propriedades descritas na tabela a seguir. Para obter mais informações e uma discussão geral sobre métodos de propriedade, consulte [Métodos de propriedade de interface](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Count**
</dt> <dd> <dl>

Recupera o número de itens no contêiner. Quando **Filter** é definido, **Count** retorna apenas o número de itens filtrados.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

**Filter**
</dt> <dd> <dl>

Recupera ou define o filtro usado para selecionar classes de objeto em uma determinada enumeração. Essa é uma matriz variante, cada elemento do qual é o nome de uma classe de esquema. Se **Filter** não estiver definido ou definido como vazio, todos os objetos de todas as classes serão recuperados pelo enumerador.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

**Dicas**
</dt> <dd> <dl>

Uma matriz variante de cadeias **de caracteres BSTR.** Cada elemento identifica o nome de uma propriedade encontrada na definição de esquema. O *parâmetro vHints* permite que o cliente indique quais atributos carregar para cada objeto enumerado. Esses dados podem ser usados para otimizar o acesso à rede. No entanto, a implementação exata é específica do provedor e atualmente não é usada pelo provedor WinNT.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentários

Os processos de enumeração em [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) e **IADsContainer::get \_ Count** são executados em relação aos objetos contidos no cache. Quando um contêiner contém um grande número de objetos, o desempenho pode ser afetado. Para melhorar o desempenho, desligue o cache, configurar um tamanho de página apropriado e use a interface [**IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Por esse motivo, não há suporte para a propriedade **\_ get Count** no provedor LDAP da Microsoft.

## <a name="examples"></a>Exemplos

O exemplo Visual Basic código a seguir mostra como métodos de propriedade de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) podem ser usados.


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



O exemplo de código C++ a seguir mostra como os métodos de propriedade de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) podem ser usados. Para a brevidade, a verificação de erros é omitida.


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID IADsContainer é definido como \_ 001677D0-FD16-11CE-ABC4-02608C9E7553<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[**Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





