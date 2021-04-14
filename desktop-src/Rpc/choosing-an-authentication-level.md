---
title: Escolhendo um nível de autenticação
description: Ao escolher um nível de autenticação, use a seguinte diretriz.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453573"
---
# <a name="choosing-an-authentication-level"></a>Escolhendo um nível de autenticação

Ao escolher um nível de autenticação, use a seguinte diretriz. Se não importa se os dados enviados podem ser interceptados e modificados e os dados recebidos podem ser interceptados ou modificados, use RPC \_ C \_ Authn \_ nível \_ None, que é o padrão. Se os dados não devem ser modificados e os dados privados não estão sendo enviados ou recebidos, use \_ a \_ integridade do pkt do nível de autenticação RPC C \_ \_ \_ . Em todos os outros casos, use \_ a \_ privacidade do PCT do nível de autenticação RPC C \_ \_ \_ .

Não use o \_ \_ \_ padrão de nível de autenticação RPC c \_ , o RPC \_ c \_ Authn \_ \_ Connect, a \_ chamada de nível RPC c \_ Authn \_ ou o PCT do \_ \_ nível de autenticação RPC c \_ \_ \_ . Um invasor sofisticado pode interromper esses níveis de autenticação e renderizá-los ineficazes. Cada um desses níveis torna um pouco mais difícil para um invasor interceptar e modificar dados, e para representar, mas a segurança não é realmente alcançada. Como o nível de sofisticação de um invasor raramente é conhecido, essas não são opções inteligentes.

 

 




