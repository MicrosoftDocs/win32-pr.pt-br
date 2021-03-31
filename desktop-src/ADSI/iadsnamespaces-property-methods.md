---
title: Métodos de propriedade IADsNamespaces (IADs. h)
description: Os métodos de propriedade da interface IADsNamespaces obtêm e definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsNamespaces
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644948"
---
# <a name="iadsnamespaces-property-methods"></a>Métodos de propriedade IADsNamespaces

Os métodos de propriedade da interface [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) obtêm e definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

A propriedade **defaultcontainer** identifica um objeto de contêiner de base ao qual você pode associar e usar como ponto de partida ao navegar. Esses dados são armazenados e recuperados do valor do registro a seguir.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

A ADSI define a propriedade **defaultcontainer** para fornecer uma maneira rápida de obter um ponteiro para um objeto de contêiner ADSI definido anteriormente.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentários

Os provedores devem fornecer essa propriedade de acordo com o usuário. O contêiner padrão é definido imediatamente após a invocação de **IADsNamespaces::p UT \_ defaultcontainer**. Não é necessário chamar [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Na verdade, o objeto namespaces fornecido pelo sistema retorna **E \_ NOTIMPL** para o método **IADs. setinfo** chamado neste objeto. Quando um contêiner é o objeto namespaces, uma operação de enumeração sempre resulta em uma lista de objetos de namespace específicos do provedor. Quando [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) é usado para obter um objeto de namespace, o parâmetro *bstrClass* é ignorado. Isso ocorre porque o contêiner, ou seja, o objeto namespaces, contém apenas um tipo de objeto, ou seja, objetos de namespace específicos do provedor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNamespaces é definido como 28B96BA0-B330-11CF-A9AD-00AA006BC149<br/>       |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[Métodos de propriedade de interface](interface-property-methods.md)
</dt> </dl>

 

 





