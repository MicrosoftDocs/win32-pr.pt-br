---
description: A biblioteca DbgHelp é implementada por DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versões do DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5adb00c6442f7ba36f5aeb86e0255e175131492124d08fbf865e57a9721a7893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343856"
---
# <a name="dbghelp-versions"></a>Versões do DbgHelp

A biblioteca DbgHelp é implementada por DbgHelp.dll. Embora essa DLL seja incluída em todas as versões com suporte do Windows, raramente é a versão mais atual do DbgHelp disponível. Além disso, a versão do DbgHelp que é Windows tem funcionalidade reduzida das outras versões, especificamente, ela não tem suporte para o Servidor de Símbolos e o Servidor de Origem.

As versões mais atuais do DbgHelp.dll, SymSrv.dll e SrcSrv.dll estão disponíveis como parte do pacote [Ferramentas de Depuração](https://developer.microsoft.com/windows/downloads/windows-10-sdk) para Windows. As políticas de redistribuição para essas DLLs incluídas foram especificamente projetadas para facilitar o máximo possível para que as pessoas incluam esses arquivos em seus próprios pacotes e versões.

> [!Caution]  
> Os usuários nunca devem tentar instalar as Ferramentas de Depuração para [Windows versões](https://developer.microsoft.com/windows/downloads/windows-10-sdk) do DbgHelp.dll do DbgHelp.dll nos diretórios do sistema Windows porque eles não são testados nesse cenário e provavelmente desestabilizam o sistema. Há versões X64 e X86 separadas do pacote de depuração e ambas são necessárias para pessoas interessadas em dar suporte a ambas as plataformas.

Para obter a versão mais recente do DbgHelp.dll, acesse [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) e baixe Ferramentas de Depuração para Windows. Consulte [Chamando a biblioteca DbgHelp para](calling-the-dbghelp-library.md) obter informações sobre a instalação adequada.

> [!Note]  
> O DbgHelp.dll arquivo que é Windows é não redistribuível.

Muitas versões do DbgHelp incluem funcionalidade adicional. Para garantir que a versão correta do DbgHelp está disponível para seu aplicativo, revise as informações de Requisitos na documentação de referência de API específica.
