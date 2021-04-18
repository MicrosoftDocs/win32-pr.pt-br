---
description: Tratamento de erros no Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Manipulando erros do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807870"
---
# <a name="handling-winsock-errors"></a>Manipulando erros do Winsock

A maioria das funções do Windows Sockets 2 não retorna a causa específica de um erro quando a função retorna. Algumas funções do Winsock retornarão um valor zero se for bem-sucedido. Caso contrário, o valor de erro de soquete \_ (-1) é retornado e um número de erro específico pode ser recuperado chamando a função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) . Para funções do Winsock que retornam um identificador, um valor de retorno de \_ soquete inválido (0xFFFF) indica um erro e um número de erro específico pode ser recuperado chamando **WSAGetLastError**. Para funções do Winsock que retornam um ponteiro, um valor de retorno de **NULL** indica um erro e um número de erro específico pode ser recuperado chamando a função **WSAGetLastError** .

Um código de erro do Winsock pode ser convertido em um HRESULT para uso em uma RPC (chamada de procedimento remoto) usando HRESULT \_ do \_ Win32. Em versões anteriores do SDK (Software Development Kit) da plataforma, \_ o HRESULT do \_ Win32 foi definido como uma macro no arquivo de cabeçalho *Winerror. h* . No SDK (Software Development Kit) do Microsoft Windows, o HRESULT \_ do \_ Win32 é definido como uma função embutida no arquivo de cabeçalho *Winerror. h* .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de erro do Windows Sockets](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



