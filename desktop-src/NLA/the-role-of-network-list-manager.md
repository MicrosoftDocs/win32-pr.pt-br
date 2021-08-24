---
title: A função do Gerenciador de lista de rede
description: A função do Gerenciador de lista de rede
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec37d0cf157b87bf43fe12e9aa3a33eb316b7800474dd75ef3a6d4e23bb6189d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780486"
---
# <a name="the-role-of-network-list-manager"></a>A função do Gerenciador de lista de rede

antes do Windows XP e do Windows Server 2003, os aplicativos eram obrigados a chamar várias APIs não relacionadas para obter dados sobre atributos de rede, como o endereço IP, o controlador de domínio ou o DNS (sistema de nomes de domínio). a partir do Windows XP e do Windows Server 2003, a API Winsock de reconhecimento de local de rede apresentou um conjunto limitado de funcionalidades de local de rede. no Windows Server 2008 e Windows Vista, o serviço de reconhecimento de rede captura os atributos de rede em um local e permite que os aplicativos consultem e recuperem redes e atributos específicos. O Gerenciador de lista de rede substitui a funcionalidade da API do Winsock anterior (disponível como um provedor de espaço para nome do Winsock) enquanto mantém a compatibilidade com aplicativos mais antigos usando a API do Winsock.

 

 




