---
description: Você pode controlar a capacidade de um processo de acessar objetos protegíveis ou executar tarefas de administração do sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Especificando um descritor de segurança de um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922729"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Especificando um descritor de segurança de um arquivo INF

Você pode controlar a capacidade de um processo de acessar objetos protegíveis ou executar tarefas de administração do sistema. Um objeto protegível é um objeto que pode ter um descritor de segurança. Todos os objetos nomeados são protegíveis. Alguns objetos sem nome, como objetos de processo e thread, também podem ter descritores de segurança. Para obter mais informações sobre como controlar o acesso a objetos protegíveis, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).

[Descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors) contêm as informações de segurança associadas a objetos protegíveis. Para a maioria dos objetos protegíveis, você pode especificar o descritor de segurança de um objeto na chamada de função que cria o objeto. Por exemplo, você pode especificar um descritor de segurança nas funções [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Para definir um descritor de segurança de um arquivo INF, adicione uma seção segurança de criação de INF-Writer imediatamente após a seção que instala o arquivo, a chave do registro ou o componente. A seção de segurança deve conter uma linha com descritor de segurança de cadeia de caracteres escrito usando o formato para [cadeias de caracteres de descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-strings). A linha também deve ser colocada entre aspas (").

Por exemplo, o seguinte trecho de arquivo INF criaria uma chave do registro para a qual somente os administradores e o sistema têm acesso. Observe que este exemplo requer privilégios administrativos.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

Nesse caso, o significado da cadeia de caracteres é que os administradores têm controle total, o sistema tem controle total e o acesso é herdável para todas as subchaves. Para obter mais informações, consulte [linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
