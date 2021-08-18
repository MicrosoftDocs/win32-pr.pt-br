---
title: Acessando o cache de propriedades com interfaces IADsProperty
description: As interfaces IADsProperty consistem em IADsPropertyList, IADsPropertyEntry e IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Acessando o cache de propriedades diretamente com a ADSI de interfaces IADsProperty
- ADSI de cache de propriedade
- ADSI do cache de propriedades, usando interfaces IADsProperty para acessar o cache de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a68cd77a10d6631b52e48ed19650dd5cd18dff0ee59ba2332db73b7fce1a8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024114"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Acessando o cache de propriedades com interfaces IADsProperty

As [**interfaces IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) consistem em [**IADsPropertyList,**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)e [**IADsPropertyValue.**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) Essas interfaces fornecem métodos para acessar e manipular diretamente as propriedades de um cache de objeto. Uma propriedade é conhecida como uma entrada de propriedade e corresponde a um atributo definido no esquema. Uma entrada de propriedade pode ter um ou muitos valores de propriedade. Um conjunto de entradas de propriedade é organizado como uma lista de propriedades.

A [**interface IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) gerencia a lista de propriedades de um objeto ADSI. A [**interface IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) executa essa operação para uma entrada de propriedade. Da mesma forma, a interface [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) representa um ou mais valores de propriedade. Juntos, eles fornecem um mecanismo para que os usuários:

-   Trabalhe diretamente com o cache de propriedade.
-   Trabalhe com diretórios que não contêm esquemas, como um servidor LDAP versão 2.

As [**interfaces IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) operam estritamente no cache de propriedades e não fazem nenhuma tentativa de cooperação com o servidor para recuperar ou modificar os dados no \* armazenamento persistente. Assim, essas interfaces são usadas apenas para examinar e manipular propriedades no cache do cliente. Antes de usar essas interfaces, você deve chamar o método [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou o método [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) explicitamente para carregar as propriedades do objeto no cache, se o cache não tiver sido inicializado. Depois de chamar os métodos dessas interfaces, você deve chamar [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para persistir as alterações no armazenamento de diretórios subjacente.

Para obter mais informações e um exemplo de código que pode ser usado para implementar essas interfaces, consulte Código de exemplo para usar [interfaces IADsProperty para](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md)acessar o Cache de Propriedades .

 

 




