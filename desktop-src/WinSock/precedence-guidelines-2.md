---
description: Os dois (ou mais) descritores que fazem referência a um Soquete compartilhado podem ser usados de forma independente no que diz respeito à e/s.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Diretrizes de precedência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090365"
---
# <a name="precedence-guidelines"></a>Diretrizes de precedência

Os dois (ou mais) descritores que fazem referência a um Soquete compartilhado podem ser usados de forma independente no que diz respeito à e/s. No entanto, a interface do Windows Sockets não implementa nenhum tipo de controle de acesso, portanto, cabe aos processos envolvidos coordenarem suas operações em um Soquete compartilhado. Um uso típico para soquetes compartilhados é ter um processo responsável pela criação de soquetes e estabelecimento de conexões que entregam soquetes a outros processos responsáveis pela troca de informações.

A diretriz geral para dar suporte a várias operações pendentes em soquetes compartilhados é que um provedor de serviços é incentivado a respeitar todas as operações simultâneas em soquetes compartilhados, especialmente a operação mais recente em um objeto de soquete. Se necessário, isso pode ocorrer às custas de cancelar algumas das operações anteriores, mas ainda pendentes, que retornarão WSAEINTR nesse caso.

 

 



