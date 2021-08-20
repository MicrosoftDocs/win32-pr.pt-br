---
title: Usando a anotação do servidor
description: Este tópico fornece informações sobre como usar a anotação de servidor para especificar um objeto de retorno de chamada.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b2955d49431b502c8587484208321bc1ab1bc0c8201fabf466b60b68f548a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823888"
---
# <a name="using-server-annotation"></a>Usando a anotação do servidor

Este tópico fornece informações sobre como usar a anotação de servidor para especificar um objeto de retorno de chamada.

**Para substituir uma propriedade que especifica um objeto de retorno de chamada**

1.  Obtenha um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o elemento acessível que deve ser anotado.
2.  Chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no elemento acessível para obter um ponteiro de interface [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .
3.  Chame [**IAccIdentity:: GetIdentityString ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) no ponteiro de interface [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) para obter uma cadeia de caracteres que identifica exclusivamente o elemento acessível a ser anotado.
4.  Use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) para criar o objeto [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
5.  Crie um objeto COM (Component Object Model) que implemente [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver).
6.  Chame [**IAccPropServices:: SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver), passando a cadeia de caracteres de identidade, um GUID indicando a propriedade a ser substituída e um ponteiro para o objeto de retorno de chamada [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) .
7.  Ponteiros de interface de versão e memória livre.

Quando um cliente solicita a propriedade do elemento acessível, o objeto de retorno de chamada será chamado e retornará o valor para o cliente.

Como ao especificar um valor, os desenvolvedores de servidor podem usar como alternativa o método [**IAccPropServices:: ComposeHwndIdentityString**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) para obter uma cadeia de caracteres de identidade; ou podem usar o método [**IAccPropServices:: SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) e especificar os parâmetros *HWND*, *idObject* ou *idChild* em vez de uma cadeia de caracteres de identidade.

Ao usar [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) ou [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) em um objeto de contêiner, os desenvolvedores de servidor podem especificar, opcionalmente, que as informações de substituição também devem ser aplicadas a todos os elementos filho desse contêiner.

Os servidores podem limpar explicitamente a anotação a qualquer momento usando [**IAccPropServices:: ClearProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops). Isso geralmente não é necessário, pois o serviço de anotação irá limpar automaticamente e liberar informações de anotação quando o elemento acessível que está sendo anotado desaparecer.

Abaixo está uma lista de propriedades que podem ser anotadas usando este procedimento.

## <a name="properties-supported-when-specifying-a-callback"></a>Propriedades com suporte ao especificar um retorno de chamada

Ao especificar um retorno de chamada, as propriedades a seguir podem ser anotadas. Atualmente, essas propriedades não podem ser anotadas diretamente, especificando um valor.



| Propriedade                      | Tipo                                                             |
|-------------------------------|------------------------------------------------------------------|
| \_nome da ACC de Propid \_             | VT \_ BSTR                                                         |
| \_Descrição da ACC de Propid \_      | VT \_ BSTR                                                         |
| \_função de ACC de Propid \_             | \_I4 VT                                                           |
| \_estado de ACC de Propid \_            | \_I4 VT                                                           |
| \_ajuda de ACC de Propid \_             | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ KEYBOARDSHORTCUT | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ DEFAULTACTION    | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ VALUEMAP         | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ ROLEMAP          | VT \_ BSTR                                                         |
| PROPID \_ ACC \_ STATEMAP         | VT \_ BSTR                                                         |
| foco do PROPID \_ ACC \_            | expedição de VT \_<br/> \_I4 VT<br/>                        |
| \_seleção de ACC de Propid \_        | expedição de VT \_<br/> \_I4 VT<br/> VT \_ desconhecido<br/> |
| \_pai de ACC de Propid \_           | expedição de VT \_                                                     |
| \_NAV ACC do Propid \_ \_          | expedição de VT \_<br/> \_I4 VT<br/>                        |
| navegação do PROPID \_ ACC \_ \_        | expedição de VT \_<br/> \_I4 VT<br/>                        |
| navegação do PROPID \_ ACC \_ \_ à esquerda        | expedição de VT \_<br/> \_I4 VT<br/>                        |
| \_ \_ navegação do Propid ACC \_ direita       | expedição de VT \_<br/> \_I4 VT<br/>                        |
| \_ \_ navegação \_ anterior do Propid ACC        | expedição de VT \_<br/> \_I4 VT<br/>                        |
| PROPID \_ ACC da \_ NAV \_ Next        | expedição de VT \_<br/> \_I4 VT<br/>                        |
| PROPID \_ ACC \_ NAV \_ FIRSTCHILD  | expedição de VT \_<br/> \_I4 VT<br/>                        |
| PROPID \_ ACC \_ NAV \_ LASTCHILD   | expedição de VT \_<br/> \_I4 VT<br/>                        |



 

 

