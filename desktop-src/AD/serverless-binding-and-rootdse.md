---
title: Associação sem servidor e RootDSE
description: Se possível, não em código um nome de servidor.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Associação sem servidor e RootDSE AD
- AD de associação sem servidor
- RootDSE AD
- Active Directory, Using, Binding, Serverless Binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3c88386ae95efdebd031199e135ff4c5d610e402b9cba522256df5eef097e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024924"
---
# <a name="serverless-binding-and-rootdse"></a>Associação sem servidor e RootDSE

Se possível, não em código um nome de servidor. Além disso, na maioria das circunstâncias, a associação não deve ser desnecessariamente vinculada a um único servidor. Active Directory Domain Services suporte à associação sem servidor, o que significa que o Active Directory pode ser vinculado ao no domínio padrão sem especificar o nome de um controlador de domínio. Para aplicativos comuns, esse normalmente é o domínio do usuário conectado. Para aplicativos de serviço, esse é o domínio da conta de logon do serviço ou o do cliente que o serviço representa.

No LDAP 3.0, rootDSE é definido como a raiz da árvore de dados de diretório em um servidor de diretório. O rootDSE não faz parte de nenhum namespace. A finalidade do rootDSE é fornecer dados sobre o servidor de diretório. A seguir está a cadeia de caracteres de associação usada para se vincular ao rootDSE.


```C++
LDAP://<servername>/rootDSE
```



O <servername> é o nome DNS de um servidor. O <servername> é opcional, conforme mostrado no formato a seguir.


```C++
LDAP://rootDSE
```



Nesse caso, um controlador de domínio padrão do domínio em que o contexto de segurança do thread de chamada está será usado. Se um controlador de domínio não puder ser acessado no site, o primeiro controlador de domínio que puder ser encontrado será usado.

O rootDSE é um local conhecido e confiável em cada servidor de diretório para obter nomes diferenciados do domínio, esquema e contêineres de configuração e outros dados sobre o servidor e o conteúdo de sua árvore de dados de diretório. Essas propriedades raramente mudam em um servidor específico. Um aplicativo pode ler essas propriedades na inicialização e usá-las durante toda a sessão.

Em resumo, um aplicativo deve usar a associação sem servidor para se vincular ao diretório no domínio atual, usar rootDSE para obter o nome diferenciado de um namespace e usar esse nome diferenciado para se vincular a objetos no namespace.

Para obter mais informações sobre atributos com suporte pelo rootDSE, consulte [RootDSE](/windows/desktop/ADSchema/rootdse) na documentação do Esquema do Active Directory.

Para obter mais informações e um exemplo de código que mostra como usar a associação sem servidor e rootDSE, consulte Código de exemplo para obter o nome [diferenciado do domínio](example-code-for-getting-the-distinguished-name-of-the-domain.md).

 

 