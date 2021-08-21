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
ms.openlocfilehash: 0eb0984b150355099e1609481432f01d9b00be110b64bb82d08a938c02acb7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692786"
---
# <a name="adsi-winnt-provider"></a>Provedor ADSI de WinNT

O provedor ADSI da Microsoft implementa um conjunto de objetos ADSI para dar suporte a várias interfaces ADSI. o nome do namespace para o provedor de Windows é "WinNT" e esse provedor é conhecido como o provedor de WinNT. Para acessar o provedor WinNT, associe-se a qualquer um dos [objetos ADSI do Winnt](adsi-objects-of-winnt.md)usando o [ADsPath WinNT](winnt-adspath.md).

o provedor WinNT está incluído no componente do sistema ADSI para Windows e Windows Server.

> [!Note]  
> O provedor WinNT padrão não pode ser considerado totalmente seguro para thread. Os gravadores de aplicativos multissegmentados devem lidar com multithreading para coordenar corretamente qualquer acesso entre threads por meio do uso adequado de objetos de sincronização, como semáforos, exclusões mútuas, seções críticas e assim por diante.

 

 

 




