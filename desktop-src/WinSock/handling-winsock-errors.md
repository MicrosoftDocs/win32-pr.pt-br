---
description: Tratamento de erro no Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Tratamento de erros winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbb0ea47fc023ce0d6ae47f82a6bb9d732e052d5749fe58f9a405d6784d941b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097896"
---
# <a name="handling-winsock-errors"></a>Tratamento de erros winsock

A maioria Windows funções soquetes 2 não retornam a causa específica de um erro quando a função retorna. Algumas funções Winsock retornarão um valor de zero se bem-sucedidas. Caso contrário, o valor SOCKET ERROR (-1) será retornado e um número de erro específico poderá ser recuperado chamando \_ a [**função WSAGetLastError.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) Para funções Winsock que retornam um handle, um valor de retorno de SOQUETE INVÁLIDO (0xffff) indica um erro e um número de erro específico pode ser recuperado chamando \_ **WSAGetLastError**. Para funções Winsock que retornam um ponteiro, um valor de retorno **NULL** indica um erro e um número de erro específico pode ser recuperado chamando a **função WSAGetLastError.**

Um código de erro Winsock pode ser convertido em um HRESULT para uso em uma RPC (chamada de procedimento remoto) usando HRESULT \_ FROM \_ WIN32. Em versões anteriores do SDK (Kit de Desenvolvimento de Software de Plataforma), o HRESULT FROM WIN32 era definido como uma macro no arquivo de título \_ \_ *Winerror.h.* No Microsoft Windows Software Development Kit (SDK), HRESULT FROM WIN32 é definido como uma função em linha no arquivo de título \_ \_ *Winerror.h.*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Códigos de erro de soquetes](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



