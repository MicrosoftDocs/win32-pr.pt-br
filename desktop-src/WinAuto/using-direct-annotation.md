---
title: Usando anotação direta
description: Usando anotação direta
ms.assetid: d9d78e74-dcab-4974-945f-e8c5d42c04b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8543b5aa4e6beb86b6119d13fe71ad45c1a34776e19095170cb48d8d9f48e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744881"
---
# <a name="using-direct-annotation"></a>Usando anotação direta

**Para usar a anotação direta para substituir o valor de uma propriedade**

1.  Use a função [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ou [CoCreateInstanceEx](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) para criar o objeto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
2.  Chame [**IAccPropServices:: SetHwndProp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndprop), passando o **HWND**, a ID do objeto, a ID filho, a propriedade a ser substituída e uma [variante](/windows/win32/api/oaidl/ns-oaidl-variant) que contém o novo valor da propriedade. Esta etapa anota o valor.
3.  Libere os ponteiros de interface e a memória livre.

O exemplo a seguir mostra como anotar a propriedade [**role**](role-property.md) de um controle de texto estático.


```C++
HRESULT CMyTextControl::SetAccessibleProperties()
{
  // COM is assumed to be initialized...
  IAccPropServices* pAccPropServices = NULL;

  HRESULT hr = CoCreateInstance(CLSID_AccPropServices,
    NULL, CLSCTX_SERVER, IID_IAccPropServices, 
    (void**)&pAccPropServices);

  if (SUCCEEDED(hr))
  {
    // Annotating the Role of this object to be STATICTEXT
    VARIANT var;
    var.vt = VT_I4;
    var.lVal = ROLE_SYSTEM_STATICTEXT;

    hr = pAccPropServices->SetHwndProp(_hwnd,
      OBJID_CLIENT,
      CHILDID_SELF,
      PROPID_ACC_ROLE,
      var);

    pAccPropServices->Release();
  }
  return hr;
}
```



## <a name="properties-supported-when-specifying-a-value"></a>Propriedades com suporte ao especificar um valor

As seguintes propriedades do Microsoft Acessibilidade Ativa podem ser anotadas ao especificar um valor (em que o valor deve ser do tipo anotado) para anotação direta. Para substituir ou adicionar uma propriedade de automação da interface do usuário da Microsoft a um controle, você pode especificar a ID da propriedade de automação da interface do usuário em vez da ID da Propriedade do Microsoft Acessibilidade Ativa. Para obter uma lista de IDs de automação de interface do usuário, consulte [identificadores de propriedade](uiauto-entry-propids.md).



| Propriedade                      | Tipo     |
|-------------------------------|----------|
| \_nome da ACC de Propid \_             | VT \_ BSTR |
| \_Descrição da ACC de Propid \_      | VT \_ BSTR |
| \_função de ACC de Propid \_             | \_I4 VT   |
| \_estado de ACC de Propid \_            | \_I4 VT   |
| \_ajuda de ACC de Propid \_             | VT \_ BSTR |
| PROPID \_ ACC \_ KEYBOARDSHORTCUT | VT \_ BSTR |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR |
| PROPID \_ ACC \_ ROLEMAP          | VT \_ BSTR |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR |



 

 

 