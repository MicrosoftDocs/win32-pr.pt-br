---
description: Diferenças entre e/s local e e/s de rede no Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Diferenças em e/s de rede e local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757561"
---
# <a name="differences-in-local-and-network-io"></a>Diferenças em e/s de rede e local

Há algumas diferenças notáveis entre a e/s local e a I/O de rede no Windows:

-   O suporte de e/s de rede depende do redirecionador e do protocolo de rede.
-   O desempenho de e/s de rede depende de quantas operações de e/s de rede estão ocorrendo e da velocidade da conexão de rede. Seu aplicativo deve ser capaz de lidar com operações de e/s de rede com servidores que podem ser muito mais rápidos ou mais lentos do que o computador local, bem como alterações transitórias na capacidade da rede. Nesses casos, seu aplicativo pode precisar permitir mais tempo para a operação ser concluída.
-   As funções usadas para executar a e/s de arquivo local podem se comportar de maneira diferente pela rede. Por exemplo, uma operação de e/s de rede que leva muito tempo para ser concluída pode atingir o tempo limite. Em algumas situações, os identificadores de arquivo podem ser deixados abertos indefinidamente por causa disso. Outro exemplo é que as funções podem retornar códigos de erro para que seu aplicativo processe que seja específico para e/s de rede.

 

 



