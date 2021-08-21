---
title: Objetos acessíveis
description: Com o Microsoft Acessibilidade Ativa, os elementos da interface do usuário são expostos aos clientes como objetos COM (Component Object Model).
ms.assetid: ab5669c3-33ce-4d56-a028-e36db25c0b28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9591c4884826ba9d85192e5702d0528f25087797faf83d83314d5c00f172459b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994376"
---
# <a name="accessible-objects"></a>Objetos acessíveis

Com o Microsoft Acessibilidade Ativa, os elementos da interface do usuário são expostos aos clientes como objetos COM (Component Object Model). Esses *objetos acessíveis* mantêm partes de informações, chamadas *Propriedades*, que descrevem o nome do objeto, o local da tela e outras informações necessárias aos auxílios de acessibilidade. Os objetos acessíveis também fornecem *métodos* que os clientes chamam para fazer com que o objeto execute alguma ação. Os objetos acessíveis que têm elementos simples associados a eles também são chamados de *pais* ou *contêineres*.

Os objetos acessíveis são implementados usando a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) baseada em com do Microsoft acessibilidade ativa. Os métodos e as propriedades **IAccessible** permitem que os aplicativos cliente obtenham informações sobre elementos de interface do usuário necessários para os usuários. Por exemplo, [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) retorna um ponteiro de interface para um pai de um objeto acessível e [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) fornece um meio para os clientes obterem informações sobre outros objetos em um contêiner.

Para obter mais informações sobre como os objetos acessíveis e os elementos simples estão relacionados, consulte [elementos simples](simple-elements.md).

 

 




