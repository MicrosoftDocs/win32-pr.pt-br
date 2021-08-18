---
description: Aplicativos isolados e assemblies lado a lado fornecem uma solução que reduz conflitos de versão de DLL. Eles permitem que os aplicativos compartilhem assemblies com segurança. Para obter mais informações, consulte Assemblies compartilhados.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Sobre aplicativos isolados e assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ab72689173d4e8942d10dfc62259091574634227c3f4d252b0d87853ec9be7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142659"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Sobre aplicativos isolados e assemblies lado a lado

[Aplicativos isolados](isolated-applications.md) [e assemblies lado](about-side-by-side-assemblies-.md) a lado fornecem uma solução que reduz conflitos de [*versão de DLL.*](d-sbscs-gly.md) Eles permitem que os aplicativos compartilhem assemblies com segurança. Para obter mais informações, consulte [Assemblies compartilhados](/windows/desktop/Msi/shared-assemblies).

Um assembly é uma unidade fundamental para nomear, vincular, controle de versão, implantar ou configurar um bloco de código de programação. Aplicativos com funcionalidade comum podem executar blocos compartilhados de código de programação que são chamados de módulos ou assemblies de código. Esses assemblies de código podem ser colocados em assemblies COM ou DLLs. A infraestrutura para o compartilhamento seguro de assemblies é conhecida como compartilhamento de assembly lado a lado.

[Assemblies lado a lado](about-side-by-side-assemblies-.md) são assemblies de código descritos por manifestos e autorados para que várias versões possam ser [executados](manifests.md) ao mesmo tempo sem conflitos entre si. Quando os desenvolvedores escrevem manifestos e escrevem aplicativos para usar o compartilhamento de [assembly](side-by-side-assembly-sharing.md)lado a lado, várias versões de assembly podem ser executados no sistema e cada aplicativo pode especificar qual versão de assembly ele deve usar.

Um assembly lado a [*lado típico é*](s-sbscs-gly.md) uma única DLL com um único manifesto. Assemblies lado a lado armazenam as informações sobre associação e ativação COM, tradicionalmente salvas no Registro, em manifestos. Em alguns casos, as versões do assembly especificado nos manifestos podem ser alteradas, global ou por aplicativo, por editores de assembly, desenvolvedores de aplicativos ou administradores. Para obter mais informações, consulte [configuração padrão,](default-configuration.md)configuração [do](publisher-configuration.md)publicador e [configuração por aplicativo.](per-application-configuration.md)

Os desenvolvedores podem usar os assemblies lado a lado fornecidos pela Microsoft ou outros editores de assembly lado a lado em seus aplicativos. Por exemplo, os desenvolvedores podem obter a funcionalidade dos controles comuns atualizados, como temas, projetando seus aplicativos para usar o assembly lado a lado que contém Comctl32.dll 6.0. Para ver a lista de assemblies e manifestos lado a lado que acompanham o Windows XP, consulte Assemblies lado a lado da [Microsoft com suporte.](supported-microsoft-side-by-side-assemblies.md) Os desenvolvedores também podem criar seus próprios assemblies lado a lado. Para obter mais informações, [consulte Diretrizes para criar assemblies](guidelines-for-creating-side-by-side-assemblies.md)lado a lado.

 

 
