---
title: Interfaces duplas (ADSI)
description: Use interfaces COM para acessar as propriedades e os métodos em qualquer objeto ADSI do provedor.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d1cf89ef07e573be8f59805034ff8c567e75fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884057"
---
# <a name="dual-interfaces-adsi"></a>Interfaces duplas (ADSI)

Use interfaces COM para acessar as propriedades e os métodos em qualquer objeto ADSI do provedor. Uma propriedade somente leitura é mapeada para uma entrada de interface do formulário **Get \_ &lt; PropertyName &gt;**. Uma propriedade de leitura/gravação é mapeada para duas entradas de interface do formulário **Get \_ &lt; &gt; PropertyName** e **Put \_ &lt; PropertyName &gt;**.

Todos os métodos em uma interface COM devem:

-   Retornar um valor HRESULT para indicar êxito ou falha. O tipo **HRESULT** é abordado na especificação com.
-   Em chamadas para **QueryInterface**, retorna **E \_ nointerface** para interfaces não implementadas.
-   Retornar **E \_ NOTIMPL** para métodos não implementados em interfaces que, de outra forma, são implementadas.
-   **\_ \_ \_ Não \_ há** suporte para retornar a propriedade Ads para propriedades de interface que não têm suporte.

Para manter a compatibilidade com os controladores de automação, todos os parâmetros e tipos de retorno devem estar dentro do subconjunto definido pelo tipo de dados variante de automação. Para obter mais informações, consulte **Variant** e **VARIANTARG** no SDK (Software Development Kit) da plataforma.

Um provedor Active Directory objeto pode expor interfaces que usam tipos de dados diferentes daqueles no subconjunto de **variantes** . no entanto, os controladores de automação, como Visual Basic, não são capazes de chamar essas interfaces. A maioria das interfaces de provedor ADSI é derivada de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e pode ser usada como ponteiros de interface **IDispatch** . No entanto, as interfaces ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)e [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) não são derivadas de **IDispatch**.

 

 
