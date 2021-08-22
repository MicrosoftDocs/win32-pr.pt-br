---
title: Analisar exceções
description: A API do Servidor HTTP fornece chaves do Registro para dar suporte a exceções de análise para a especificação HTTP/1.1 para compatibilidade com compatibilidade com backward.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analisar exceções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b546c5473641bbd5d719908903c2d9e19db25ade2ff6677a5ce5ec7ea472d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950725"
---
# <a name="parsing-exceptions"></a>Analisar exceções

A API do Servidor HTTP fornece chaves do Registro para dar suporte a exceções de análise para a especificação HTTP/1.1 para compatibilidade com compatibilidade com backward. Essas exceções não são habilitadas por padrão e devem ser habilitadas apenas caso a caso, quando o servidor tem problemas de compatibilidade com clientes HTTP. Esses valores são criados no seguinte local do Registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

A tabela a seguir lista as chaves do Registro fornecidas para dar suporte às exceções listadas. Para habilitar uma exceção, de acordo com o valor da chave correspondente como 1 e reinicie o serviço HTTP.



| Nome da chave                              | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)     | Permite que o analisador HTTP aceite nomes de cabeçalho com caracteres separadores, como '?'.                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)    | Permite que o analisador HTTP aceite valores de cabeçalho com caracteres de controle brutos (semscape).                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)     | Permite que o analisador HTTP aceite métodos/verbos HTTP minúsculos, como "get".                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD) | Permite que o analisador HTTP aceite caracteres de controle em abspath e cadeias de caracteres de consulta da URL. No caso de uma URL absoluta, os caracteres de controle não serão permitidos no nome do host. Todas as variantes de URLs, ou seja, UTF8, DBCS e ANSI, permitirão caracteres de controle. Todos os caracteres de controle ASCII, exceto NUL (0x00), LF (0x0a), CR (0x0d) e Tabulação Horizontal(0x09) serão permitidos. |



 

 

 




