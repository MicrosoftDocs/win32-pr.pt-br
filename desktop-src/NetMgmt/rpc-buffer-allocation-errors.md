---
title: Erros de alocação de buffer RPC
description: Como a biblioteca de tempo de execução RPC aloca memória para buffers de envio e recebimento, a função deve esperar erros de alocação RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292152"
---
# <a name="rpc-buffer-allocation-errors"></a>Erros de alocação de buffer RPC

Como a biblioteca de tempo de execução RPC aloca memória para buffers de envio e recebimento, a função deve esperar erros de alocação RPC. No caso de um erro de alocação de RPC, um identificador retomável é invalidado. Esse é um requisito porque as funções retomáveis não são rebobinadas.

 

 




