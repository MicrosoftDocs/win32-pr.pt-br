---
title: Associação sem servidor e RootDSE
description: Se possível, não codifique um nome de servidor.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Associação sem servidor e o AD RootDSE
- AD sem Associação de servidor
- AD RootDSE
- Active Directory, usando, associação, associação sem servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453906"
---
# <a name="serverless-binding-and-rootdse"></a>Associação sem servidor e RootDSE

Se possível, não codifique um nome de servidor. Além disso, na maioria das circunstâncias, a associação não deve ser desnecessariamente vinculada a um único servidor. Active Directory Domain Services suporte à associação sem servidor, o que significa que Active Directory pode ser associado ao domínio padrão sem especificar o nome de um controlador de domínio. Para aplicativos comuns, normalmente esse é o domínio do usuário conectado. Para aplicativos de serviço, esse é o domínio da conta de logon do serviço ou do cliente que o serviço representa.

No LDAP 3,0, o rootDSE é definido como a raiz da árvore de dados do diretório em um servidor de diretório. O rootDSE não faz parte de nenhum namespace. A finalidade do rootDSE é fornecer dados sobre o servidor de diretório. A seguir está a cadeia de vinculação usada para associar a rootDSE.


```C++
LDAP://<servername>/rootDSE
```



O <servername> é o nome DNS de um servidor. O <servername> é opcional, conforme mostrado no formato a seguir.


```C++
LDAP://rootDSE
```



Nesse caso, um controlador de domínio padrão do domínio no qual o contexto de segurança do thread de chamada está será usado. Se um controlador de domínio não puder ser acessado no site, o primeiro controlador de domínio que pode ser encontrado será usado.

O rootDSE é um local bem conhecido e confiável em cada servidor de diretório para obter nomes distintos do domínio, do esquema e dos contêineres de configuração, além de outros dados sobre o servidor e o conteúdo de sua árvore de dados de diretório. Essas propriedades raramente mudam em um servidor específico. Um aplicativo pode ler essas propriedades na inicialização e usá-las em toda a sessão.

Em resumo, um aplicativo deve usar a associação sem servidor para associar ao diretório no domínio atual, usar rootDSE para obter o nome distinto de um namespace e usar esse nome distinto para associar a objetos no namespace.

Para obter mais informações sobre atributos com suporte do rootDSE, consulte [RootDSE](/windows/desktop/ADSchema/rootdse) na documentação do esquema de Active Directory.

Para obter mais informações e um exemplo de código que mostra como usar a associação sem servidor e o rootDSE, consulte [código de exemplo para obter o nome distinto do domínio](example-code-for-getting-the-distinguished-name-of-the-domain.md).

 

 