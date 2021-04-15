---
description: Identificadores de evento identificam exclusivamente um evento específico.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificadores de evento (log de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502062"
---
# <a name="event-identifiers-event-logging"></a><span data-ttu-id="9f484-103">Identificadores de evento (log de eventos)</span><span class="sxs-lookup"><span data-stu-id="9f484-103">Event Identifiers (Event Logging)</span></span>

<span data-ttu-id="9f484-104">Identificadores de evento identificam exclusivamente um evento específico.</span><span class="sxs-lookup"><span data-stu-id="9f484-104">Event identifiers uniquely identify a particular event.</span></span> <span data-ttu-id="9f484-105">Cada [origem de evento](event-sources.md) pode definir seus próprios eventos numerados e as cadeias de caracteres de descrição para as quais eles são mapeados em seu arquivo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9f484-105">Each [event source](event-sources.md) can define its own numbered events and the description strings to which they are mapped in its message file.</span></span> <span data-ttu-id="9f484-106">Os visualizadores de eventos podem apresentar essas cadeias de caracteres ao usuário.</span><span class="sxs-lookup"><span data-stu-id="9f484-106">Event viewers can present these strings to the user.</span></span> <span data-ttu-id="9f484-107">Eles devem ajudar o usuário a entender o que deu errado e a sugerir as ações a serem tomadas.</span><span class="sxs-lookup"><span data-stu-id="9f484-107">They should help the user understand what went wrong and suggest what actions to take.</span></span> <span data-ttu-id="9f484-108">Direcione a descrição para os usuários que resolvem seus próprios problemas, não para administradores ou técnicos de suporte.</span><span class="sxs-lookup"><span data-stu-id="9f484-108">Direct the description at users solving their own problems, not at administrators or support technicians.</span></span> <span data-ttu-id="9f484-109">Para obter mais informações, consulte [diretrizes de mensagem de erro](/windows/desktop/Debug/error-message-guidelines).</span><span class="sxs-lookup"><span data-stu-id="9f484-109">For more information, see [Error Message Guidelines](/windows/desktop/Debug/error-message-guidelines).</span></span>

## <a name="format"></a><span data-ttu-id="9f484-110">Formatar</span><span class="sxs-lookup"><span data-stu-id="9f484-110">Format</span></span>

<span data-ttu-id="9f484-111">O diagrama a seguir ilustra o formato de um identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="9f484-111">The following diagram illustrates the format of an event identifier.</span></span>

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span data-ttu-id="9f484-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev</span><span class="sxs-lookup"><span data-stu-id="9f484-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev</span></span>
</dt> <dd>

<span data-ttu-id="9f484-113">Gravidade.</span><span class="sxs-lookup"><span data-stu-id="9f484-113">Severity.</span></span> <span data-ttu-id="9f484-114">A severidade é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9f484-114">The severity is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="9f484-115">00-êxito</span><span class="sxs-lookup"><span data-stu-id="9f484-115">00 - Success</span></span></dd> <dd><span data-ttu-id="9f484-116">01-informativo</span><span class="sxs-lookup"><span data-stu-id="9f484-116">01 - Informational</span></span></dd> <dd><span data-ttu-id="9f484-117">10-aviso</span><span class="sxs-lookup"><span data-stu-id="9f484-117">10 - Warning</span></span></dd> <dd><span data-ttu-id="9f484-118">11-erro</span><span class="sxs-lookup"><span data-stu-id="9f484-118">11 - Error</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="9f484-119"><span id="C"></span><span id="c"></span>&</span><span class="sxs-lookup"><span data-stu-id="9f484-119"><span id="C"></span><span id="c"></span>C</span></span>
</dt> <dd>

<span data-ttu-id="9f484-120">Bit do cliente.</span><span class="sxs-lookup"><span data-stu-id="9f484-120">Customer bit.</span></span> <span data-ttu-id="9f484-121">Esse bit é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9f484-121">This bit is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="9f484-122">0-código do sistema</span><span class="sxs-lookup"><span data-stu-id="9f484-122">0 - System code</span></span></dd> <dd><span data-ttu-id="9f484-123">1-código do cliente</span><span class="sxs-lookup"><span data-stu-id="9f484-123">1 - Customer code</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="9f484-124"><span id="R"></span><span id="r"></span>D</span><span class="sxs-lookup"><span data-stu-id="9f484-124"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="9f484-125">Bit reservado.</span><span class="sxs-lookup"><span data-stu-id="9f484-125">Reserved bit.</span></span>

</dd> <dt>

<span data-ttu-id="9f484-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Saldo</span><span class="sxs-lookup"><span data-stu-id="9f484-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Facility</span></span>
</dt> <dd>

<span data-ttu-id="9f484-127">Código de instalação.</span><span class="sxs-lookup"><span data-stu-id="9f484-127">Facility code.</span></span> <span data-ttu-id="9f484-128">Esse valor pode ser um recurso \_ nulo.</span><span class="sxs-lookup"><span data-stu-id="9f484-128">This value can be FACILITY\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="9f484-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Auto-completar</span><span class="sxs-lookup"><span data-stu-id="9f484-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

<span data-ttu-id="9f484-130">Código de status para a instalação.</span><span class="sxs-lookup"><span data-stu-id="9f484-130">Status code for the facility.</span></span>

</dd> </dl>

## <a name="message-definitions"></a><span data-ttu-id="9f484-131">Definições de mensagem</span><span class="sxs-lookup"><span data-stu-id="9f484-131">Message Definitions</span></span>

<span data-ttu-id="9f484-132">As mensagens são definidas no arquivo de mensagem de evento.</span><span class="sxs-lookup"><span data-stu-id="9f484-132">Messages are defined in the event message file.</span></span> <span data-ttu-id="9f484-133">As cadeias de caracteres de descrição no arquivo de mensagem de evento são indexadas pelo identificador de evento, permitindo que Visualizador de Eventos exiba texto específico de evento para qualquer evento com base no identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="9f484-133">The description strings in the event message file are indexed by event identifier, enabling Event Viewer to display event-specific text for any event based on the event identifier.</span></span> <span data-ttu-id="9f484-134">Todas as descrições são localizadas e dependentes do idioma.</span><span class="sxs-lookup"><span data-stu-id="9f484-134">All descriptions are localized and language dependent.</span></span> <span data-ttu-id="9f484-135">Para obter mais informações sobre como criar um arquivo de mensagem, consulte [arquivos de texto da mensagem](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="9f484-135">For more information on building a message file, see [Message Text Files](message-text-files.md).</span></span>

<span data-ttu-id="9f484-136">As cadeias de caracteres de descrição podem conter espaços reservados de cadeia de inserção, do formato%*n*, onde %1 indica a primeira cadeia de caracteres de inserção e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9f484-136">The description strings may contain insertion string placeholders, of the form %*n*, where %1 indicates the first insertion string, and so on.</span></span> <span data-ttu-id="9f484-137">Por exemplo, veja a seguir um exemplo de entrada no arquivo. MC:</span><span class="sxs-lookup"><span data-stu-id="9f484-137">For example, the following is a sample entry in the .mc file:</span></span>

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

<span data-ttu-id="9f484-138">Nesse caso, o buffer retornado por [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contém cadeias de caracteres de inserção.</span><span class="sxs-lookup"><span data-stu-id="9f484-138">In this case, the buffer returned by [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contains insertion strings.</span></span> <span data-ttu-id="9f484-139">O membro **NumStrings** da estrutura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica o número de cadeias de caracteres de inserção.</span><span class="sxs-lookup"><span data-stu-id="9f484-139">The **NumStrings** member of the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure indicates the number of insertion strings.</span></span> <span data-ttu-id="9f484-140">O membro **StringOffset** da estrutura **EVENTLOGRECORD** indica o local da primeira cadeia de caracteres de inserção no buffer.</span><span class="sxs-lookup"><span data-stu-id="9f484-140">The **StringOffset** member of the **EVENTLOGRECORD** structure indicates the location of the first insertion string in the buffer.</span></span> <span data-ttu-id="9f484-141">Você pode passar uma matriz de \_ Ptrs DWORD que aponta para o endereço de cada cadeia de caracteres no buffer ao chamar a função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e irá inserir as cadeias de caracteres na mensagem.</span><span class="sxs-lookup"><span data-stu-id="9f484-141">You can pass an array of DWORD\_PTRs that point to the address each string in the buffer when calling the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function and it will insert the strings into the message.</span></span>

<span data-ttu-id="9f484-142">A cadeia de caracteres de descrição também pode conter espaços reservados para cadeias de caracteres de parâmetro do arquivo de mensagem de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f484-142">The description string can also contain placeholders for parameter strings from the parameter message file.</span></span> <span data-ttu-id="9f484-143">Os espaços reservados estão no formato%%*n*, onde% %1 é substituído pela cadeia de caracteres do parâmetro com o identificador de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9f484-143">The placeholders are of the form %%*n*, where %%1 is replaced by the parameter string with the identifier of 1, and so on.</span></span> <span data-ttu-id="9f484-144">No entanto, cabe a você inserir as cadeias de caracteres de parâmetro na cadeia de mensagem que [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) retorna.</span><span class="sxs-lookup"><span data-stu-id="9f484-144">However, it is up to you to insert the parameter strings into the message string that [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) returns.</span></span> <span data-ttu-id="9f484-145">Normalmente, você chama **FormatMessage** para obter a cadeia de caracteres da mensagem para o evento.</span><span class="sxs-lookup"><span data-stu-id="9f484-145">Typically, you call **FormatMessage** to get the message string for the event.</span></span> <span data-ttu-id="9f484-146">Em seguida, analise a cadeia de caracteres da mensagem para%%*n* parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9f484-146">You then parse the message string for %%*n* parameters.</span></span> <span data-ttu-id="9f484-147">Se a mensagem contiver um ou mais parâmetros, carregue o valor do registro **ParameterMessageFile** para a origem.</span><span class="sxs-lookup"><span data-stu-id="9f484-147">If the message contains one or more parameters, load the **ParameterMessageFile** registry value for the source.</span></span> <span data-ttu-id="9f484-148">Para cada parâmetro na cadeia de caracteres de mensagem, obtenha o identificador e passe-o para **FormatMessage** para obter a cadeia de caracteres do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f484-148">For each parameter in the message string, get the identifier and pass it to **FormatMessage** to get the parameter string.</span></span> <span data-ttu-id="9f484-149">Substitua o parâmetro na cadeia de caracteres de mensagem pela cadeia de caracteres de parâmetro retornada por **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="9f484-149">Replace the parameter in the message string with the parameter string that **FormatMessage** returned.</span></span>

## <a name="insertion-strings"></a><span data-ttu-id="9f484-150">Cadeias de caracteres de inserção</span><span class="sxs-lookup"><span data-stu-id="9f484-150">Insertion Strings</span></span>

<span data-ttu-id="9f484-151">Cadeias de caracteres de inserção são cadeias de caracteres opcionais independentes de idioma usadas para preencher valores para espaços reservados em cadeias de caracteres de descrição.</span><span class="sxs-lookup"><span data-stu-id="9f484-151">Insertion strings are optional language-independent strings used to fill in values for placeholders in description strings.</span></span> <span data-ttu-id="9f484-152">Como as cadeias de caracteres não são localizadas, é essencial que esses espaços reservados sejam usados apenas para representar cadeias de caracteres independentes de idioma, como valores numéricos, nomes de arquivos, nomes de usuário e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9f484-152">Because the strings are not localized, it is critical that these placeholders be used only to represent language-independent strings such as numeric values, file names, user names, and so on.</span></span> <span data-ttu-id="9f484-153">O comprimento da cadeia de caracteres não deve exceder 32 quilobytes-1 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9f484-153">The string length must not exceed 32 kilobytes - 1 characters.</span></span>

<span data-ttu-id="9f484-154">Evite usar várias cadeias de caracteres para criar uma descrição maior.</span><span class="sxs-lookup"><span data-stu-id="9f484-154">Avoid using several strings to create a larger description.</span></span> <span data-ttu-id="9f484-155">Uma cadeia de caracteres de inserção deve ser tratada como dados, não texto.</span><span class="sxs-lookup"><span data-stu-id="9f484-155">An insertion string should be treated as data, not text.</span></span> <span data-ttu-id="9f484-156">Por exemplo, no exemplo a seguir, pszString1 e pszString2 não devem ser usados como cadeias de caracteres de inserção para pszDescription.</span><span class="sxs-lookup"><span data-stu-id="9f484-156">For example, in the following example, pszString1 and pszString2 should not be used as insertion strings for pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

<span data-ttu-id="9f484-157">No exemplo a seguir, é apropriado usar pszString1 ou pszString2 para a cadeia de caracteres de inserção em pszDescription.</span><span class="sxs-lookup"><span data-stu-id="9f484-157">In the following example, it is appropriate to use either pszString1 or pszString2 for the insertion string in pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
