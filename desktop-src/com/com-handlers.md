---
title: Manipuladores COM
description: A finalidade dos manipuladores COM é fornecer algumas \ 0034; inteligente \ 0034; código no espaço de endereço do cliente que pode otimizar chamadas entre um cliente e um servidor. Os manipuladores podem substituir algumas interfaces ao delegar outras pessoas diretamente ao servidor (por meio do proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105766514"
---
# <a name="com-handlers"></a>Manipuladores COM

A finalidade dos manipuladores COM é fornecer um código "inteligente" no espaço de endereço do cliente que possa otimizar as chamadas entre um cliente e um servidor. Os manipuladores podem substituir algumas interfaces ao delegar outras pessoas diretamente ao servidor (por meio do proxy).

Há dois tipos de manipuladores COM:

-   [O manipulador OLE](the-ole-handler.md) é uma DLL de alta gramatura que fornece serviços importantes para vinculação e inserção. Normalmente, ele é criado antes de o servidor ser iniciado e é inicializado para que o servidor seja ativado quando o objeto inserido entrar no estado de execução.
-   [O manipulador leve do lado do cliente](the-lightweight-client-side-handler.md) pode ser criado para qualquer finalidade, pode ser muito pequeno e não pode ser criado antes do servidor.

 

 




