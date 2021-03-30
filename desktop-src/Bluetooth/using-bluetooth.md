---
title: Usando Bluetooth
description: Esta seção descreve as tarefas relacionadas à gravação de aplicativos baseados em Windows para Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642907"
---
# <a name="using-bluetooth"></a>Usando Bluetooth

Esta seção descreve as tarefas relacionadas à gravação de aplicativos baseados em Windows para Bluetooth.

O Bluetooth fornece definições de programação nos arquivos Ws2bth. h e BluetoothAPIs. h. O arquivo Bthsdpdef. h deve ser incluído antes de BluetoothAPIs. h. O arquivo Ws2bth. h deve ser incluído após o Winsock2. h para usar soquetes Bluetooth. Vincule somente a bthprops. lib e evite vincular a irprops. lib. Irprops. lib é fornecido apenas para fins de compatibilidade com versões anteriores. Bthprops. lib está disponível no SDK do Windows Vista. Você pode usar o SDK do Windows Vista para desenvolver aplicativos para o Windows XP com Service Pack 2 (SP2). O SDK do Windows Vista está disponível no [centro de download](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).

Todos os mecanismos padrão síncronos e sobrepostos para ler e gravar dados que atualmente têm suporte com outras famílias de endereços operam corretamente com a \_ família de endereços BTH de AF.

Há um código de exemplo incluído no SDK que mostra um aplicativo simples de Bluetooth usando o Winsock 2,2 e o protocolo RFCOMM. O código-fonte do exemplo pode ser encontrado no local de instalação do SDK em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ <version number> \\ Samples \\ NetDs \\ Winsock \\ Bluetooth.

Esta seção descreve os tópicos a seguir.



| Seção                                                                                      | Conteúdo                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Programação de Bluetooth com Windows Sockets](bluetooth-programming-with-windows-sockets.md) | Explica como usar as interfaces do Windows Sockets para implementar uma rede Bluetooth. |



 

 

 




