---
title: Métodos de propriedade IADsGroup (Iads.h)
description: Métodos de propriedade da interface IADsGroup.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADsGroup ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f15a55765a10afef10087e7b28d04304ab0cc2668915a6e6ffa71fc770eb54a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082400"
---
# <a name="iadsgroup-property-methods"></a>Métodos de propriedade IADsGroup

Os métodos de propriedade da interface [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) leem e escrevem as propriedades a seguir. Para obter mais informações, consulte [Métodos de propriedade de interface](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Descrição**
</dt> <dd> <dl>

Indica a descrição textual da associação de grupo.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentários

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Usando IADsGroup para recuperar descrições de grupos internos

Os exemplos a seguir mostram como recuperar informações sobre Windows de grupo por nome. Em um ambiente multilíngue, grupos integrados às vezes são conhecidos por nomes localizados diferentes, o que significa que eles não podem ser recuperados diretamente usando identificadores de cadeia de caracteres, como "WinNT://Microsoft/Administrators". Nesse caso, o usuário pode se vincular ao objeto SID conhecido do grupo, recuperar o nome do grupo localizado e fornecioná-lo ao método GetObject. Para obter mais informações, consulte [SIDs conhecidos.](/windows/desktop/SecAuthZ/well-known-sids)

## <a name="examples"></a>Exemplos

O exemplo Visual Basic a seguir mostra como se vincular a um objeto de grupo e exibir a descrição do grupo.


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



O exemplo C++ a seguir mostra como se vincular a um objeto de grupo e exibir a descrição do grupo.


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID IADsGroup é definido como \_ 27636B00-410F-11CF-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Métodos de propriedade interface](interface-property-methods.md)
</dt> </dl>

 

