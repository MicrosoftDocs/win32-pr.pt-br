---
description: O servidor TAPI (TAPISRV) é o repositório central de dados de telefonia em um computador de usuário.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Servidor TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829286"
---
# <a name="tapi-server"></a>Servidor TAPI

O servidor TAPI (TAPISRV) é o repositório central de dados de telefonia em um computador de usuário. Esse processo de serviço controla recursos de telefonia locais e remotos, aplicativos registrados para lidar com solicitações de telefonia assistidas e funções assíncronas pendentes e também permite uma interface consistente com provedores de serviço de telefonia (TSPs). Para obter mais informações e um diagrama que ilustra a relação do servidor TAPI com outros componentes e uma visão geral de suas funções, consulte [modelo de programação de telefonia da Microsoft](microsoft-telephony-programming-model.md).

Para computadores em execução em sistemas operacionais Windows Server 2003, Windows XP e Windows 2000, o TAPISRV é executado dentro do contexto de Svchost.exe. Para computadores em execução no Windows NT, ele é executado como um processo de serviço separado. Quando um aplicativo carrega uma DLL TAPI em seu espaço de processo e executa uma operação de inicialização, a DLL estabelece um link RPC para o servidor TAPI. O servidor TAPI carrega provedores de serviço de telefone (TSPs) em seu espaço de processo. Independentemente de quantos aplicativos acessarem os dispositivos de um determinado provedor, haverá apenas uma instância de um determinado TSP.

 

 



