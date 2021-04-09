---
description: 'O Windows Sockets 2 incorpora o conceito de um protocolo em camadas: um que implementa apenas funções de comunicação de nível mais alto ao depender de uma pilha de transporte subjacente para a troca real de dados com um ponto de extremidade remoto.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocolos em camadas e cadeias de protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090378"
---
# <a name="layered-protocols-and-protocol-chains"></a><span data-ttu-id="436ff-103">Protocolos em camadas e cadeias de protocolos</span><span class="sxs-lookup"><span data-stu-id="436ff-103">Layered Protocols and Protocol Chains</span></span>

<span data-ttu-id="436ff-104">O Windows Sockets 2 incorpora o conceito de um protocolo em camadas: um que implementa apenas funções de comunicação de nível mais alto ao depender de uma pilha de transporte subjacente para a troca real de dados com um ponto de extremidade remoto.</span><span class="sxs-lookup"><span data-stu-id="436ff-104">Windows Sockets 2 incorporates the concept of a layered protocol: one that implements only higher-level communications functions while relying on an underlying transport stack for the actual exchange of data with a remote endpoint.</span></span> <span data-ttu-id="436ff-105">Um exemplo desse tipo de protocolo em camadas é uma camada de segurança que adiciona um protocolo ao processo de conexão de soquete a fim de realizar a autenticação e estabelecer um esquema de criptografia.</span><span class="sxs-lookup"><span data-stu-id="436ff-105">An example of this type of layered protocol is a security layer that adds a protocol to the socket connection process in order to perform authentication and establish an encryption scheme.</span></span> <span data-ttu-id="436ff-106">Um protocolo de segurança desse tipo geralmente requer os serviços de um protocolo de transporte básico e confiável, como TCP ou SPX.</span><span class="sxs-lookup"><span data-stu-id="436ff-106">Such a security protocol generally requires the services of an underlying and reliable transport protocol such as TCP or SPX.</span></span>

<span data-ttu-id="436ff-107">O termo *protocolo base* refere-se a um protocolo, como TCP ou SPX, que é totalmente capaz de executar comunicações de dados com um ponto de extremidade remoto.</span><span class="sxs-lookup"><span data-stu-id="436ff-107">The term *base protocol* refers to a protocol, such as TCP or SPX, that is fully capable of performing data communications with a remote endpoint.</span></span> <span data-ttu-id="436ff-108">Um *protocolo em camadas* é um protocolo que não pode ser autônomo, enquanto uma *cadeia de protocolos* é um ou mais protocolos em camadas juntos e ancorados por um protocolo base.</span><span class="sxs-lookup"><span data-stu-id="436ff-108">A *layered protocol* is a protocol that cannot stand alone, while a *protocol chain* is one or more layered protocols strung together and anchored by a base protocol.</span></span>

<span data-ttu-id="436ff-109">Você pode criar uma cadeia de protocolos se criar os protocolos em camadas para dar suporte ao SPI do Windows Sockets 2 em ambas as bordas superiores e inferiores.</span><span class="sxs-lookup"><span data-stu-id="436ff-109">You can create a protocol chain if you design the layered protocols to support the Windows Sockets 2 SPI at both their upper and lower edges.</span></span> <span data-ttu-id="436ff-110">Uma estrutura especial de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) refere-se à cadeia de protocolos como um todo e descreve a ordem explícita na qual os protocolos em camadas são Unidos.</span><span class="sxs-lookup"><span data-stu-id="436ff-110">A special [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure refers to the protocol chain as a whole and describes the explicit order in which the layered protocols are joined.</span></span> <span data-ttu-id="436ff-111">Isso é ilustrado na figura abaixo.</span><span class="sxs-lookup"><span data-stu-id="436ff-111">This is illustrated in the figure below.</span></span> <span data-ttu-id="436ff-112">Como somente protocolos base e cadeias de protocolo são diretamente utilizáveis por aplicativos, eles são os únicos listados quando os protocolos instalados são enumerados com a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="436ff-112">Since only base protocols and protocol chains are directly usable by applications, they are the only ones listed when the installed protocols are enumerated with the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

![arquitetura de protocolo em camadas](images/ovrvw2-3.png)

 

 
