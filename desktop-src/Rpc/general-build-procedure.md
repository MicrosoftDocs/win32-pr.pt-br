---
title: Procedimento de build geral
description: Página de navegação para o processo de criação de um aplicativo cliente/servidor usando a RPC (Chamada de Procedimento Remoto).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8402a14ceac3b34114e7b40998038a4e09fb7ba1a915c173f2062f7fab9e63d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929624"
---
# <a name="general-build-procedure"></a>Procedimento de build geral

O processo para criar um aplicativo cliente/servidor usando o Microsoft RPC é:

-   Desenvolva a interface .
-   Desenvolva o servidor que implementa a interface .
-   Desenvolva o cliente que usa a interface .

A figura a seguir ilustra essas etapas.

![processo para criar um aplicativo cliente-servidor usando o microsoft rpc](images/appdev.png)

É viável e comum desenvolver os aplicativos cliente e servidor simultaneamente. Como os programas cliente e servidor dependem da interface, no entanto, a interface entre eles deve ser desenvolvida antes que o cliente e o servidor sejam desenvolvidos, conforme mostrado no diagrama anterior.

Esta seção discute as etapas necessárias para criar um aplicativo cliente/servidor com RPC. As informações são apresentadas nos tópicos a seguir:

-   [Desenvolvendo a interface](developing-the-interface.md)
-   [Desenvolvendo o servidor](developing-the-server.md)
-   [Desenvolvendo o cliente](developing-the-client.md)

 

 




