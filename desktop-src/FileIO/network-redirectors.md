---
description: Descreve a funcionalidade de um redirecionador de rede.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirecionadores de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837337"
---
# <a name="network-redirectors"></a>Redirecionadores de rede

Um redirecionador de rede é um driver de sistema de arquivos (ou FSD) que funciona da seguinte maneira:

-   Como um cliente em uma operação de e/s de rede enviando solicitações de e/s para servidores e processando as respostas dos servidores.
-   Como um servidor em uma operação de e/s de rede, recebendo solicitações de e/s de servidores e processando as solicitações.

Ele realiza toda a interação de nível baixo com o servidor para resolver o nome do arquivo fornecido pelo aplicativo com o local do recurso no servidor remoto. Dessa forma, o redirecionador permite que o aplicativo acesse e manipule recursos em servidores remotos como se eles estivessem localizados no computador local.

Os redirecionadores funcionam inteiramente no modo kernel. Isso fornece as seguintes vantagens de desempenho em relação às alternativas de modo de usuário:

-   Ele pode interagir com FSDs de modo kernel em execução no servidor, como o servidor FSD, sem a necessidade de modo de usuário para kernel e alternâncias de contexto de modo kernel para usuário.
-   Ele pode interagir no modo kernel com o Gerenciador de cache no servidor para armazenar em cache os dados de e/s enviados pelo Gerenciador de cache do servidor no cliente.
-   As funções de API personalizadas feitas para solicitações de e/s remotas e as alterações nas funções de e/s de arquivo padrão para fornecer essa funcionalidade não são necessárias.

 

 



