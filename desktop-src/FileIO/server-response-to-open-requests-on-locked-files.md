---
description: Você pode minimizar o impacto que seu aplicativo tem em outros clientes e o impacto que eles têm em seu aplicativo concedendo o máximo de compartilhamento possível, solicitando o nível mínimo de acesso necessário e usando o bloqueio oportunista menos intrusivo adequado para seu aplicativo.
ms.assetid: c28b0ae0-0d35-4b59-9f54-87c55ca72716
title: Resposta do servidor para abrir solicitações em arquivos bloqueados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d397613f6b54f2b42c26a5674a787b796f5f19e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501924"
---
# <a name="server-response-to-open-requests-on-locked-files"></a>Resposta do servidor para abrir solicitações em arquivos bloqueados

A vida útil de um bloqueio oportunista inclui três intervalos de tempo distintos. Durante cada um, o servidor determina por diferentes significa sua reação a uma solicitação de um cliente para abrir um arquivo bloqueado por outro cliente. Em geral, você pode minimizar o impacto que seu aplicativo tem em outros clientes e o impacto que eles têm em seu aplicativo concedendo o máximo de compartilhamento possível, solicitando o nível mínimo de acesso necessário e usando o bloqueio oportunista menos intrusivo adequado para seu aplicativo.

O primeiro é o período após o servidor abrir um arquivo para um cliente, mas antes de conceder um bloqueio. Durante esse tempo, nenhum bloqueio existe no arquivo e o servidor depende do compartilhamento, dos modos de acesso e do tipo de bloqueio oportunista solicitado para determinar sua reação a outra solicitação para abrir o mesmo arquivo. Por exemplo, se você abrir o arquivo em questão para acesso de gravação, poderá inibir a concessão de bloqueios oportunistas que permitem o acesso de cache de leitura a outros clientes. O período de tempo antes que o servidor conceda um bloqueio normalmente está no intervalo de milissegundos, mas pode ser mais longo.

Depois que o bloqueio oportunista é concedido, o servidor examina o bloqueio para determinar a reação do servidor a uma solicitação aberta em um arquivo bloqueado. Novamente, como o aplicativo abriu o arquivo e o tipo de bloqueio que ele mantém afeta o modo como o servidor responde. Para obter mais informações sobre como o servidor responde em cada caso, consulte [tipos de bloqueios oportunistas](types-of-opportunistic-locks.md).

Por fim, há a extensão após o servidor determinar que o bloqueio deve ser quebrado (encerrado), mas antes de o aplicativo concluir sua reação à interrupção. Dependendo do tipo de bloqueio, seu aplicativo pode fazer o downgrade do bloqueio para um nível inferior ou nenhum. Seu aplicativo também pode fechar o arquivo e o bloqueio. Durante esse tempo, o servidor mantém no abeyance todas as solicitações de outros clientes para abrir o arquivo anteriormente bloqueado. Esse período de tempo pode variar de milissegundos a dezenas de segundos. Para obter mais informações, consulte [interrompendo os bloqueios oportunistas](breaking-opportunistic-locks.md).

 

 



