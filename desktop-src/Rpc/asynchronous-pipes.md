---
title: Pipes assíncronos
description: O uso de parâmetros de pipe com RPC assíncrono permite que você transmita dados incrementalmente, à medida que eles se tornam disponíveis, sem atirá-los no cliente e no servidor.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0957b1ddc381d2a91b77033842b2807ed8a9dd34718d0148d6853083229d408d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023786"
---
# <a name="asynchronous-pipes"></a>Pipes assíncronos

O [uso](/windows/desktop/Midl/pipe) de parâmetros de pipe com RPC assíncrono permite que você transmita dados incrementalmente, à medida que eles se tornam disponíveis, sem atirá-los no cliente e no servidor. Isso é particularmente útil quando você tem uma grande quantidade de dados a transferir, combinada com um cliente lento, um servidor lento ou uma rede lenta. Se você usar um pipe em uma chamada de função assíncrona, ele será, por definição, um pipe assíncrono. Não há suporte para pipes síncronos em conjunto com funções assíncronas.

Ao contrário dos pipes convencionais (síncronos), em que o servidor lida com todos os detalhes de envio e recebimento de dados de pipe, os pipes assíncronos são simétricos. Ou seja, o cliente e o servidor podem fazer push e pull de dados por meio do pipe.

> [!Note]  
> Os parâmetros de pipe só podem ser passados por referência. Mesmo que o arquivo IDL mostre parâmetros de [pipe](/windows/desktop/Midl/pipe) sendo passados por valor, os stubs gerados aceitarão parâmetros de pipe somente por referência.

 

Na discussão a seguir sobre pipes assíncronos, supõe-se familiaridade com o construtor de tipo de pipe. Para obter mais informações sobre os procedimentos de pipe descritos nestes tópicos, consulte [Pipes](pipes.md).

 

 