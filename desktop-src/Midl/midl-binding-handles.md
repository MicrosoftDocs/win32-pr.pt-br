---
title: Identificadores de associação de MIDL
description: Identificadores de associação são objetos de dados que representam a associação entre o cliente e o servidor.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- tipos de dados MIDL, identificadores de associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007380"
---
# <a name="midl-binding-handles"></a>Identificadores de associação de MIDL

Identificadores de associação são objetos de dados que representam a associação entre o cliente e o servidor.

MIDL dá suporte ao manipulador de tipo base [**\_ t**](handle-t.md). Os identificadores desse tipo são conhecidos como "identificadores primitivos".

Você pode definir seus próprios tipos de identificador usando o atributo **\[ Handle \]** . Os identificadores definidos dessa forma são conhecidos como identificadores "definidos pelo usuário" ou "personalizados" ou "genéricos".

Você também pode definir um identificador que mantém informações de estado usando o atributo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** . Os identificadores definidos dessa maneira são conhecidos como identificadores de "contexto".

Se nenhuma informação de estado for necessária e você não optar por chamar as bibliotecas de tempo de execução RPC para gerenciar o identificador, você poderá solicitar que as bibliotecas de tempo de execução forneçam associação automática. Isso é feito usando o **\[** [**\_ identificador automático**](auto-handle.md)de palavra-chave ACF **\]** .

Você pode especificar uma variável global como o identificador de associação usando o **\[** [**\_ identificador implícito**](implicit-handle.md)da palavra-chave ACF **\]** . A palavra-chave de **\[ \_ identificador \] explícita** é usada para declarar que cada função remota tem um identificador explicitamente especificado.

Para obter mais informações, consulte [Binding e Handles](/windows/desktop/Rpc/binding-and-handles).

 

 