---
title: Usando Bluetooth
description: esta seção descreve as tarefas relacionadas à gravação de aplicativos baseados em Windows para Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80d57d12b2594ab5bbaeb5ad5d026552ab180ae409ba81446288ac396c746a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701826"
---
# <a name="using-bluetooth"></a>Usando Bluetooth

esta seção descreve as tarefas relacionadas à gravação de aplicativos baseados em Windows para Bluetooth.

Bluetooth fornece definições de programação nos arquivos Ws2bth. h e BluetoothAPIs. h. O arquivo Bthsdpdef. h deve ser incluído antes de BluetoothAPIs. h. o arquivo Ws2bth. h deve ser incluído após o Winsock2. h para usar os soquetes de Bluetooth. Vincule somente a bthprops. lib e evite vincular a irprops. lib. Irprops. lib é fornecido apenas para fins de compatibilidade com versões anteriores. Bthprops. lib está disponível no SDK do Windows Vista. você pode usar o SDK do Windows Vista para desenvolver aplicativos para o Windows XP com Service Pack 2 (SP2). o SDK do Windows Vista está disponível no [centro de Download](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).

Todos os mecanismos padrão síncronos e sobrepostos para ler e gravar dados que atualmente têm suporte com outras famílias de endereços operam corretamente com a \_ família de endereços BTH de AF.

há um código de exemplo incluído no SDK que mostra um aplicativo Bluetooth simples usando o Winsock 2,2 e o protocolo RFCOMM. o código-fonte do exemplo pode ser encontrado no local de instalação do SDK em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ <version number> \\ exemplos \\ NetDs \\ winsock \\ Bluetooth.

Esta seção descreve os tópicos a seguir.



| Seção                                                                                      | Conteúdo                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Bluetooth programando com soquetes de Windows](bluetooth-programming-with-windows-sockets.md) | explica como usar as interfaces de soquetes de Windows para implementar uma rede de Bluetooth. |



 

 

 




