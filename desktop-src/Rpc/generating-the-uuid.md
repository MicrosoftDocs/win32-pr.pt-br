---
title: Gerando o UUID
description: A primeira etapa na definição da interface é usar o utilitário Uuidgen para gerar um UUID (identificador universal exclusivo).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- RPC de chamada de procedimento remoto, tarefas, gerando o UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822593"
---
# <a name="generating-the-uuid"></a>Gerando o UUID

A primeira etapa na definição da interface é usar o utilitário **Uuidgen** para gerar um UUID (identificador universal exclusivo). Um UUID permite que os aplicativos cliente e servidor identifiquem um ao outro. O utilitário **Uuidgen** (Uuidgen.exe) é instalado automaticamente quando você instala o SDK (Software Development Kit) da plataforma.

O comando a seguir gera um UUID e cria um arquivo de modelo chamado Hello. idl.

**Uuidgen/i/ohello.idl**

Seu modelo Hello. idl terá a seguinte aparência (com um UUID diferente, é claro).

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




