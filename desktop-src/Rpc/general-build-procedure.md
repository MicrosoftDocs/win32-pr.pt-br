---
title: Procedimento de Build geral
description: Página de navegação para o processo de criação de um aplicativo cliente/servidor usando RPC (chamada de procedimento remoto).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005393"
---
# <a name="general-build-procedure"></a>Procedimento de Build geral

O processo para criar um aplicativo cliente/servidor usando o Microsoft RPC é:

-   Desenvolva a interface.
-   Desenvolva o servidor que implementa a interface.
-   Desenvolva o cliente que usa a interface.

A figura a seguir ilustra essas etapas.

![processo para criar um aplicativo cliente-servidor usando o Microsoft RPC](images/appdev.png)

É viável e comum desenvolver aplicativos cliente e servidor simultaneamente. Como os programas cliente e servidor dependem da interface, no entanto, a interface entre eles deve ser desenvolvida antes que o cliente e o servidor sejam desenvolvidos, conforme mostrado no diagrama anterior.

Esta seção aborda as etapas necessárias para a criação de um aplicativo cliente/servidor com RPC. As informações são apresentadas nos seguintes tópicos:

-   [Desenvolvendo a interface](developing-the-interface.md)
-   [Desenvolvendo o servidor](developing-the-server.md)
-   [Desenvolvendo o cliente](developing-the-client.md)

 

 




