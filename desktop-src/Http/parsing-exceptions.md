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
# <a name="parsing-exceptions"></a>Analisando exceções

A API do servidor HTTP fornece chaves do registro para dar suporte à análise de exceções para a especificação HTTP/1.1 para compatibilidade com versões anteriores. Essas exceções não são habilitadas por padrão e só devem ser habilitadas caso a caso, quando o servidor experimenta problemas de compatibilidade com clientes HTTP. Esses valores são criados no seguinte local do registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

A tabela a seguir lista as chaves do registro fornecidas para dar suporte às exceções listadas. Para habilitar uma exceção, defina o valor de chave correspondente como 1 e reinicie o serviço HTTP.



| Nome da chave                              | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)     | Permite que o analisador HTTP aceite nomes de cabeçalho com caracteres separadores, como '? '.                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)    | Permite que o analisador HTTP aceite valores de cabeçalho com caracteres de controle brutos (sem escape) nele.                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)     | Permite que o analisador HTTP aceite métodos/verbos HTTP minúsculos, como "Get".                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD) | Permite que o analisador HTTP aceite caracteres de controle em absPath e cadeias de caracteres de consulta da URL. No caso de uma URL absoluta, os caracteres de controle não serão permitidos no nome do host. Todos os tipos de URLs, ou seja, UTF8, DBCS e ANSI, permitirão caracteres de controle. Todos os caracteres de controle ASCII, exceto NUL (0x00), LF (0x0A), CR (0x0D) e tabulação horizontal (0x09) serão permitidos. |



 

 

 




