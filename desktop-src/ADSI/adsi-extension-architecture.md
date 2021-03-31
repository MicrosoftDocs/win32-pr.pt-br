---
title: Arquitetura de extensão ADSI
description: As extensões ADSI são baseadas no modelo de agregação com, com vários aprimoramentos. As extensões devem aderir a todas as regras COM. Para obter mais informações, consulte a especificação COM.
ms.assetid: 59e39273-1f66-4bdd-89ed-31947a268d1f
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, arquitetura de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377409f4b9ac36d72d6885e89860b9e6e680b103
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641846"
---
# <a name="adsi-extension-architecture"></a>Arquitetura de extensão ADSI

As extensões ADSI são baseadas no modelo de agregação com, com vários aprimoramentos. As extensões devem aderir a todas as regras COM. Para obter mais informações, consulte a especificação COM.

Aqui está uma revisão do modelo de agregação COM.

![modelo de agregação com](images/comagmod.png)

Uma agregação, também conhecida como objeto interno, é um objeto criado por um agregador. O objeto de extensão é uma agregação.

Um agregador, também conhecido como objeto externo, é um objeto que cria uma agregação. ADSI é um agregador.

O objeto interno Delega seu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para o **IUnknown** do agregador.

Extensões ADSI adicionam os seguintes aprimoramentos à agregação COM para atender aos seus requisitos:

-   Permite que cada gravador de extensão estenda objetos ADSI. Um gravador de extensão pode registrar sua extensão com ADSI e não ser afetado pela existência de outras extensões. No modelo de agregação COM, o agregador deve ter o CLSID da agregação. A ADSI ameniza esse requisito fazendo com que ele atue como o agregador para todas as extensões. Portanto, em vez de formar uma camada de componentes aninhados, as extensões estão no mesmo nível.
-   Permite um objeto, um IDispatch. O suporte à automação é um dos recursos mais importantes do ADSI. O suporte à automação é obtido porque a ADSI dá suporte à interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Os gravadores de extensão são incentivados a dar suporte à interface **IDispatch** . No entanto, deve haver apenas uma interface **IDispatch** em um determinado objeto. A ADSI integra e coleta as muitas interfaces **IDispatch** de extensões diferentes e as apresenta como um **IDispatch** consistente para o controlador de automação. Cada extensão, quando agregada, deve rotear novamente suas chamadas **IDispatch** para o **IDISPATCH** fornecido pela ADSI.

Todas essas soluções são possíveis devido aos serviços que o Gerenciador de objetos do ADSI fornece, que residem em cada provedor ADSI.

A figura a seguir mostra a arquitetura do modelo de extensão ADSI.

![arquitetura de modelo de extensão ADSI](images/adsiexmo.png)

A ADSI dá suporte a dois níveis de extensão:

-   Suporte de ligação antecipada. Esse é o primeiro nível de extensão. Uma extensão deve dar suporte ao registro e implementar novas interfaces. Os consumidores de extensão devem usar ferramentas ou hosts de script que dão suporte à associação inicial, por exemplo, Visual C++ Visual Basic.
-   Suporte à ligação tardia. Isso acontece quando uma extensão atende a todos os requisitos de associação antecipada e implementa uma interface adicional, [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension). Implementadores de extensão podem usar qualquer ferramenta que opere como um controlador de automação, como o Windows Script Host, Active Server páginas ou HTML com VBScript.

 

 