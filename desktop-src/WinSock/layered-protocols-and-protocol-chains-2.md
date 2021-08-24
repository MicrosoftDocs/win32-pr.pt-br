---
description: 'Windows Os soquetes 2 incorporam o conceito de um protocolo em camadas: um que implementa apenas funções de comunicação de nível mais alto ao depender de uma pilha de transporte subjacente para a troca real de dados com um ponto de extremidade remoto.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocolos em camadas e cadeias de protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e60943bac5545fd7bb2bc87709d08c59d3addab205d14cab80687596721b973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858446"
---
# <a name="layered-protocols-and-protocol-chains"></a>Protocolos em camadas e cadeias de protocolos

Windows Os soquetes 2 incorporam o conceito de um protocolo em camadas: um que implementa apenas funções de comunicação de nível mais alto ao depender de uma pilha de transporte subjacente para a troca real de dados com um ponto de extremidade remoto. Um exemplo desse tipo de protocolo em camadas é uma camada de segurança que adiciona um protocolo ao processo de conexão de soquete a fim de realizar a autenticação e estabelecer um esquema de criptografia. Um protocolo de segurança desse tipo geralmente requer os serviços de um protocolo de transporte básico e confiável, como TCP ou SPX.

O termo *protocolo base* refere-se a um protocolo, como TCP ou SPX, que é totalmente capaz de executar comunicações de dados com um ponto de extremidade remoto. Um *protocolo em camadas* é um protocolo que não pode ser autônomo, enquanto uma *cadeia de protocolos* é um ou mais protocolos em camadas juntos e ancorados por um protocolo base.

você pode criar uma cadeia de protocolos se criar os protocolos em camadas para dar suporte ao SPI do Windows sockets 2 em ambas as bordas superiores e inferiores. Uma estrutura especial de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) refere-se à cadeia de protocolos como um todo e descreve a ordem explícita na qual os protocolos em camadas são Unidos. Isso é ilustrado na figura abaixo. Como somente protocolos base e cadeias de protocolo são diretamente utilizáveis por aplicativos, eles são os únicos listados quando os protocolos instalados são enumerados com a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

![arquitetura de protocolo em camadas](images/ovrvw2-3.png)

 

 
