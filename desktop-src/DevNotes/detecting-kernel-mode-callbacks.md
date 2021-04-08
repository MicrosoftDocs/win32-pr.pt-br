---
description: Se um thread estiver aguardando a conclusão de um retorno de chamada de modo kernel, o lado do modo de usuário do thread será atrasado em uma chamada para a função ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Detectando retornos de chamada Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920475"
---
# <a name="detecting-kernel-mode-callbacks"></a>Detectando retornos de chamada Kernel-Mode

A maior parte do código para o sistema operacional Windows é executada no modo kernel. O modo de processador muda de modo de usuário para modo kernel sempre que um thread de aplicativo chama uma função da API do Windows que, por sua vez, chama uma função interna do sistema que deve ser executada no modo kernel. O modo de processador retorna ao modo de usuário antes de o controle retornar à função para que os dados do sistema sejam protegidos.

Se um thread estiver aguardando a conclusão de um retorno de chamada de modo kernel, o lado do modo de usuário do thread será atrasado em uma chamada para a função **ZwCallbackReturn** .

 

 



