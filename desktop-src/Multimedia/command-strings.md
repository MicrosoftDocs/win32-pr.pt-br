---
title: Cadeias de caracteres de comando
description: Cadeias de caracteres de comando
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Cadeias de caracteres de comando MCI, sobre
- Cadeias de caracteres de comando MCI, sintaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365849"
---
# <a name="command-strings"></a><span data-ttu-id="ee49d-105">Cadeias de caracteres de comando</span><span class="sxs-lookup"><span data-stu-id="ee49d-105">Command Strings</span></span>

<span data-ttu-id="ee49d-106">Para enviar um comando de cadeia de caracteres para um dispositivo MCI, use a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , que inclui parâmetros para o comando de cadeia de caracteres e um buffer para qualquer informação retornada.</span><span class="sxs-lookup"><span data-stu-id="ee49d-106">To send a string command to an MCI device, use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, which includes parameters for the string command and a buffer for any returned information.</span></span>

<span data-ttu-id="ee49d-107">A função **mciSendString** retornará zero se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ee49d-107">The **mciSendString** function returns zero if successful.</span></span> <span data-ttu-id="ee49d-108">Se a função falhar, a palavra de ordem inferior do valor de retorno conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="ee49d-108">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="ee49d-109">Você pode passar esse código de erro para a função [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obter uma descrição de texto do erro.</span><span class="sxs-lookup"><span data-stu-id="ee49d-109">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-strings"></a><span data-ttu-id="ee49d-110">Sintaxe de cadeias de caracteres de comando</span><span class="sxs-lookup"><span data-stu-id="ee49d-110">Syntax of Command Strings</span></span>

<span data-ttu-id="ee49d-111">As cadeias de caracteres de comando MCI usam uma sintaxe de modificador de objeto verbo consistente.</span><span class="sxs-lookup"><span data-stu-id="ee49d-111">MCI command strings use a consistent verb-object-modifier syntax.</span></span> <span data-ttu-id="ee49d-112">Cada cadeia de caracteres de comando inclui um comando, um identificador de dispositivo e argumentos de comando.</span><span class="sxs-lookup"><span data-stu-id="ee49d-112">Each command string includes a command, a device identifier, and command arguments.</span></span> <span data-ttu-id="ee49d-113">Os argumentos são opcionais para alguns comandos e são necessários para outros.</span><span class="sxs-lookup"><span data-stu-id="ee49d-113">Arguments are optional for some commands and required for others.</span></span>

<span data-ttu-id="ee49d-114">Uma cadeia de caracteres de comando tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="ee49d-114">A command string has the following form:</span></span>

<span data-ttu-id="ee49d-115">*argumentos de ID do dispositivo de comando \_*</span><span class="sxs-lookup"><span data-stu-id="ee49d-115">*command device\_id arguments*</span></span>

<span data-ttu-id="ee49d-116">Esses componentes contêm as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="ee49d-116">These components contain the following information:</span></span>

-   <span data-ttu-id="ee49d-117">O *comando* especifica um comando MCI, como [**abrir**](open.md), [**Fechar**](close.md)ou [**reproduzir**](play.md).</span><span class="sxs-lookup"><span data-stu-id="ee49d-117">The *command* specifies an MCI command, such as [**open**](open.md), [**close**](close.md), or [**play**](play.md).</span></span>
-   <span data-ttu-id="ee49d-118">A *\_ ID do dispositivo* identifica uma instância de um driver MCI.</span><span class="sxs-lookup"><span data-stu-id="ee49d-118">The *device\_id* identifies an instance of an MCI driver.</span></span> <span data-ttu-id="ee49d-119">A *\_ ID do dispositivo* é criada quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="ee49d-119">The *device\_id* is created when the device is opened.</span></span>
-   <span data-ttu-id="ee49d-120">Os *argumentos* especificam os sinalizadores e as variáveis usadas pelo comando.</span><span class="sxs-lookup"><span data-stu-id="ee49d-120">The *arguments* specify the flags and variables used by the command.</span></span> <span data-ttu-id="ee49d-121">Os sinalizadores são palavras-chave reconhecidas com o comando MCI.</span><span class="sxs-lookup"><span data-stu-id="ee49d-121">Flags are keywords recognized with the MCI command.</span></span> <span data-ttu-id="ee49d-122">Variáveis são números ou cadeias de caracteres que se aplicam ao comando ou sinalizador MCI.</span><span class="sxs-lookup"><span data-stu-id="ee49d-122">Variables are numbers or strings that apply to the MCI command or flag.</span></span>

    <span data-ttu-id="ee49d-123">Por exemplo, o comando **reproduzir** usa os argumentos "da *posição* " e "para *posição* " para indicar as posições nas quais iniciar e terminar reprodução.</span><span class="sxs-lookup"><span data-stu-id="ee49d-123">For example, the **play** command uses the arguments "from *position* " and "to *position* " to indicate the positions at which to start and end play.</span></span> <span data-ttu-id="ee49d-124">Você pode listar os sinalizadores usados com um comando em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="ee49d-124">You can list the flags used with a command in any order.</span></span> <span data-ttu-id="ee49d-125">Ao usar um sinalizador que tem uma variável associada a ele, você deve fornecer um valor para a variável.</span><span class="sxs-lookup"><span data-stu-id="ee49d-125">When you use a flag that has a variable associated with it, you must supply a value for the variable.</span></span>

    <span data-ttu-id="ee49d-126">Os argumentos de comando não especificados (e opcionais) assumem um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="ee49d-126">Unspecified (and optional) command arguments assume a default value.</span></span>

