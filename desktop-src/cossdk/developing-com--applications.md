---
description: Ao desenvolver aplicativos COM+, as principais tarefas incluem a criação de componentes COM para encapsular a lógica do aplicativo e integrar esses componentes em um aplicativo COM+, criar o aplicativo COM+ e administrar o aplicativo por meio de implantação e manutenção.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Desenvolvendo aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54526cc0fd900dbf92f8a69986b9aafc8e41a59f3964eafa2317b196ffbf6f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047475"
---
# <a name="developing-com-applications"></a>Desenvolvendo aplicativos COM+

Ao desenvolver aplicativos COM+, as principais tarefas incluem a criação de componentes COM para encapsular a lógica do aplicativo e integrar esses componentes em um aplicativo COM+, criar o aplicativo COM+ e administrar o aplicativo por meio de implantação e manutenção.

## <a name="designing-com-components"></a>Criando componentes COM

As etapas a seguir descrevem um procedimento geral para um bom design de componente:

1.  Defina as classes COM e as classes de implementação.
2.  Agrupe as classes em componentes.
3.  Selecione o conjunto de serviços COM+ para seu componente, mesmo se você não especificar todos eles ao desenvolver o componente. Esses serviços podem ser mais tarde especificados usando a ferramenta administrativa serviços de componentes ou o modelo de objeto de administração COM+ (consulte [automatizando a administração do com+](automating-com--administration.md) para obter mais informações sobre o modelo de objeto de administração com+).

## <a name="creating-the-com-application"></a>Criando o aplicativo COM+

Depois de criar os componentes COM, o desenvolvedor integra os componentes em um aplicativo COM+ e configura o aplicativo. As etapas a seguir descrevem o processo:

1.  Integre os componentes em um aplicativo COM+. Você pode integrar os componentes em um aplicativo existente do COM+ ou criar um novo aplicativo (vazio) para os componentes. (Consulte [criando aplicativos com+](creating-com--applications.md).)
2.  Especifique o conjunto correto de atributos para cada uma das classes (se houver, e se não for especificado na ferramenta de desenvolvimento). Esses atributos expressam as dependências dos componentes em qualquer serviço COM+ em que sua implementação possa depender (por exemplo, transações, componentes enfileirados, segurança, pool de objetos e ativação Just-in-time).
3.  Configure a estrutura de segurança (funções e atribuição de funções para classes, interfaces e métodos).
4.  Configure atributos específicos do ambiente em classes e aplicativos (o tamanho padrão do pool de objetos, por exemplo). Esses atributos específicos do ambiente podem ser posteriormente definidos (ou modificados) pelo administrador do sistema.
5.  Exporte o aplicativo para redistribuição e implantação.

Para obter informações mais detalhadas sobre as etapas de criação de aplicativos distribuídos, consulte [projetando aplicativos com+](designing-com--applications.md).

## <a name="administering-com-applications"></a>Administrando aplicativos COM+

Normalmente, um desenvolvedor fornece um aplicativo COM+ parcialmente configurado para o administrador do sistema. O administrador pode personalizar o aplicativo para um ou mais ambientes específicos (por exemplo, adicionando contas de usuário em funções e nomes de servidor em um cluster de aplicativo). As tarefas do administrador incluem o seguinte:

-   Instalar o aplicativo COM+ parcialmente configurado em um computador administrativo.
-   Fornecendo atributos específicos do ambiente, como membros da função e o tamanho do pool de objetos.
-   Exportando novamente o aplicativo COM+ totalmente configurado.
-   Criar um proxy de aplicativo (se o aplicativo for ser acessado remotamente).

Depois que um aplicativo é totalmente configurado para um ambiente específico, o administrador pode implantá-lo em computadores de teste ou produção. Isso envolve a instalação do aplicativo COM+ totalmente configurado em um ou mais computadores.

Para obter informações detalhadas sobre os procedimentos de administração do COM+, consulte a ferramenta administrativa serviços de componentes.

 

 



