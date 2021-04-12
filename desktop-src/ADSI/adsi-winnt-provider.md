---
title: Provedor ADSI de WinNT
description: O provedor ADSI da Microsoft implementa um conjunto de objetos ADSI para dar suporte a várias interfaces ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI do provedor do ADSI Winnt
- ADSI do provedor de serviços WinNT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363657"
---
# <a name="adsi-winnt-provider"></a>Provedor ADSI de WinNT

O provedor ADSI da Microsoft implementa um conjunto de objetos ADSI para dar suporte a várias interfaces ADSI. O nome do namespace para o provedor do Windows é "WinNT" e esse provedor é conhecido como o provedor de WinNT. Para acessar o provedor WinNT, associe-se a qualquer um dos [objetos ADSI do Winnt](adsi-objects-of-winnt.md)usando o [ADsPath WinNT](winnt-adspath.md).

O provedor WinNT está incluído no componente do sistema ADSI para Windows e Windows Server.

> [!Note]  
> O provedor WinNT padrão não pode ser considerado totalmente seguro para thread. Os gravadores de aplicativos multissegmentados devem lidar com multithreading para coordenar corretamente qualquer acesso entre threads por meio do uso adequado de objetos de sincronização, como semáforos, exclusões mútuas, seções críticas e assim por diante.

 

 

 




