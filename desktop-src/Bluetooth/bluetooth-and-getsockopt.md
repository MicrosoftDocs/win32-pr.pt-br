---
title: Bluetooth e getsockopt
description: Bluetooth usa a função getsockopt para consultar vários parâmetros associados ao canal do servidor ou à conexão.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth e getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee63d8dc1665868023967dd88c5ba223cce538c1fa1d41dd151329f6bf52f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081080"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth e getsockopt

Bluetooth usa a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar vários parâmetros associados ao canal do servidor ou à conexão. o uso de **getsockopt** com Bluetooth tem os seguintes requisitos:

-   o parâmetro *s* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve ser um soquete de Bluetooth válido.
-   O parâmetro de *nível* de [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve ser sol \_ RFCOMM.

para obter uma lista das opções de soquete Bluetooth disponíveis, consulte [opções de Bluetooth e soquete](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 