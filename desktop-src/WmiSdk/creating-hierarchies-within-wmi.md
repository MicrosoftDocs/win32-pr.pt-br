---
description: O namespace WMI é um objeto de programação que define o escopo de um conjunto de classes e instâncias. As classes de provedor WMI devem ser definidas dentro de um namespace.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Criando hierarquias no WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2649fb764c1710613b27e1c9bbe518dd4cb8d02215df935ddccb59c9d7e922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568776"
---
# <a name="creating-hierarchies-within-wmi"></a>Criando hierarquias no WMI

[*O namespace WMI*](gloss-n.md) é um objeto de programação que define o escopo de um conjunto de classes e instâncias. As classes de provedor WMI devem ser definidas dentro de um namespace.

Os namespaces descrevem diferentes ambientes gerenciados, como o ambiente de SMS. Como as classes e instâncias de um esquema definem os componentes de um ambiente gerenciado, cada novo esquema requer um novo namespace. Por exemplo, o namespace cimv2 raiz contém as classes e instâncias definidas no esquema Win32, bem como as classes CIM (modelo CIM pai) das quais o esquema \\ Win32 herda. As classes CIM são definidas pela[DMTF](https://www.dmtf.org/home)(Distributed Management Task Force).

> [!Note]  
> Para garantir que todas as definições de classe WMI para objetos gerenciados sejam restauradas para o repositório WMI se o [*WMI*](gloss-w.md) tiver uma falha e reiniciar, use a instrução de pré-processador de recuperação automática [**\# pragma**](pragma-autorecover.md) no arquivo [*MOF (Managed Object Format).*](gloss-m.md)

 

O WMI define um namespace como uma instância da classe do sistema [**\_ \_ namespace**](--namespace.md) ou qualquer classe derivada do **\_ \_ Namespace**. A **\_ \_ classe de sistema Namespace** tem uma única propriedade chamada **Name**, que deve ser exclusiva dentro do escopo do namespace pai. A **propriedade Name** também deve conter uma cadeia de caracteres que começa com uma letra. Todos os outros caracteres na cadeia de caracteres podem ser letras, dígitos ou sublinhados. Todos os caracteres não fazem maiúsculas de minúsculas.

Além de determinar o nome exclusivo de um namespace filho, o namespace pai do WMI pode proteger as instâncias estáticas de suas classes contra modificações acidentais por outros provedores. Por exemplo, você pode achar conveniente aninhar um novo namespace em um namespace existente para outro provedor. No entanto, o provedor original pode tentar atualizar todas as instâncias de classe para corresponder a um novo esquema. Ao fazer isso, o provedor original pode excluir todos os sub-filhos em um namespace. Embora essa possa ser uma ação apropriada para o namespace de destino, ela pode afetar instâncias de classe não relacionadas em um namespace filho (ou seja, suas próprias classes de provedor).

Portanto, geralmente é recomendável que você crie e registre seu namespace como separado dos namespaces que você não controla diretamente. Isso é especialmente verdadeiro se suas classes derivam apenas de classes CIM gerais ou de outras classes de sua empresa. Seu namespace pode estar **no** namespace Raiz, como o seguinte:

**Root/myCompany/myProduct**

Por outro lado, se a nova classe deriva da classe de outro provedor, talvez seja necessário armazenar sua classe em um sub-namespace desse provedor. Observe que isso expõe sua nova classe à exclusão acidental pelo provedor original.

O WMI fornece várias maneiras diferentes de criar um namespace:

-   [Criando um namespace filho com código MOF](creating-a-child-namespace-with-mof-code.md)
-   [Criando um namespace irmão com código MOF](creating-a-sibling-namespace-with-mof-code.md)
-   [Criando um namespace com a API WMI](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando classes Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



