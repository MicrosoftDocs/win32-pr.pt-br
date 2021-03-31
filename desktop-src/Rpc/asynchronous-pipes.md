---
title: Pipes assíncronos
description: O uso de parâmetros de pipe com RPC assíncrono permite transmitir dados de forma incremental, pois eles ficam disponíveis, sem ligar o cliente e o servidor.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641632"
---
# <a name="asynchronous-pipes"></a>Pipes assíncronos

O uso de parâmetros de [pipe](/windows/desktop/Midl/pipe) com RPC assíncrono permite transmitir dados de forma incremental, pois eles ficam disponíveis, sem ligar o cliente e o servidor. Isso é particularmente útil quando você tem uma grande quantidade de dados a serem transferidos, combinados com um cliente lento, um servidor lento ou uma rede lenta. Se você usar um pipe em uma chamada de função assíncrona, ele será, por definição, um pipe assíncrono. Não há suporte para pipes síncronos em conjunto com funções assíncronas.

Ao contrário dos pipes convencionais (síncronos) em que o servidor lida com todos os detalhes de envio e recebimento de dados de pipe, os pipes assíncronos são simétricos. Ou seja, o cliente e o servidor podem enviar e extrair dados por meio do pipe.

> [!Note]  
> Os parâmetros de pipe só podem ser passados por referência. Mesmo que o arquivo IDL mostre os parâmetros de [pipe](/windows/desktop/Midl/pipe) que estão sendo passados pelo valor, os stubs gerados aceitarão os parâmetros de pipe por referência apenas.

 

Na seguinte discussão sobre pipes assíncronos, a familiaridade com o construtor de tipo de pipe é assumida. Para obter mais informações sobre os procedimentos de pipe descritos nestes tópicos, consulte [pipes](pipes.md).

 

 