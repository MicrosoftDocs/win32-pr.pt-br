---
title: As interfaces IADs e IDirectoryObject
description: Os clientes ADSI gerenciam e manipulam objetos de serviço de diretório usando uma das duas interfaces COM IADs ou IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, sobre
- IDirectoryObject ADSI, sobre
- Interfaces ADSI ADSI, using, IADs e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dfef47fe1c66e4303725deecec14fe93d1fd92
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823989"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>As interfaces IADs e IDirectoryObject

Os clientes ADSI gerenciam e manipulam objetos de serviço de diretório usando uma das duas interfaces COM: [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) ou [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). **IADs** é uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) destinada a uso por clientes com associação tardia, como as escritas em Microsoft Visual Basic, Java e várias linguagens de script. **IDirectoryObject** é uma interface vtable que fornece acesso direto a objetos por clientes de ligação antecipada, como aqueles escritos em C e C++.

Cada objeto ADSI deve implementar [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Os clientes ADSI escritos em linguagens como C ou C++, que são capazes de acessar diretamente vtables, podem usar qualquer interface, mas não ambos no mesmo aplicativo. Os clientes ADSI escritos em Visual Basic ou Java são limitados ao uso de **IADs**.

A interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) permite que os clientes de ligação tardia tirem proveito dos recursos de manutenção inerentes do modelo de objeto ADSI. Entre esses recursos está o cache de propriedades, que permite que os clientes leiam e gravem Propriedades sem passar pelo fio para cada chamada. Além disso, os aplicativos cliente têm o uso de uma interface do usuário e de bibliotecas de controles ActiveX poderosas e um estilo mais simples de programação. Em retorno, os clientes de ligação tardia devem usar o tipo de dados **Variant** , que impede o uso de tipos de dados nativos mais avançados fornecidos pela ADSI.

A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) permite que os clientes de ligação inicial aproveitem ao máximo os tipos de dados nativos do serviço de diretório no custo de uma ligeira vantagem de desempenho de usar o cache de propriedades. Em retorno, a interface **IDirectoryObject** fornece acesso direto e durante a transmissão às propriedades do objeto por meio de uma única solicitação, em vez de chamadas **Get** e **Put** individuais.

 

 