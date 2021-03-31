---
title: Provedores de segurança
description: A interface de provedor de suporte de segurança (SSPI) fornece suporte para autenticação mútua e é exposta diretamente por meio de APIs e serviços SSPI em camadas em SSPI, incluindo RPC.
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf033550c2a2da66b7eab05f23289ba988690e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004898"
---
# <a name="security-providers"></a>Provedores de segurança

A interface de provedor de suporte de segurança (SSPI) fornece suporte para autenticação mútua e é exposta diretamente por meio de APIs e serviços SSPI em camadas em SSPI, incluindo RPC.

Nem todos os pacotes de segurança disponíveis para SSPI dão suporte à autenticação mútua. Para obter a autenticação mútua, o aplicativo deve solicitar autenticação mútua e um pacote de segurança que ofereça suporte a ele. Por exemplo, o exemplo de código em [autenticação mútua em um serviço de soquetes do Windows com um SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) usa o pacote "Negotiate" no Secur32.dll, que está incluído no Windows 2000.

 

 




