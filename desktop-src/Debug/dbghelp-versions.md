---
description: A biblioteca DbgHelp é implementada pelo DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versões do DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646210"
---
# <a name="dbghelp-versions"></a>Versões do DbgHelp

A biblioteca DbgHelp é implementada pelo DbgHelp.dll. Embora essa DLL esteja incluída em todas as versões com suporte do Windows, raramente é a versão mais atual do DbgHelp disponível. Além disso, a versão do DbgHelp que acompanha o Windows reduziu a funcionalidade de outras versões – especificamente, ela não tem suporte para servidor de símbolos e servidor de origem.

As versões mais atuais do DbgHelp.dll, SymSrv.dll e SrcSrv.dll estão disponíveis como parte do pacote de [ferramentas de depuração para Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) . As políticas de redistribuição para essas DLLs incluídas foram especificamente projetadas para facilitar o máximo possível para que as pessoas incluam esses arquivos em seus próprios pacotes e versões.

> [!Caution]  
> Os usuários nunca devem tentar instalar as [ferramentas de depuração para](https://developer.microsoft.com/windows/downloads/windows-10-sdk) versões do windows do DbgHelp.dll nos diretórios de sistema do Windows porque eles não são testados nesse cenário e provavelmente desestabilizam o sistema. Há versões separadas x64 e x86 do pacote de depuração e ambas são necessárias para as pessoas interessadas em dar suporte a ambas as plataformas.

Para obter a versão mais recente do DbgHelp.dll, acesse [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) e baixe as ferramentas de depuração para Windows. Consulte [chamando a biblioteca dbghelp](calling-the-dbghelp-library.md) para obter informações sobre a instalação correta.

> [!Note]  
> O arquivo de DbgHelp.dll fornecido no Windows não é redistribuível.

Muitas versões do DbgHelp incluem funcionalidade adicional. Para garantir que a versão correta do DbgHelp esteja disponível para seu aplicativo, examine as informações de requisitos na documentação de referência da API específica.
