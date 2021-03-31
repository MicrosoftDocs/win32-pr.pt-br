---
title: Acessando o cache de propriedades com interfaces IADsproperty
description: As interfaces IADsproperty consistem em IADsPropertyList, IADsPropertyEntry e IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Acessando o cache de propriedades diretamente com o ADSI de interfaces IADsproperty
- ADSI do cache de propriedades
- ADSI do cache de propriedades, usando as interfaces IADsproperty para acessar o cache de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "103916901"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Acessando o cache de propriedades com interfaces IADsproperty

As interfaces [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) consistem em [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue). Essas interfaces fornecem métodos para acessar e manipular diretamente as propriedades de um cache de objeto. Uma propriedade é conhecida como uma entrada de propriedade e corresponde a um atributo definido no esquema. Uma entrada de propriedade pode ter um ou muitos valores de propriedade. Um conjunto de entradas de propriedade é organizado como uma lista de propriedades.

A interface [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) gerencia a lista de propriedades de um objeto ADSI. A interface [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) executa essa operação para uma entrada de propriedade. Da mesma forma, a interface [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) representa um ou mais valores de propriedade. Juntos, eles fornecem um mecanismo para os usuários:

-   Trabalhe diretamente com o cache de propriedades.
-   Trabalhe com diretórios que não contêm esquemas, como um servidor LDAP versão 2.

As interfaces [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* operam estritamente no cache de propriedades e não fazem nenhuma tentativa de cooperar com o servidor para recuperar ou modificar os dados no repositório persistente. Dessa forma, essas interfaces são usadas apenas para examinar e manipular as propriedades no cache do cliente. Antes de usar essas interfaces, você deve chamar o método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ou o método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) explicitamente para carregar as propriedades do objeto no cache, se o cache não tiver sido inicializado. Depois de chamar os métodos dessas interfaces, você deve chamar [**IADs:: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para persistir as alterações no repositório de diretórios subjacente.

Para obter mais informações e um exemplo de código que pode ser usado para implementar essas interfaces, consulte [código de exemplo para usar interfaces iadsproperty para acessar o cache de propriedades](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).

 

 




