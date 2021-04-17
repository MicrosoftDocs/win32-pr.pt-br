---
description: A resiliência é a capacidade de um aplicativo de se recuperar normalmente de situações em que um componente vital está faltando ou foi substituído por uma versão incompatível.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resiliência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757112"
---
# <a name="resiliency"></a>Resiliência

A resiliência é a capacidade de um aplicativo de se recuperar normalmente de situações em que um componente vital está faltando ou foi substituído por uma versão incompatível. Ao criar um pacote de instalação e usar as [funções do instalador](installer-functions.md), os desenvolvedores podem usar o Windows Installer para produzir aplicativos resilientes capazes de se recuperar dessas situações.

-   Use a lista de origem do instalador para aumentar a resiliência de aplicativos que dependem de recursos de rede. Para obter mais informações, consulte [resiliência de origem](source-resiliency.md).
-   Use a API do instalador para verificar se um recurso, componente, arquivo ou versão de arquivo vital está instalado.
-   Use a API do instalador para verificar o caminho para um componente em tempo de execução. Isso reduz a dependência do aplicativo em caminhos de arquivo estáticos, que normalmente são diferentes entre computadores.
-   Use o instalador para reinstalar atalhos danificados, entradas de registro e outros componentes sem precisar executar a instalação novamente.
-   Aumente a resiliência da instalação do produto, deixando o recurso de reversão do instalador habilitado. Para obter mais informações, consulte [Rollback Installation](rollback-installation.md).

 

 



