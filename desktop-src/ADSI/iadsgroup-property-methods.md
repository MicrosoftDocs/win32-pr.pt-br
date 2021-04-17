---
title: Métodos de propriedade IADs (IADs. h)
description: Métodos de propriedade da interface IADs.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- ADSI dos métodos de propriedade de IADs
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
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755902"
---
# <a name="iadsgroup-property-methods"></a>Métodos de propriedade IADs

Os métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iadsgroup) lêem e gravam as propriedades a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Descrição**
</dt> <dd> <dl>

Indica a descrição textual da Associação de grupo.

<dt>

Tipo de acesso: leitura/gravação
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

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a>Usando o IADs para recuperar descrições de grupos internos

Os exemplos a seguir mostram como recuperar informações sobre objetos de grupo do Windows por nome. Em um ambiente multilíngue, os grupos internos são, às vezes, conhecidos por diferentes nomes localizados, o que significa que eles não podem ser recuperados diretamente usando identificadores de cadeia de caracteres como "WinNT://Microsoft/Administrators". Nesse caso, o usuário pode se associar ao objeto SID conhecido para o grupo, recuperar o nome do grupo localizado e fornecê-lo ao método GetObject. Para obter mais informações, consulte [SIDs conhecidos](/windows/desktop/SecAuthZ/well-known-sids).

## <a name="examples"></a>Exemplos

O exemplo a seguir Visual Basic mostra como associar a um objeto de grupo e exibir a descrição do grupo.


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



O exemplo de C++ a seguir mostra como associar a um objeto de grupo e exibir a descrição do grupo.


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
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | \_O IID IADs é definido como 27636B00-410f-11CF-B1FF-02608C9E7553<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[Métodos de propriedade de interface](interface-property-methods.md)
</dt> </dl>

 

