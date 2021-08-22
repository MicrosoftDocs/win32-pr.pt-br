---
title: Gerando o UUID
description: A primeira etapa na definição da interface é usar o utilitário Uuidgen para gerar um UUID (identificador universal exclusivo).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- RPC de chamada de procedimento remoto, tarefas, gerando o UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c1fbb257a4ce41a4fc0159f703a01705b4dd5926356d7850ec4ce1e0d2e002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929523"
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

 

 




