---
description: Estruturas SOCKADDR e suposições de ordenação de bytes no Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Suposições de ordenação de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21c1e680b0fe658994723b0a1d87c2a7d6adbf0a00a5452b185401b03099089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097906"
---
# <a name="byte-ordering-assumptions"></a>Suposições de ordenação de bytes

Um provedor de serviços deve tratar todos os componentes [**SOCKADDR**](sockaddr-2.md) exclusivos do parâmetro de família de endereços como se eles estivessem na ordem de bytes de rede e o parâmetro de família de endereços como na ordem de bytes do computador local. É responsabilidade do aplicativo Winsock garantir que os endereços contidos em estruturas **SOCKADDR** sejam organizados corretamente. A API do Winsock fornece várias rotinas de conversão para simplificar essa tarefa. Atualmente, essas rotinas entendem a conversão entre a ordem de bytes naturais do host local e a ordenação de bytes de rede big-endian ou little-endian. A arquitetura do Winsock pode dar suporte a outros esquemas de ordenação de bytes no futuro.

 

 



