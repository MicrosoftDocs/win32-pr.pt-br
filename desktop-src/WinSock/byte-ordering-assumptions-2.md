---
description: Estruturas SOCKADDR e suposições de ordenação de bytes no Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Suposições de ordenação de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814105"
---
# <a name="byte-ordering-assumptions"></a>Suposições de ordenação de bytes

Um provedor de serviços deve tratar todos os componentes [**SOCKADDR**](sockaddr-2.md) exclusivos do parâmetro de família de endereços como se eles estivessem na ordem de bytes de rede e o parâmetro de família de endereços como na ordem de bytes do computador local. É responsabilidade do aplicativo Winsock garantir que os endereços contidos em estruturas **SOCKADDR** sejam organizados corretamente. A API do Winsock fornece várias rotinas de conversão para simplificar essa tarefa. Atualmente, essas rotinas entendem a conversão entre a ordem de bytes naturais do host local e a ordenação de bytes de rede big-endian ou little-endian. A arquitetura do Winsock pode dar suporte a outros esquemas de ordenação de bytes no futuro.

 

 



