---
description: As tabelas de mensagens são recursos especiais de cadeia de caracteres usados ao exibir mensagens de erro. Eles são declarados em um arquivo de recurso usando a instrução de definição de recurso MESSAGEtable. Para acessar as cadeias de caracteres de mensagem, use a função FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Tabelas de mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920172"
---
# <a name="message-tables"></a>Tabelas de mensagens

As tabelas de mensagens são recursos especiais de cadeia de caracteres usados ao exibir mensagens de erro. Eles são declarados em um arquivo de recurso usando a instrução de definição de recurso [messagetable](../menurc/messagetable-resource.md) . Para acessar as cadeias de caracteres de mensagem, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .

O sistema fornece uma tabela de mensagens para os [códigos de erro do sistema](system-error-codes.md). Para recuperar a cadeia de caracteres que corresponde ao código de erro, chame [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema.

Para fornecer uma tabela de mensagens para seu aplicativo, siga as instruções em [arquivos de texto da mensagem](../eventlog/message-text-files.md). Para recuperar cadeias de caracteres da tabela de mensagens, chame [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a \_ mensagem \_ de formato do \_ sinalizador HMODULE.

 

 
