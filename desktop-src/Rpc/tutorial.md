---
title: Tutorial
description: Este tutorial orienta você pelas etapas necessárias para criar um aplicativo distribuído simples, de único cliente e de servidor único a partir de um aplicativo autônomo existente.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- RPC de chamada de procedimento remoto, tutorial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005883"
---
# <a name="tutorial"></a>Tutorial

Este tutorial orienta você pelas etapas necessárias para criar um aplicativo distribuído simples, de único cliente e de servidor único a partir de um aplicativo autônomo existente. Estas etapas são:

-   Criar definição de interface e arquivos de configuração de aplicativo.
-   Use o compilador MIDL para gerar cabeçalhos e stubs de cliente e de servidor C-Language a partir desses arquivos.
-   Grave um aplicativo cliente que gerencia sua conexão com o servidor.
-   Escreva um aplicativo de servidor que contenha os procedimentos remotos reais.
-   Compile e vincule esses arquivos à biblioteca de tempo de execução RPC para produzir o aplicativo distribuído.

O aplicativo cliente passa uma cadeia de caracteres para o servidor em uma chamada de procedimento remoto e o servidor imprime a cadeia de caracteres "Olá, mundo" para a saída padrão.

Os arquivos de origem completos para este aplicativo de exemplo, com código adicional para lidar com a entrada de linha de comando e para gerar várias mensagens de status para o usuário, estão no \\ diretório de saudação RPC do SDK (Software Development Kit) da plataforma.

Esta seção apresenta sua discussão nos seguintes tópicos:

-   [O aplicativo autônomo](the-standalone-application.md)
-   [Definindo a interface](defining-the-interface.md)
-   [Gerando o UUID](generating-the-uuid.md)
-   [O arquivo IDL](the-idl-file.md)
-   [O arquivo ACF](the-acf-file.md)
-   [Gerando os arquivos stub](generating-the-stub-files.md)
-   [O aplicativo cliente](the-client-application.md)
-   [O aplicativo de servidor](the-server-application.md)
-   [Parando o aplicativo de servidor](stopping-the-server-application.md)
-   [Compilando e vinculando](compiling-and-linking.md)
-   [Executando o aplicativo](running-the-application.md)

 

 