<span data-ttu-id="ee49d-127">A função de exemplo a seguir envia o comando [**Play**](play.md) com os sinalizadores "from" e "to".</span><span class="sxs-lookup"><span data-stu-id="ee49d-127">The following example function sends the [**play**](play.md) command with the "from" and "to" flags.</span></span>


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a><span data-ttu-id="ee49d-128">Tipos de dados para variáveis de comando</span><span class="sxs-lookup"><span data-stu-id="ee49d-128">Data Types for Command Variables</span></span>

<span data-ttu-id="ee49d-129">Você pode usar os seguintes tipos de dados para as variáveis em uma cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="ee49d-129">You can use the following data types for the variables in a command string.</span></span>



| <span data-ttu-id="ee49d-130">**Data type**</span><span class="sxs-lookup"><span data-stu-id="ee49d-130">**Data type**</span></span>        | <span data-ttu-id="ee49d-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ee49d-131">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee49d-132">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="ee49d-132">Strings</span></span>              | <span data-ttu-id="ee49d-133">Os tipos de dados de cadeia de caracteres são delimitados por espaços em branco à esquerda e à direita e aspas.</span><span class="sxs-lookup"><span data-stu-id="ee49d-133">String data types are delimited by leading and trailing white spaces and quotation marks.</span></span> <span data-ttu-id="ee49d-134">O MCI remove aspas simples de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ee49d-134">MCI removes single quotation marks from a string.</span></span> <span data-ttu-id="ee49d-135">Para colocar uma aspa em uma cadeia de caracteres, use um conjunto de duas aspas em que você deseja inserir as aspas.</span><span class="sxs-lookup"><span data-stu-id="ee49d-135">To put a quotation mark in a string, use a set of two quotation marks where you want to embed your quotation mark.</span></span> <span data-ttu-id="ee49d-136">Para usar uma cadeia de caracteres vazia, use duas aspas delimitadas por espaços em branco à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="ee49d-136">To use an empty string, use two quotation marks delimited by leading and trailing white spaces.</span></span> |
| <span data-ttu-id="ee49d-137">Inteiros longos assinados</span><span class="sxs-lookup"><span data-stu-id="ee49d-137">Signed long integers</span></span> | <span data-ttu-id="ee49d-138">Os tipos de dados inteiros longos assinados são delimitados por espaços em branco à esquerda e à direita.</span><span class="sxs-lookup"><span data-stu-id="ee49d-138">Signed long integer data types are delimited by leading and trailing white spaces.</span></span> <span data-ttu-id="ee49d-139">A menos que especificado de outra forma, os inteiros podem ser positivos ou negativos.</span><span class="sxs-lookup"><span data-stu-id="ee49d-139">Unless otherwise specified, integers can be positive or negative.</span></span> <span data-ttu-id="ee49d-140">Se você usar inteiros negativos, não deverá separar o sinal de subtração e o primeiro dígito por um espaço.</span><span class="sxs-lookup"><span data-stu-id="ee49d-140">If you use negative integers, you should not separate the minus sign and the first digit with a space.</span></span>                                                                                                    |
| <span data-ttu-id="ee49d-141">Retângulos</span><span class="sxs-lookup"><span data-stu-id="ee49d-141">Rectangles</span></span>           | <span data-ttu-id="ee49d-142">Os tipos de dados Rectangle são uma lista ordenada de quatro valores curtos assinados.</span><span class="sxs-lookup"><span data-stu-id="ee49d-142">Rectangle data types are an ordered list of four signed short values.</span></span> <span data-ttu-id="ee49d-143">O espaço em branco delimita esse tipo de dados e separa cada inteiro na lista.</span><span class="sxs-lookup"><span data-stu-id="ee49d-143">White space delimits this data type and separates each integer in the list.</span></span>                                                                                                                                                                                                              |



 

 

 