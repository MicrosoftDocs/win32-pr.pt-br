---
description: Os aplicativos isolados e os assemblies lado a lado fornecem uma solução que reduz conflitos de controle de versão de DLL. Eles permitem que os aplicativos compartilhem assemblies com segurança. Para obter mais informações, consulte assemblies compartilhados.
ms.assetid: 0fb0d9c2-9f6d-4fcd-a6c6-9ba8fe9f5fb5
title: Sobre aplicativos isolados e assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9099ca2e41d61c84e2952661b33ca008651f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091601"
---
# <a name="about-isolated-applications-and-side-by-side-assemblies"></a>Sobre aplicativos isolados e assemblies lado a lado

[Os aplicativos isolados e os](isolated-applications.md) assemblies lado a lado fornecem uma solução que reduz [*conflitos de controle*](d-sbscs-gly.md) [de](about-side-by-side-assemblies-.md) versão de dll. Eles permitem que os aplicativos compartilhem assemblies com segurança. Para obter mais informações, consulte [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies).

Um assembly é uma unidade fundamental para nomeação, vinculação, controle de versão, implantação ou configuração de um bloco de código de programação. Aplicativos com funcionalidade comum podem executar blocos compartilhados de código de programação que são chamados de módulos ou assemblies de código. Esses assemblies de código podem ser colocados em DLLs ou assemblies COM. A infraestrutura para o compartilhamento seguro de assemblies é conhecida como compartilhamento de assembly lado a lado.

[Assemblies lado a lado](about-side-by-side-assemblies-.md) são assemblies de código descritos por [manifestos](manifests.md) e criados para que várias versões possam ser executadas ao mesmo tempo sem entrar em conflito entre si. Quando os desenvolvedores criam manifestos e escrevem aplicativos para usar o [compartilhamento de assembly lado a lado](side-by-side-assembly-sharing.md), várias versões de assembly podem ser executadas no sistema e cada aplicativo pode especificar qual versão de assembly deve ser usada.

Um [*assembly lado a lado*](s-sbscs-gly.md) típico é uma única DLL com um único manifesto. Os assemblies lado a lado armazenam as informações sobre associação e ativação COM, tradicionalmente salvas no registro, em manifestos. Em alguns casos, as versões do assembly especificado em manifestos podem ser alteradas, em uma base global ou por aplicativo, por editores de assembly, desenvolvedores de aplicativos ou administradores. Para obter mais informações, consulte [configuração padrão](default-configuration.md), [configuração do editor](publisher-configuration.md)e [configuração por aplicativo](per-application-configuration.md).

Os desenvolvedores podem usar os assemblies lado a lado fornecidos pela Microsoft ou outros publicadores de assembly lado a lado, em seus aplicativos. Por exemplo, os desenvolvedores podem obter a funcionalidade dos controles comuns atualizados, como eles, criando seus aplicativos para usar o assembly lado a lado que contém Comctl32.dll 6,0. Para obter a lista de assemblies e manifestos lado a lado que acompanham o Windows XP, consulte [assemblies lado a lado da Microsoft com suporte](supported-microsoft-side-by-side-assemblies.md). Os desenvolvedores também podem criar seus próprios assemblies lado a lado. Para obter mais informações, consulte [diretrizes para criar assemblies lado a lado](guidelines-for-creating-side-by-side-assemblies.md).

 

 
