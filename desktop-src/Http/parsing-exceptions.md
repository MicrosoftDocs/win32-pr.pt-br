---
title: Analisando exceções
description: A API do servidor HTTP fornece chaves do registro para dar suporte à análise de exceções para a especificação HTTP/1.1 para compatibilidade com versões anteriores.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analisando exceções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916380"
---
# <a name="parsing-exceptions"></a><span data-ttu-id="f4392-104">Analisando exceções</span><span class="sxs-lookup"><span data-stu-id="f4392-104">Parsing Exceptions</span></span>

<span data-ttu-id="f4392-105">A API do servidor HTTP fornece chaves do registro para dar suporte à análise de exceções para a especificação HTTP/1.1 para compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="f4392-105">HTTP Server API provides registry keys to support parsing exceptions to the HTTP/1.1 specification for backward compatibility.</span></span> <span data-ttu-id="f4392-106">Essas exceções não são habilitadas por padrão e só devem ser habilitadas caso a caso, quando o servidor experimenta problemas de compatibilidade com clientes HTTP.</span><span class="sxs-lookup"><span data-stu-id="f4392-106">These exceptions are not enabled by default and should be enabled only on a case-by-case basis, when the server experiences compatibility issues with HTTP clients.</span></span> <span data-ttu-id="f4392-107">Esses valores são criados no seguinte local do registro:</span><span class="sxs-lookup"><span data-stu-id="f4392-107">These values are created under the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

<span data-ttu-id="f4392-108">A tabela a seguir lista as chaves do registro fornecidas para dar suporte às exceções listadas.</span><span class="sxs-lookup"><span data-stu-id="f4392-108">The following table lists registry keys provided to support the exceptions listed.</span></span> <span data-ttu-id="f4392-109">Para habilitar uma exceção, defina o valor de chave correspondente como 1 e reinicie o serviço HTTP.</span><span class="sxs-lookup"><span data-stu-id="f4392-109">To enable an exception set the corresponding key value to 1 and restart the HTTP service.</span></span>



| <span data-ttu-id="f4392-110">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="f4392-110">Key name</span></span>                              | <span data-ttu-id="f4392-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4392-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4392-112">AllowWeakHeaderNameSyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="f4392-112">AllowWeakHeaderNameSyntax (DWORD)</span></span>     | <span data-ttu-id="f4392-113">Permite que o analisador HTTP aceite nomes de cabeçalho com caracteres separadores, como '? '.</span><span class="sxs-lookup"><span data-stu-id="f4392-113">Allows the HTTP parser to accept header names with separator characters such as '?'.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f4392-114">AllowWeakHeaderValueSyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="f4392-114">AllowWeakHeaderValueSyntax (DWORD)</span></span>    | <span data-ttu-id="f4392-115">Permite que o analisador HTTP aceite valores de cabeçalho com caracteres de controle brutos (sem escape) nele.</span><span class="sxs-lookup"><span data-stu-id="f4392-115">Allows the HTTP parser to accept header values with raw (unescaped) control characters in it.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f4392-116">AllowCaseInsensitiveVerbs (DWORD)</span><span class="sxs-lookup"><span data-stu-id="f4392-116">AllowCaseInsensitiveVerbs (DWORD)</span></span>     | <span data-ttu-id="f4392-117">Permite que o analisador HTTP aceite métodos/verbos HTTP minúsculos, como "Get".</span><span class="sxs-lookup"><span data-stu-id="f4392-117">Allows the HTTP parser to accept lowercase HTTP methods/verbs such as "get".</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f4392-118">AllowUnEscapedRestrictedChars (DWORD)</span><span class="sxs-lookup"><span data-stu-id="f4392-118">AllowUnEscapedRestrictedChars (DWORD)</span></span> | <span data-ttu-id="f4392-119">Permite que o analisador HTTP aceite caracteres de controle em absPath e cadeias de caracteres de consulta da URL.</span><span class="sxs-lookup"><span data-stu-id="f4392-119">Allows the HTTP parser to accept control characters in abspath and query strings of the URL.</span></span> <span data-ttu-id="f4392-120">No caso de uma URL absoluta, os caracteres de controle não serão permitidos no nome do host.</span><span class="sxs-lookup"><span data-stu-id="f4392-120">In case of an absolute URL, control characters will not be allowed in the hostname.</span></span> <span data-ttu-id="f4392-121">Todos os tipos de URLs, ou seja, UTF8, DBCS e ANSI, permitirão caracteres de controle.</span><span class="sxs-lookup"><span data-stu-id="f4392-121">All flavors of URLs, namely UTF8, DBCS and ANSI, will allow control characters.</span></span> <span data-ttu-id="f4392-122">Todos os caracteres de controle ASCII, exceto NUL (0x00), LF (0x0A), CR (0x0D) e tabulação horizontal (0x09) serão permitidos.</span><span class="sxs-lookup"><span data-stu-id="f4392-122">All ASCII control characters except NUL (0x00), LF (0x0a), CR (0x0d) and Horizontal Tab(0x09) will be allowed.</span></span> |



 

 

 




