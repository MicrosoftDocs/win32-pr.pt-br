---
title: As interfaces IADs e IDirectoryObject
description: Os clientes ADSI gerenciam e manipulam objetos de serviço de diretório usando uma das duas interfaces COM IADs ou IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, sobre
- IDirectoryObject ADSI, sobre
- Interfaces ADSI ADSI , using, IADs e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dccfa643c0076224abece6f449f20caf5a4de5d378c03d37cf0e2248ed5a50b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838376"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>As interfaces IADs e IDirectoryObject

Os clientes ADSI gerenciam e manipulam objetos de serviço de diretório usando uma das duas interfaces COM: [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) ou [**IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) **IADs** é uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) destinada a uso por clientes de limite tardia, como aqueles escritos no Microsoft Visual Basic, Java e várias linguagens de script. **IDirectoryObject** é uma interface vtable que fornece acesso direto a objetos por clientes com limite antecipado, como aqueles escritos em C e C++.

Cada objeto ADSI deve implementar [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) Os clientes ADSI escritos em linguagens como C ou C++, que são capazes de acessar diretamente vtables, podem usar qualquer interface, mas não ambos no mesmo aplicativo. Os clientes ADSI escritos em Visual Basic java ou java estão limitados ao uso **de IADs**.

A [**interface IADs**](/windows/desktop/api/Iads/nn-iads-iads) permite que clientes com limite tardia aproveitem os recursos de manutenção inerentes do modelo de objeto ADSI. Entre esses recursos está o cache de propriedades, que permite que os clientes leiam e escrevam propriedades sem passar pela transmissão de cada chamada. Além disso, os aplicativos cliente têm o uso de bibliotecas de controle ActiveX interface do usuário e um estilo mais simples de programação. Em troca, os clientes com limite tardia devem usar o tipo de dados **VARIANT,** que impede o uso dos tipos de dados nativos mais antigos fornecidos pela ADSI.

A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) permite que os clientes com limite antecipado aproveitem ao máximo os tipos de dados do serviço de diretório nativo, com o custo de uma pequena vantagem de desempenho do uso do cache de propriedades. Em troca, a interface **IDirectoryObject** fornece acesso direto e na conexão às propriedades  do objeto por meio de uma única solicitação, em vez de por meio de chamadas get e **put** individuais.

 

 