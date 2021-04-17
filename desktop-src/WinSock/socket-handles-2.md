---
description: Um identificador de soquete pode, opcionalmente, ser um identificador de arquivo no Windows Sockets 2. Um identificador de soquete de um provedor Winsock pode ser usado com outras funções não Winsock, como ReadFile, WriteFile, ReadFileEx e WriteFileEx.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Identificadores de soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6ca8ed935819e018a59c52fb43dcf816530c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787766"
---
# <a name="socket-handles"></a>Identificadores de soquete

Um identificador de soquete pode, opcionalmente, ser um identificador de arquivo no Windows Sockets 2. Um identificador de soquete de um provedor Winsock pode ser usado com outras funções não Winsock, como [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex).

O **XP1 \_ IFS \_ manipula** o membro na estrutura de informações de protocolo para um provedor determina se um identificador de soquete de um provedor é um identificador IFS (sistema de arquivos instalável). Identificadores de soquete que são identificadores de IFS podem ser usados sem uma penalidade de desempenho com outras funções não Winsock ([**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), por exemplo). Qualquer identificador de soquete não IFS quando usado com funções não Winsock (**ReadFile** e **WriteFile**, por exemplo) resulta em interações entre o provedor e o sistema de arquivos onde a sobrecarga de processamento extra está envolvida e pode resultar em uma penalidade de desempenho significativa. Ao usar identificadores de soquete com funções não Winsock, os códigos de erro propagados do sistema de arquivos base nem sempre são mapeados para códigos de erro do Winsock. Consequentemente, é recomendável que os identificadores de soquete sejam usados apenas com as funções do Winsock.

Um identificador de soquete não deve ser usado com a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) . A presença de LSPs (provedores de serviço em camadas) pode causar a falha e não há nenhuma maneira para o processo de destino importar o identificador de soquete.

> [!Note]  
> Os provedores de serviço em camadas são preteridos. A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).

 

O Windows Sockets 2 expandiu determinadas funções que transferem dados entre soquetes usando identificadores. As funções oferecem vantagens específicas para soquetes para transferência de dados e incluem [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa).

 

 
