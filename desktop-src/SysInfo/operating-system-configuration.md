---
description: o diretório Windows é o diretório que contém aplicativos baseados em Windows, arquivos de inicialização e arquivos de ajuda. A função GetWindowsDirectory recupera o caminho para esse diretório.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configuração do sistema operacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747a881568f9814152a230880d38891590d33ffc67cfa5e8178adfa66c1a01fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885283"
---
# <a name="operating-system-configuration"></a>Configuração do sistema operacional

o *diretório Windows* é o diretório que contém aplicativos baseados em Windows, arquivos de inicialização e arquivos de ajuda. A função [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recupera o caminho para esse diretório.

O *diretório do sistema* é o diretório que contém bibliotecas de vínculo dinâmico, drivers e arquivos de fonte. A função [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) recupera o caminho para esse diretório.

A função [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) recupera o nome do usuário atualmente conectado ao sistema. O nome de usuário será o nome de logon ou o nome completo do usuário, se o último estiver incluído no registro.

Uma *variável de ambiente* é uma variável simbólica que representa algum elemento do sistema, como um caminho, um nome de arquivo ou outros dados literais. Por exemplo, o caminho da variável de ambiente representa os diretórios nos quais pesquisar arquivos executáveis. Quando um usuário faz logon, o sistema inicializa as variáveis de ambiente com base na seção ambiente do registro. A função [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) recupera os valores das variáveis de ambiente especificadas.

Informações adicionais são fornecidas pela interface [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) .

 

 
