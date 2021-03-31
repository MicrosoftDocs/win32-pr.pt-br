---
title: A função do Gerenciador de lista de rede
description: A função do Gerenciador de lista de rede
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823030"
---
# <a name="the-role-of-network-list-manager"></a>A função do Gerenciador de lista de rede

Antes do Windows XP e do Windows Server 2003, os aplicativos eram obrigados a chamar várias APIs não relacionadas para obter dados sobre atributos de rede, como o endereço IP, o controlador de domínio ou o DNS (sistema de nomes de domínio). A partir do Windows XP e do Windows Server 2003, a API Winsock de reconhecimento de local de rede apresentou um conjunto limitado de funcionalidades de local de rede. No Windows Server 2008 e no Windows Vista, o serviço de reconhecimento de rede captura os atributos de rede em um local e permite que os aplicativos consultem e recuperem redes e atributos específicos. O Gerenciador de lista de rede substitui a funcionalidade da API do Winsock anterior (disponível como um provedor de espaço para nome do Winsock) enquanto mantém a compatibilidade com aplicativos mais antigos usando a API do Winsock.

 

 




