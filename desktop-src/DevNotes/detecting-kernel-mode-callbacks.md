---
description: Se um thread estiver aguardando a conclusão de um retorno de chamada no modo kernel, o lado do modo de usuário do thread atrasará em uma chamada para a função ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Detectando Kernel-Mode retornos de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029ecf7d5b1f9220de51c2ecffe4bdf30da4cbd088d9d251fd0d24bab04934e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691446"
---
# <a name="detecting-kernel-mode-callbacks"></a>Detectando Kernel-Mode retornos de chamada

A maioria do código para o Windows operacional é executado no modo kernel. O modo de processador alterna do modo de usuário para o modo kernel sempre que um thread de aplicativo chama uma função da API Windows que, por sua vez, chama uma função interna do sistema que deve ser executada no modo kernel. O modo de processador retorna ao modo de usuário antes que o controle retorne à função para que os dados do sistema são protegidos.

Se um thread estiver aguardando a conclusão de um retorno de chamada no modo kernel, o lado do modo de usuário do thread atrasará em uma chamada para a **função ZwCallbackReturn.**

 

 



