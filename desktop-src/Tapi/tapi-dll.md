---
description: As DLLs tapi, juntamente com o servidor TAPI (Tapisvr.exe), são abstrações cruciais que separam aplicativos de usuário final ou servidor de provedores de serviços. Uma DLL tapi em conjunto com o servidor TAPI fornece uma interface consistente entre essas duas camadas.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: TAPI DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff26274baf25047212a3f9f8e15c2211d90cbaa10db23674ae54dbb97bbfdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012196"
---
# <a name="tapi-dll"></a>TAPI DLL

As DLLs tapi, juntamente com o servidor TAPI (Tapisvr.exe), são abstrações cruciais que separam aplicativos de usuário final ou servidor de provedores de serviços. Uma DLL tapi em conjunto com o servidor TAPI fornece uma interface consistente entre essas duas camadas.

Um aplicativo TAPI carrega a DLL apropriada em seu espaço de processo. Durante a inicialização, a TAPI estabelece um link RPC com Tapisvr.exe. O servidor TAPI é executado no contexto de SVCHOST.

Há três DLLs associadas à TAPI: Tapi.dll, Tapi32.dll e Tapi3.dll. Essas DLLs estão localizadas em %SystemRoot% \\ system32. A figura a seguir ilustra as funções de suas respectivas funções na Telefonia da Microsoft:

![funções das três dlls tapi](images/dllserv.png)

Os aplicativos de 16 bits existentes vinculam-se Tapi.dll. Tapi.dll é simplesmente uma camada de trabalho que mapeia endereços de 16 bits para endereços de 32 bits e passa solicitações para Tapi32.dll.

Os aplicativos TAPI 2.x existentes de 32 bits são link para Tapi32.dll. Tapi32.dll é uma camada de marshalling fino que transfere solicitações de função para o tapi server (TAPISRV) e, quando necessário, carrega e invoca DLLs do provedor de serviços de mídia no processo do aplicativo.

Link de aplicativos TAPI 3.x para Tapi3.dll.

 

 



