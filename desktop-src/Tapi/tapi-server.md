---
description: O tapi server (TAPISRV) é o repositório central de dados de telefonia em um computador de usuário.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Servidor TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19eb335ddef68f5f4cc588e34edab4931ad8be1e5e1d768e07a142989afe2291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002674"
---
# <a name="tapi-server"></a>Servidor TAPI

O tapi server (TAPISRV) é o repositório central de dados de telefonia em um computador de usuário. Esse processo de serviço rastreia recursos de telefonia local e remota, aplicativos registrados para lidar com solicitações de Telefonia Assistida e funções assíncronas pendentes, além de habilitar uma interface consistente com TSPs (provedores de serviços de telefonia). Para obter mais informações e um diagrama que ilustra a relação do servidor TAPI com outros componentes e uma visão geral de suas funções, consulte Modelo de Programação [de Telefonia da Microsoft](microsoft-telephony-programming-model.md).

Para computadores em execução em sistemas operacionais Windows Server 2003, Windows XP e Windows 2000, o TAPISRV é executado dentro do contexto de Svchost.exe. Para computadores em execução Windows NT, ele é executado como um processo de serviço separado. Quando um aplicativo carrega uma DLL TAPI em seu espaço de processo e executa uma operação de inicialização, a DLL estabelece um link RPC para o servidor TAPI. O servidor TAPI carrega TSPs (provedores de serviços de telefone) em seu espaço de processo. Independentemente de quantos aplicativos acessam os dispositivos de um determinado provedor, somente uma instância de um determinado TSP existirá.

 

 



