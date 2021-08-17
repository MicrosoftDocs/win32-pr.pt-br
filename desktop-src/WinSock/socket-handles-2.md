---
description: um identificador de soquete pode, opcionalmente, ser um identificador de arquivo no Windows sockets 2. Um identificador de soquete de um provedor Winsock pode ser usado com outras funções não Winsock, como ReadFile, WriteFile, ReadFileEx e WriteFileEx.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Identificadores de soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a9c9c642c317e9ab4ef897a20b68184df2c04324bcb76c33dea762e78c2846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740030"
---
# <a name="socket-handles"></a>Identificadores de soquete

um identificador de soquete pode, opcionalmente, ser um identificador de arquivo no Windows sockets 2. Um identificador de soquete de um provedor Winsock pode ser usado com outras funções não Winsock, como [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex).

O **XP1 \_ IFS \_ manipula** o membro na estrutura de informações de protocolo para um provedor determina se um identificador de soquete de um provedor é um identificador IFS (sistema de arquivos instalável). Identificadores de soquete que são identificadores de IFS podem ser usados sem uma penalidade de desempenho com outras funções não Winsock ([**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), por exemplo). Qualquer identificador de soquete não IFS quando usado com funções não Winsock (**ReadFile** e **WriteFile**, por exemplo) resulta em interações entre o provedor e o sistema de arquivos onde a sobrecarga de processamento extra está envolvida e pode resultar em uma penalidade de desempenho significativa. Ao usar identificadores de soquete com funções não Winsock, os códigos de erro propagados do sistema de arquivos base nem sempre são mapeados para códigos de erro do Winsock. Consequentemente, é recomendável que os identificadores de soquete sejam usados apenas com as funções do Winsock.

Um identificador de soquete não deve ser usado com a função [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) . A presença de LSPs (provedores de serviço em camadas) pode causar a falha e não há nenhuma maneira para o processo de destino importar o identificador de soquete.

> [!Note]  
> Os provedores de serviço em camadas são preteridos. começando com Windows 8 e Windows Server 2012, use [Windows plataforma de filtragem](../fwp/windows-filtering-platform-start-page.md).

 

Windows O Sockets 2 expandiu determinadas funções que transferem dados entre soquetes usando identificadores. As funções oferecem vantagens específicas para soquetes para transferência de dados e incluem [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)e [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa).

 

 
