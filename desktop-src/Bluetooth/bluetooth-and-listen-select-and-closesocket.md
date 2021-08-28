---
title: Bluetooth e escutar, selecionar e fechamento
description: Bluetooth usa as funções escutar, selecionar e fechamento sem qualquer modificação da programação standard Windows sockets.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- fechamento
- ouvir
- select
- Bluetooth e escutar
- Bluetooth e escutar, selecione
- Bluetooth e escutar, selecionar e fechamento
- ouvir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fa3fc1285a9035173da80cc7a9821535409b872b171f7822708c379ff01543
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004476"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a>Bluetooth e escutar, selecionar e fechamento

Bluetooth usa as funções [**escutar**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**selecionar**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) sem qualquer modificação da programação standard Windows sockets.

assim como ocorre com soquetes de Windows, a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) libera recursos associados ao soquete.

Ao chamar a função [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , é altamente recomendável que um valor baixo seja usado para o parâmetro de lista de *pendências* (normalmente de 2 a 4), já que apenas algumas conexões de cliente são aceitas. Isso reduz os recursos do sistema que são alocados para uso pelo soquete de escuta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[**Não**](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 