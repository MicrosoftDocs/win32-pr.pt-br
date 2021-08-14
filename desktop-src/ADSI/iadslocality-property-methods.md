---
title: Métodos de propriedade IADsLocality (IADs. h)
description: Os métodos da interface IADsLocality lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 5d1cea40-62fb-49d4-857f-4563e9db7f51
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsLocality
topic_type:
- apiref
api_name:
- IADsLocality Property Methods
- IADsLocality.Description
- IADsLocality.get_Description
- IADsLocality.put_Description
- IADsLocality.LocalityName
- IADsLocality.get_LocalityName
- IADsLocality.put_LocalityName
- IADsLocality.PostalAddress
- IADsLocality.get_PostalAddress
- IADsLocality.put_PostalAddress
- IADsLocality.SeeAlso
- IADsLocality.get_SeeAlso
- IADsLocality.put_SeeAlso
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03954f95446dc898c5992c0ac6a16cc9679e363e9574adc2e780d29c90cb26f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428033"
---
# <a name="iadslocality-property-methods"></a>Métodos de propriedade IADsLocality

Os métodos da interface [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality) lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Descrição**
</dt> <dd> <dl>

Indica o texto que descreve a localidade.

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


</dt> </dl> </dd> <dt>

**LocalityName**
</dt> <dd> <dl>

Indica o nome da região geográfica conforme representado por esse objeto de localidade.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LocalityName(
  [out] BSTR* pbstrLocalityName
);
HRESULT put_LocalityName(
  [in] BSTR bstrLocalityName
);
```


</dt> </dl> </dd> <dt>

**PostalAddress**
</dt> <dd> <dl>

Indica o endereço postal principal da localidade.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] BSTR* pbstrPostalAddress
);
HRESULT put_PostalAddress(
  [in] BSTR bstrPostalAddress
);
```


</dt> </dl> </dd> <dt>

**SeeAlso**
</dt> <dd> <dl>

Indica uma matriz de nomes ADsPath de objetos de diretório relevantes para esse objeto.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SeeAlso(
  [out] VARIANT* pvSeeAlso
);
HRESULT put_SeeAlso(
  [in] VARIANT vSeeAlso
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir exibe os dados de localidade de um objeto de contêiner. Ele assume que um objeto de localidade, chamado "mylocality", foi criado para o objeto de contêiner e as propriedades foram definidas.


```VB
Dim dom As IADsContainer
Dim loc As IADsLocality
On Error GoTo Cleanup
 
Set dom = getObject("LDAP://adsrv1/dc=Fabrikam, dc=Com")
Set loc = dom.GetObject("locality","L=myLocality")
Debug.Print loc.Name
Debug.Print loc.LocalityName
Debug.Print loc.Description
Debug.Print loc.PostalAddress
Debug.Print loc.SeeAlso

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set dom = Nothing
    Set loc = Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsLocality é definido como A05E03A2-EFFE-11CF-8ABC-00C04FD8D503<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)
</dt> <dt>

[Métodos de propriedade de interface](interface-property-methods.md)
</dt> </dl>

 

 





