---
title: Bluetooth e getsockopt
description: O Bluetooth usa a função getsockopt para consultar vários parâmetros associados ao canal do servidor ou à conexão.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth e getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641365"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth e getsockopt

O Bluetooth usa a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar vários parâmetros associados ao canal do servidor ou à conexão. O uso de **getsockopt** com Bluetooth tem os seguintes requisitos:

-   O parâmetro *s* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve ser um soquete Bluetooth válido.
-   O parâmetro de *nível* de [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve ser sol \_ RFCOMM.

Para obter uma lista de opções de soquete Bluetooth disponíveis, consulte [Opções de soquete e Bluetooth](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 