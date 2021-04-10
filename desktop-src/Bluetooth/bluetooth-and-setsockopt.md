---
title: Bluetooth e setsockopt
description: O Bluetooth usa a função setsockopt para definir vários parâmetros associados ao canal do servidor ou à conexão.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth e setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294129"
---
# <a name="bluetooth-and-setsockopt"></a>Bluetooth e setsockopt

O Bluetooth usa a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para definir vários parâmetros associados ao canal do servidor ou à conexão. O uso de **setsockopt** com Bluetooth tem os seguintes requisitos:

-   O parâmetro *s* de [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser um soquete Bluetooth válido.
-   O parâmetro de *nível* de [**SETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser sol \_ RFCOMM.

Para obter uma lista de opções de soquete Bluetooth disponíveis, consulte [Opções de soquete e Bluetooth](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 