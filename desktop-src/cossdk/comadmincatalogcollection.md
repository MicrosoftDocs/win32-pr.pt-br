---
description: Representa qualquer coleção no catálogo COM+. Use-o para enumerar, adicionar, remover e recuperar itens em uma coleção e para acessar coleções relacionadas.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Classe COMAdminCatalogCollection (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646440"
---
# <a name="comadmincatalogcollection-class"></a>Classe COMAdminCatalogCollection

Representa qualquer coleção no catálogo COM+. Use-o para enumerar, adicionar, remover e recuperar itens em uma coleção e para acessar coleções relacionadas.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|--------------------------------------------------|
| Interfaces | [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a>Quando usar

Use objetos criados a partir da classe **COMAdminCatalogCollection** quando desejar manipular programaticamente uma coleção no catálogo com+. Essas coleções correspondem às pastas na ferramenta de administração de serviços de componentes. Os itens dentro das pastas correspondem a itens em coleções, que você pode representar usando objetos criados a partir da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Para obter informações sobre as coleções no catálogo e suas propriedades, consulte [coleções de administração do com+](com--administration-collections.md).

Para obter uma introdução à administração programática do COM+, consulte [automatizando a administração do com+](automating-com--administration.md).

## <a name="remarks"></a>Comentários

Você não pode criar diretamente um objeto **COMAdminCatalogCollection** . Para usar os métodos desse objeto, você deve criar um objeto [**COMAdminCatalog**](comadmincatalog.md) , obter uma referência a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e, em seguida, usar [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obter uma referência a uma interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa uma coleção de nível superior. Isso é mostrado no exemplo a seguir, em que "TopCollection" deve ser substituído pelo nome de uma das coleções de administração COM+ de nível superior.


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+. Um objeto COMAdminCatalogCollection pode ser criado chamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) em um objeto [**COMAdminCatalog**](comadmincatalog.md) . Isso é mostrado no exemplo a seguir, em que "TopCollection" deve ser substituído pelo nome de uma das coleções de administração COM+ de nível superior.


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>COMAdmin. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




