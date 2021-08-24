---
description: As tabelas de mensagens são recursos de cadeia de caracteres especiais usados ao exibir mensagens de erro. Eles são declarados em um arquivo de recurso usando a instrução messagetable resource-definition. Para acessar as cadeias de caracteres de mensagem, use a função FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tabelas de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6141f78342db2554e85053adda7ee68bdb0e855f213f103da1bb7f62eac1d703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691816"
---
# <a name="message-tables"></a>Tabelas de mensagens

As tabelas de mensagens são recursos de cadeia de caracteres especiais usados ao exibir mensagens de erro. Eles são declarados em um arquivo de recurso usando a [instrução messagetable](../menurc/messagetable-resource.md) resource-definition. Para acessar as cadeias de caracteres de mensagem, use [**a função FormatMessage.**](/windows/desktop/api/WinBase/nf-winbase-formatmessage)

O sistema fornece uma tabela de mensagens para os códigos [de erro do sistema.](system-error-codes.md) Para recuperar a cadeia de caracteres que corresponde ao código de erro, chame [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com o sinalizador FORMAT \_ MESSAGE FROM \_ \_ SYSTEM.

Para fornecer uma tabela de mensagens para seu aplicativo, siga as instruções em [Arquivos de Texto da Mensagem](../eventlog/message-text-files.md). Para recuperar cadeias de caracteres da tabela de mensagens, [**chame FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com o sinalizador FORMAT \_ MESSAGE FROM \_ \_ HMODULE.

 

 
