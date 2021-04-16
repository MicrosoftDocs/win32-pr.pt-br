---
description: As DLLs TAPI, juntamente com o servidor TAPI (Tapisvr.exe), são abstrações cruciais que separam aplicativos de usuário final ou de servidor dos provedores de serviço. Uma DLL TAPI em conjunto com o servidor TAPI fornece uma interface consistente entre essas duas camadas.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: DLL TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553811"
---
# <a name="tapi-dll"></a>DLL TAPI

As DLLs TAPI, juntamente com o servidor TAPI (Tapisvr.exe), são abstrações cruciais que separam aplicativos de usuário final ou de servidor dos provedores de serviço. Uma DLL TAPI em conjunto com o servidor TAPI fornece uma interface consistente entre essas duas camadas.

Um aplicativo TAPI carrega a DLL apropriada em seu espaço de processo. Durante a inicialização, a TAPI estabelece um link RPC com Tapisvr.exe. O servidor TAPI é executado no contexto de SVCHOST.

Há três DLLs associadas à TAPI: Tapi.dll, Tapi32.dll e Tapi3.dll. Essas DLLs estão localizadas em% SystemRoot% \\ System32. A figura a seguir ilustra as funções de suas respectivas funções na telefonia da Microsoft:

![funções das três DLLs TAPI](images/dllserv.png)

Os aplicativos de 16 bits existentes são vinculados a Tapi.dll. Tapi.dll é simplesmente uma camada de conversão que mapeia endereços de 16 bits para endereços de 32 bits e passa solicitações para Tapi32.dll.

Os aplicativos existentes da TAPI 2. x de 32 bits são vinculados a Tapi32.dll. Tapi32.dll é uma camada de Marshalling fina que transfere solicitações de função para o servidor TAPI (TAPISRV) e, quando necessário, carrega e invoca as DLLs do provedor de serviços de mídia no processo do aplicativo.

Os aplicativos TAPI 3. x são vinculados a Tapi3.dll.

 

 



