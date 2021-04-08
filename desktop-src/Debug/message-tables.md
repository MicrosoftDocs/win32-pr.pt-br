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
# <a name="message-tables"></a><span data-ttu-id="06d6c-105">Tabelas de mensagens</span><span class="sxs-lookup"><span data-stu-id="06d6c-105">Message Tables</span></span>

<span data-ttu-id="06d6c-106">As tabelas de mensagens são recursos especiais de cadeia de caracteres usados ao exibir mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="06d6c-106">Message tables are special string resources used when displaying error messages.</span></span> <span data-ttu-id="06d6c-107">Eles são declarados em um arquivo de recurso usando a instrução de definição de recurso [messagetable](../menurc/messagetable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="06d6c-107">They are declared in a resource file using the [MESSAGETABLE](../menurc/messagetable-resource.md) resource-definition statement.</span></span> <span data-ttu-id="06d6c-108">Para acessar as cadeias de caracteres de mensagem, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="06d6c-108">To access the message strings, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="06d6c-109">O sistema fornece uma tabela de mensagens para os [códigos de erro do sistema](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="06d6c-109">The system provides a message table for the [system error codes](system-error-codes.md).</span></span> <span data-ttu-id="06d6c-110">Para recuperar a cadeia de caracteres que corresponde ao código de erro, chame [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema.</span><span class="sxs-lookup"><span data-stu-id="06d6c-110">To retrieve the string that corresponds to the error code, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag.</span></span>

<span data-ttu-id="06d6c-111">Para fornecer uma tabela de mensagens para seu aplicativo, siga as instruções em [arquivos de texto da mensagem](../eventlog/message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="06d6c-111">To provide a message table for your application, follow the instructions in [Message Text Files](../eventlog/message-text-files.md).</span></span> <span data-ttu-id="06d6c-112">Para recuperar cadeias de caracteres da tabela de mensagens, chame [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a \_ mensagem \_ de formato do \_ sinalizador HMODULE.</span><span class="sxs-lookup"><span data-stu-id="06d6c-112">To retrieve strings from your message table, call [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) with the FORMAT\_MESSAGE\_FROM\_HMODULE flag.</span></span>

 

 
