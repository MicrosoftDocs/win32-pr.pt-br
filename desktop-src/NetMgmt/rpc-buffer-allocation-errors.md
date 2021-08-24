---
title: Erros de alocação de buffer RPC
description: Como a biblioteca de tempo de execução RPC aloca memória para buffers de envio e recebimento, a função deve esperar erros de alocação RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c484837f1f03bce8a8175ddb343065051e3695eec7c65d8a9de89c15fb5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745006"
---
# <a name="rpc-buffer-allocation-errors"></a>Erros de alocação de buffer RPC

Como a biblioteca de tempo de execução RPC aloca memória para buffers de envio e recebimento, a função deve esperar erros de alocação RPC. No caso de um erro de alocação de RPC, um identificador retomável é invalidado. Esse é um requisito porque as funções retomáveis não são rebobinadas.

 

 




