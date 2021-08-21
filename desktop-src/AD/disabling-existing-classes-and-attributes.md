---
title: Desabilitando classes e atributos existentes
description: As adições de esquema são permanentes.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a783bc0898cf3ecc883865abde037d1e70c60ec83913f2fb9148e230ae392f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018787"
---
# <a name="disabling-existing-classes-and-attributes"></a>Desabilitando classes e atributos existentes

As adições de esquema são permanentes. Não é possível **excluir objetos attributeSchema** **e classSchema.** Em um sistema distribuído, é difícil garantir que não haja instâncias de uma determinada classe ou atributo. Remover a definição de uma classe ou atributo causa danos a instâncias existentes dessa classe ou atributo.

Você pode desabilitar uma classe ou atributo existente marcando-o como "defunct". Isso não afeta instâncias existentes da classe ou atributo tão marcadas, mas impede a criação de novas instâncias.

As seguintes restrições se aplicam ao desabilitar classes e atributos de esquema:

-   Não é possível desabilitar uma classe ou atributo de Categoria 1.
-   Não é possível desabilitar um atributo que seja membro de uma classe que também não está desabilitada. Isso porque um atributo pode ser necessário para a classe (não desabilitada) e desabilitar o atributo impede que novas instâncias da classe sejam criadas.

Para desabilitar um atributo, de definido o **atributo isDefunct** de **seu objeto attributeSchema** como **TRUE.** Quando um atributo é desabilitado, novas instâncias do atributo não podem ser criadas. Para reabilitar o atributo, de acordo com o **atributo isDefunct** como **FALSE.**

Para desabilitar uma classe, de definido o **atributo isDefunct** de **seu objeto classSchema** como **TRUE.** Quando uma classe é desabilitada, novas instâncias da classe não podem ser criadas. Para reabilitar a classe, de acordo com o **atributo isDefunct** como **FALSE.**

Definir objetos de esquema como defuntivos pode ser útil em ambientes de produção. Quando uma versão de teste de uma extensão de esquema não for mais necessária, marque-a como função. Você pode restaurá-lo removendo o **atributo isDefunct** ou definindo o valor do atributo como **FALSE.** Isso também protege contra uma remoção não intencional de um objeto de esquema definindo-o como defunção porque a operação pode ser revertida facilmente.

Esteja ciente de que o servidor do Active Directory não limpa instâncias existentes de um atributo ou classe quando você faz um objeto de esquema ser desativado. Se você remover a **propriedade isDefunct,** todas as instâncias se tornarão objetos normais e válidos novamente.

A lista a seguir inclui outras consequências da marcação de um **objeto attributeSchema** ou **classSchema** defunção:

-   Falha na adição ou modificação de uma instância.
-   Os códigos de erro se comportam como se uma classe defunção nunca tivesse existido.
-   A pesquisa e a exclusão se comportam como se nenhum objeto de esquema tivesse sido apagado.
-   Permitir apenas a exclusão de atributo inteiro do objeto .

A lista a seguir inclui opções adicionais em um ambiente de produção para reduzir o impacto das extensões de esquemas defunção:

-   Remova todos os valores de atributo **mayHave** de uma classe defunta.
-   Reduza o tamanho de todos os valores de atributo **mustHave** de uma classe defunta.
-   Remova um atributo defunção do catálogo global.
-   Remova um atributo defunção de qualquer índice.

Outras opções para remover alterações de esquema indesejadas em um ambiente de produção são para os desenvolvedores usarem um controlador de domínio privado para teste. Nesse caso, você pode:

-   "Redefinir" o servidor do Active Directory usando Dcpromo.exe para rebaixar o DC. Após a conclusão do rebaixamento, use Dcpromo.exe novamente para promover o servidor de volta para um DC. Em seguida, o desenvolvedor pode usar scripts LDIF para recarregar quaisquer classes, atributos e instâncias de objeto necessárias.
-   Use Ntbackup.exe para executar um backup de estado do sistema para uma partição de disco disponível. Reinicialize para Cofre/Modo de Restauração do Serviço de Diretório a ser restaurado.

Para sistemas operacionais do Windows Server 2003, ao definir uma classe ou atributo como defunção, você pode reutilizar imediatamente os valores **ldapDisplayName**, **schemaIdGuid,** **OID** e **mapiID** do elemento de esquema defunção ao criar uma nova classe ou atributo para substituí-lo. A versão defunta da classe ou atributo é mantida no contêiner Esquema, mas está oculta no snap-in do MMC. Para reativar o elemento de esquema antigo, delimite **isDefunct** como **FALSE.**

O exemplo de código LDIF a seguir mostra como modificar o atributo **isDefunct** e alterar o RDN para que ele não seja confundido com a nova classe que você cria para substituí-lo.

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

Use o comando a seguir para executar o exemplo de código LDIF em uma floresta para um computador em execução em sistemas operacionais Windows Server 2003.

**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**

(Em que "DC=X" é uma constante)

 

 




