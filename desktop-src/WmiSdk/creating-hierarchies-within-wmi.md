---
description: O namespace WMI é um objeto de programação que define o escopo de um conjunto de classes e instâncias. As classes do provedor WMI devem ser definidas dentro de um namespace.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Criando hierarquias dentro do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165337"
---
# <a name="creating-hierarchies-within-wmi"></a>Criando hierarquias dentro do WMI

O [*namespace WMI*](gloss-n.md) é um objeto de programação que define o escopo de um conjunto de classes e instâncias. As classes do provedor WMI devem ser definidas dentro de um namespace.

Os namespaces descrevem diferentes ambientes gerenciados, como o ambiente SMS. Como as classes e instâncias de um esquema definem os componentes de um ambiente gerenciado, cada novo esquema requer um novo namespace. Por exemplo, o \\ namespace raiz cimv2 contém as classes e instâncias definidas no esquema Win32, bem como as classes de modelo CIM pai (CIM) das quais o esquema Win32 herda. As classes CIM são definidas pela[DMTF](https://www.dmtf.org/home)(Distributed Management Task Force).

> [!Note]  
> Para garantir que todas as suas definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório WMI*](gloss-w.md) se o WMI tiver uma falha e for reiniciado, use a instrução de pré-processador de [**\# AutoRecuperação pragma**](pragma-autorecover.md) no seu arquivo [*formato MOF (MOF)*](gloss-m.md) .

 

O WMI define um namespace como uma instância da classe de sistema de [**\_ \_ namespace**](--namespace.md) ou qualquer classe derivada do **\_ \_ namespace**. A classe de sistema **\_ \_ namespace** tem uma única propriedade chamada **Name**, que deve ser exclusiva dentro do escopo do namespace pai. A propriedade **Name** também deve conter uma cadeia de caracteres que comece com uma letra. Todos os outros caracteres na cadeia de caracteres podem ser letras, dígitos ou sublinhados. Todos os caracteres não diferenciam maiúsculas de minúsculas.

Além de determinar o nome exclusivo para um namespace filho, o namespace pai WMI pode proteger as instâncias estáticas de suas classes contra a modificação acidental por outros provedores. Por exemplo, você pode achar conveniente aninhar um novo namespace em um namespace existente para outro provedor. No entanto, o provedor original pode tentar atualizar todas as instâncias de classe para que correspondam a um novo esquema. Ao fazer isso, o provedor original pode excluir todos os subfilhos em um namespace. Embora isso possa ser uma ação apropriada para o namespace de destino, ele pode afetar instâncias de classe não relacionadas em um namespace filho (ou seja, suas próprias classes de provedor).

Portanto, geralmente é recomendável que você crie e Registre seu namespace como separado dos namespaces que você não controla diretamente. Isso é especialmente verdadeiro se suas classes derivarem somente de classes CIM gerais ou de outras classes de sua empresa. O namespace pode estar no namespace **raiz** , como o seguinte:

**Raiz/myCompany/MyProduct**

Por outro lado, se a sua nova classe derivar da classe de outro provedor, talvez seja necessário armazenar sua classe em um subnamespace desse provedor. Observe que isso expõe sua nova classe à exclusão acidental pelo provedor original.

O WMI fornece várias maneiras diferentes de criar um namespace:

-   [Criando um namespace filho com código MOF](creating-a-child-namespace-with-mof-code.md)
-   [Criando um namespace irmão com código MOF](creating-a-sibling-namespace-with-mof-code.md)
-   [Criando um namespace com a API do WMI](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



