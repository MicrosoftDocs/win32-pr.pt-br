---
title: Bluetooth e escutar, selecionar e fechamento
description: O Bluetooth usa as funções escutar, selecionar e fechamento sem qualquer modificação da programação padrão de soquetes do Windows.
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
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454161"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a>Bluetooth e escutar, selecionar e fechamento

O Bluetooth usa as funções [**escutar**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**selecionar**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) sem qualquer modificação da programação padrão de soquetes do Windows.

Assim como ocorre com o Windows Sockets, a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) libera recursos associados ao soquete.

Ao chamar a função [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , é altamente recomendável que um valor baixo seja usado para o parâmetro de lista de *pendências* (normalmente de 2 a 4), já que apenas algumas conexões de cliente são aceitas. Isso reduz os recursos do sistema que são alocados para uso pelo soquete de escuta.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**ouvir**](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[**Não**](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 