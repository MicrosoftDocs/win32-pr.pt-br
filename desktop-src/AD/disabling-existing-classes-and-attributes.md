---
title: Desabilitando classes e atributos existentes
description: Adições de esquema são permanentes.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634973"
---
# <a name="disabling-existing-classes-and-attributes"></a>Desabilitando classes e atributos existentes

Adições de esquema são permanentes. Não é possível excluir objetos **attributeSchema** e **classSchema** . Em um sistema distribuído, é difícil garantir que não haja nenhuma instância de uma determinada classe ou atributo. A remoção da definição de uma classe ou atributo danifica as instâncias existentes dessa classe ou atributo.

Você pode desabilitar uma classe ou atributo existente marcando-o como "extinto". Isso não afeta as instâncias existentes da classe ou do atributo, portanto marcado, mas impede a criação de novas instâncias.

As seguintes restrições se aplicam ao desabilitar classes e atributos de esquema:

-   Não é possível desabilitar uma classe ou atributo de categoria 1.
-   Não é possível desabilitar um atributo que seja membro de uma classe que não esteja desabilitada também. Isso ocorre porque um atributo pode ser necessário para a classe (não desabilitada) e a desabilitação do atributo impede que novas instâncias da classe sejam criadas.

Para desabilitar um atributo, defina o atributo **Isfuncde** de seu objeto **attributeSchema** como **true**. Quando um atributo é desabilitado, não é possível criar novas instâncias do atributo. Para reabilitar o atributo, defina o atributo **isextinto** como **false**.

Para desabilitar uma classe, defina o atributo **Isfuncde** de seu objeto **classSchema** como **true**. Quando uma classe é desabilitada, novas instâncias da classe não podem ser criadas. Para reabilitar a classe, defina o atributo **isextinto** como **false**.

Definir objetos de esquema como extintos pode ser útil em ambientes de produção. Quando uma versão de teste de uma extensão de esquema não for mais necessária, marque-a como expirada. Você pode restaurá-lo removendo o atributo **Isfunct** ou definindo o valor do atributo como **false**. Isso também protege contra uma remoção não intencional de um objeto de esquema definindo-o como extinto porque a operação pode ser facilmente revertida.

Lembre-se de que o servidor de Active Directory não limpa as instâncias existentes de um atributo ou classe quando você torna um objeto de esquema extinto. Se você remover a propriedade **Isfuncde** , todas as instâncias se tornarão objetos normais válidos novamente.

A lista a seguir inclui outras consequências de marcar um objeto **attributeSchema** ou **classSchema** extinto:

-   Falha na adição ou modificação de uma instância.
-   Os códigos de erro se comportam como se uma classe expirada nunca existia.
-   A pesquisa e a exclusão se comportam como se nenhum objeto de esquema fosse desativado.
-   Permitir excluir apenas o atributo inteiro do objeto.

A lista a seguir inclui opções adicionais em um ambiente de produção para reduzir o impacto das extensões de esquema expiradas:

-   Remova todos os valores de atributo **mayHave** de uma classe expirada.
-   Reduza o tamanho de todos os valores de atributo **mustHave** de uma classe expirada.
-   Remova um atributo extinto do catálogo global.
-   Remova um atributo extinto de qualquer índice.

Outras opções para remover alterações de esquema indesejadas em um ambiente de produção são para os desenvolvedores usarem um controlador de domínio privado para teste. Nesse caso, você pode:

-   "Redefinir" o servidor de Active Directory usando Dcpromo.exe para rebaixar o controlador de domínio. Depois que o rebaixamento for concluído, use Dcpromo.exe novamente para promover o servidor de volta para um controlador de domínio. O desenvolvedor pode, então, usar scripts LDIF para recarregar todas as classes, atributos e instâncias de objeto necessários.
-   Use Ntbackup.exe para executar um backup de estado do sistema para uma partição de disco disponível. Reinicialize para o modo de restauração do serviço de diretório/seguro para restaurar.

Para sistemas operacionais Windows Server 2003, quando você define uma classe ou atributo como extinto, você pode reutilizar imediatamente os valores **ldapDisplayName**, **schemaIDGUID**, **OID** e **mAPIID** do elemento de esquema extinto quando você cria uma nova classe ou atributo para substituí-lo. A versão expirada da classe ou do atributo é mantida no contêiner de esquema, mas fica oculta no snap-in do MMC. Para reativar o elemento de esquema antigo, defina **isfunc** como **false**.

O exemplo de código LDIF a seguir mostra como modificar o atributo **Isfunct** e alterar o RDN para que ele não seja confundido com a nova classe que você cria para substituí-lo.

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

Use o comando a seguir para executar o exemplo de código LDIF em uma floresta para um computador que executa o em sistemas operacionais Windows Server 2003.

**LDIFDE/i/f RDN. ldf/c "DC = X" "DC = mydomain, DC = com"**

(Em que "DC = X" é uma constante)

 

 




