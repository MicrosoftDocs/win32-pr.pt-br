---
title: LocalServer32
description: Especifica o caminho completo para um aplicativo de servidor local de 32 bits.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- COM chave do registro LocalServer32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104499170"
---
# <a name="localserver32"></a><span data-ttu-id="8d843-104">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="8d843-104">LocalServer32</span></span>

<span data-ttu-id="8d843-105">Especifica o caminho completo para um aplicativo de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8d843-105">Specifies the full path to a 32-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="8d843-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="8d843-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a><span data-ttu-id="8d843-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d843-107">Remarks</span></span>

<span data-ttu-id="8d843-108">O valor **ServerExecutable** , que é do tipo **reg \_ sz** e tem suporte a partir do Windows Server 2003, funciona em conjunto com a subchave **LocalServer32** para evitar qualquer ambiguidade ao usar a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="8d843-108">The **ServerExecutable** value, which is of type **REG\_SZ** and is supported starting with Windows Server 2003, works in conjunction with the **LocalServer32** subkey to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="8d843-109">**LocalServer32** especifica o local do aplicativo de servidor com a ser iniciado, e essas informações são passadas como o primeiro parâmetro *lpApplicationName* para **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="8d843-109">**LocalServer32** specifies the location of the COM server application to launch, and this information is passed as the first parameter *lpApplicationName* for **CreateProcess**.</span></span> <span data-ttu-id="8d843-110">Dependendo da implementação de **CreateProcess**, essas informações podem ser ambíguas.</span><span class="sxs-lookup"><span data-stu-id="8d843-110">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="8d843-111">Por esse motivo, se **ServerExecutable** for especificado, com passará o valor nomeado **ServerExecutable** para o parâmetro *lpApplicationName* de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="8d843-111">For this reason, if **ServerExecutable** is specified, COM passes the **ServerExecutable** named value to the *lpApplicationName* parameter of **CreateProcess**.</span></span> <span data-ttu-id="8d843-112">Se **ServerExecutable** não for especificado, com passará **NULL** como o valor para o primeiro parâmetro de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="8d843-112">If **ServerExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

<span data-ttu-id="8d843-113">Para ajudar a fornecer segurança do sistema, use cadeias de caracteres entre aspas no caminho para indicar onde o nome do arquivo executável termina e os argumentos começam.</span><span class="sxs-lookup"><span data-stu-id="8d843-113">To help provide system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="8d843-114">Por exemplo, em vez de especificar o seguinte caminho como a entrada **LocalServer32** :</span><span class="sxs-lookup"><span data-stu-id="8d843-114">For example, instead of specifying the following path as the **LocalServer32** entry:</span></span>

<span data-ttu-id="8d843-115">"C: \\ arquivos de programa \\ arquivos da empresa \\Application.exe param1 param2"</span><span class="sxs-lookup"><span data-stu-id="8d843-115">"C:\\Program Files\\Company Files\\Application.exe param1 param2"</span></span>

<span data-ttu-id="8d843-116">Especifique o caminho usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="8d843-116">specify the path using the following syntax:</span></span>

<span data-ttu-id="8d843-117">" \\ C: \\ Program Files \\ arquivos da empresa \\Application.exe\\ " param1 param2 "</span><span class="sxs-lookup"><span data-stu-id="8d843-117">"\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2"</span></span>

<span data-ttu-id="8d843-118">COM anexa o sinalizador "-incorporando" à cadeia de caracteres, de modo que o aplicativo que usa sinalizadores precisa analisar toda a cadeia de caracteres e verificar o sinalizador de incorporação.</span><span class="sxs-lookup"><span data-stu-id="8d843-118">COM appends the "-Embedding" flag to the string, so the application that uses flags needs to parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="8d843-119">Quando o COM inicia um servidor local de 32 bits, o servidor deve registrar um objeto de classe dentro de um tempo decorrido definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="8d843-119">When COM starts a 32-bit local server, the server must register a class object within an elapsed time set by the user.</span></span> <span data-ttu-id="8d843-120">Por padrão, o valor de tempo decorrido deve ser de pelo menos 5 minutos, em milissegundos, mas não pode exceder o número de milissegundos em 30 dias.</span><span class="sxs-lookup"><span data-stu-id="8d843-120">By default, the elapsed time value must be at least 5 minutes, in milliseconds, but cannot exceed the number of milliseconds in 30 days.</span></span> <span data-ttu-id="8d843-121">Normalmente, os aplicativos não devem definir esse valor, que está na entrada **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ COM2 \\ ServerStartElapsedTime** .</span><span class="sxs-lookup"><span data-stu-id="8d843-121">Applications typically should not set this value, which is in the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\COM2\\ServerStartElapsedTime** entry.</span></span>

<span data-ttu-id="8d843-122">As entradas necessárias para servidores locais de 32 bits são [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** e [**insertáveis**](insertable.md).</span><span class="sxs-lookup"><span data-stu-id="8d843-122">The required entries for 32-bit local servers are [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32**, and [**Insertable**](insertable.md).</span></span>

<span data-ttu-id="8d843-123">Se um contêiner estiver pesquisando o registro de um servidor local, um servidor local de 32 bits terá prioridade sobre um servidor local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8d843-123">If a container is searching the registry for a local server, a 32-bit local server has priority over a 16-bit local server.</span></span>

<span data-ttu-id="8d843-124">Se você estiver implementando classes como serviços, deve estar ciente de que o [**LocalService**](localservice.md) nomeado Value é usado em preferência à chave **LocalServer32** para ativação local e remota requestsâ € "se o **LocalService** existir e se referir a um serviço válido, a chave **LocalServer32** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="8d843-124">If you are implementing classes as services, you should be aware that the [**LocalService**](localservice.md) named value is used in preference to the **LocalServer32** key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d843-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d843-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d843-126">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="8d843-126">**LocalServer**</span></span>](localserver.md)
</dt> <dt>

[<span data-ttu-id="8d843-127">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="8d843-127">**LocalService**</span></span>](localservice.md)
</dt> </dl>

 

 