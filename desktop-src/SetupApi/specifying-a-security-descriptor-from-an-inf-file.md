---
description: Você pode controlar a capacidade de um processo de acessar objetoscuráveis ou executar tarefas de administração do sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Especificando um descritor de segurança de um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52267f443bf20fe8a9b71a64e2422ac43688d7a54bca2692f1b61ad891fda8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964832"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Especificando um descritor de segurança de um arquivo INF

Você pode controlar a capacidade de um processo de acessar objetoscuráveis ou executar tarefas de administração do sistema. Um objeto seguro é um objeto que pode ter um descritor de segurança. Todos os objetos nomeados sãocuráveis. Alguns objetos sem nome, como objetos de processo e thread, também podem ter descritores de segurança. Para obter mais informações sobre como controlar o acesso a objetos de segurança, consulte [Controle de acesso](/windows/desktop/SecAuthZ/access-control).

[Os descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors) contêm as informações de segurança associadas a objetos de segurança. Para a maioria dos objetos de segurança, você pode especificar o descritor de segurança de um objeto na chamada de função que cria o objeto . Por exemplo, você pode especificar um descritor de segurança nas [**funções CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Para definir um descritor de segurança de um arquivo INF, adicione uma seção Segurança criado pelo inf-writer imediatamente após a seção que instala o arquivo, a chave do Registro ou o componente. A seção Segurança deve conter uma linha com o descritor de segurança de cadeia de caracteres gravado nele usando o formato para [Cadeias de Caracteres do Descritor de Segurança](/windows/desktop/SecAuthZ/security-descriptor-strings). A linha também deve ser entre aspas (").

Por exemplo, o snippet de arquivo INF a seguir criaria uma chave do Registro à qual apenas os administradores e o sistema têm acesso. Observe que este exemplo requer privilégios administrativos.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

Nesse caso, o significado da cadeia de caracteres é que os administradores têm controle total, o sistema tem controle total e o acesso é herdável para todas as sub-chaves. Para obter mais informações, consulte [Linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
