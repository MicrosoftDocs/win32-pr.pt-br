---
description: Um assembly lado a lado do Windows é descrito por manifestos.
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: Sobre assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e190e6428f2e366af45a4f0961ad6ea6fb3561fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921627"
---
# <a name="about-side-by-side-assemblies"></a>Sobre assemblies lado a lado

Um assembly lado a lado do Windows é descrito por [manifestos](manifests.md). Um assembly lado a lado contém uma coleção de recursos — um grupo de DLLs, classes do Windows, servidores COM, bibliotecas de tipos ou interfaces — que são sempre fornecidos para aplicativos juntos. Eles são descritos no manifesto do assembly.

Normalmente, um assembly lado a lado é uma única DLL. Por exemplo, o assembly Microsoft COMCTL32 é uma única DLL com um manifesto, enquanto que o assembly de bibliotecas de tempo de execução do sistema de desenvolvimento Microsoft Visual C++ contém vários arquivos. Os manifestos contêm [*metadados*](m-sbscs-gly.md) que descrevem assemblies lado a lado e dependências de assembly lado a lado.

Os assemblies lado a lado são usados pelo sistema operacional como unidades fundamentais de nomenclatura, associação, controle de versão, implantação e configuração. Cada assembly lado a lado tem uma identidade exclusiva. Um dos atributos da identidade do assembly é sua versão. Para obter mais informações, consulte [versões de assembly](assembly-versions.md).

A partir do Windows XP, várias versões de assemblies lado a lado podem ser usadas por aplicativos em execução ao mesmo tempo. Os manifestos e o número de versão do assembly são usados pelo carregador para determinar a ligação correta das versões de assembly para os aplicativos. Assemblies e manifestos lado a lado funcionam com aplicativos e com o Gerenciador lado a lado, conforme ilustrado na figura a seguir.

![representação de um assembly lado a lado típico](images/sxsman.png)

No exemplo anterior, Comctl32.DLL versão 6,0 e Comctl32.DLL versão 5,0 estão no cache de assembly lado a lado e disponíveis para aplicativos. Quando um aplicativo chama para carregar a DLL, o Gerenciador lado a lado determina se o aplicativo tem uma dependência de versão descrita em um manifesto. Se não houver nenhum manifesto relevante, o sistema carregará a versão padrão do assembly. Para o Windows XP, a versão 5,0 de Comctl32.DLL é o padrão do sistema. Se o gerente lado a lado encontrar uma dependência na versão 6,0 mencionada em um manifesto, essa versão será carregada para ser executada com o aplicativo.

Vários assemblies principais do sistema estão sendo disponibilizados da Microsoft como assemblies lado a lado. Para obter mais informações, consulte [assemblies da Microsoft lado a lado com suporte](supported-microsoft-side-by-side-assemblies.md). Os desenvolvedores de aplicativos também podem criar seus próprios assemblies lado a lado. Para obter mais informações, consulte [diretrizes para criar assemblies lado a lado](guidelines-for-creating-side-by-side-assemblies.md). Em muitos casos, é possível atualizar aplicativos existentes para usar assemblies lado a lado sem precisar alterar o código do aplicativo.

Os desenvolvedores são incentivados a usar assemblies lado a lado para criar [aplicativos isolados](isolated-applications.md)e para atualizar aplicativos existentes em aplicativos isolados pelos seguintes motivos:

-   Os assemblies lado a lado reduzem a possibilidade de conflitos de versão de DLL.
-   O compartilhamento de assembly lado a lado permite que várias versões de assemblies COM ou Windows sejam executadas ao mesmo tempo.
-   Os aplicativos e administradores podem atualizar a configuração de assembly em uma base de configuração [global](publisher-configuration.md) ou [por aplicativo após a](per-application-configuration.md) implantação. Por exemplo, um aplicativo pode ser atualizado para usar um assembly lado a lado que inclui uma atualização sem precisar reinstalar o aplicativo.

 

 



