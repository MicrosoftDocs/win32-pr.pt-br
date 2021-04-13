---
title: E/s assíncrona e RPC assíncrono
description: E/s assíncrona é um meio eficiente para um único thread gerenciar várias solicitações de e/s simultaneamente.
ms.assetid: a9105518-4130-4119-b8d1-e73064b077e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932e85283eb67ff6675a646e791bbce5fe15d65
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366592"
---
# <a name="asynchronous-io-and-asynchronous-rpc"></a>E/s assíncrona e RPC assíncrono

E/s assíncrona é um meio eficiente para um único thread gerenciar várias solicitações de e/s simultaneamente. O RPC assíncrono no servidor realiza uma finalidade semelhante para solicitações RPC. Em versões do Windows anteriores ao Windows Vista, não é recomendável postar solicitações de e/s assíncronas a partir de procedimentos de servidor usando RPC assíncrono. No entanto, no Windows Vista e em versões posteriores do Windows, as solicitações de e/s assíncronas associadas a uma porta de conclusão de e/s são suportadas pelo RPC assíncrono.

Antes do Windows Vista, uma chamada de procedimento remoto assíncrona pode ser concluída antes de a solicitação de e/s assíncrona ser concluída. Quando a chamada assíncrona for concluída, seu thread poderá ser encerrado se o tempo de execução RPC decidir que ele tem threads suficientes disponíveis para atender à carga de trabalho esperada. O sistema associa todas as solicitações de e/s ao thread que as inicia. Se o thread for encerrado, todas as solicitações de e/s pendentes nesse thread serão anuladas. As solicitações de e/s pendentes não podem ser movidas para outro thread.

Portanto, os designers de aplicativos direcionados a versões do Windows anteriores ao Windows Vista podem usar e/s síncrona em procedimentos de servidor, ou podem encaminhar todas as solicitações que envolvem e/s assíncrona para procedimentos executados em um pool de threads que o aplicativo gerencia. A API do Windows fornece funções para gerenciamento de pool de threads. Consulte [funções de thread e processo](/windows/desktop/ProcThread/process-and-thread-functions).

 

 