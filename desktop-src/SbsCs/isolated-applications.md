---
description: Aplicativos isolados são aplicativos autodescreviados instalados com manifestos. Aplicativos isolados podem usar assemblies privados e assemblies compartilhados.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Aplicativos isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abe13dc452c81b2a763706036e1f59400f31ccd138c95a9ab241481898aee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142119"
---
# <a name="isolated-applications"></a>Aplicativos isolados

Aplicativos isolados são aplicativos autodescreviados instalados com [manifestos](manifests.md). Aplicativos isolados podem usar [assemblies privados](/windows/desktop/Msi/private-assemblies) e [assemblies compartilhados.](/windows/desktop/Msi/shared-assemblies)

Um aplicativo será considerado totalmente isolado se todos os seus componentes são [assemblies](about-side-by-side-assemblies-.md) compartilhados lado a lado ou assemblies privados. Ele será chamado de parcialmente isolado se usar alguns componentes que não são assemblies lado a lado. Observe que, se um aplicativo usar alguns componentes que não são assemblies lado a lado ou que usam assemblies privados, o aplicativo poderá ser afetado pela instalação ou remoção de outros aplicativos no sistema. Para obter mais informações, consulte [Compartilhamento de assembly lado a lado.](side-by-side-assembly-sharing.md)

Os desenvolvedores são incentivados a criar aplicativos isolados e atualizar aplicativos existentes em aplicativos isolados pelos seguintes motivos:

-   Aplicativos isolados são mais estáveis e atualizados de forma confiável porque não são afetados pela instalação, remoção ou atualização de outros aplicativos no sistema.
-   Aplicativos isolados podem ser projetados para que sempre sejam executados usando as mesmas versões de assembly com as quais foram criados e testados.
-   Aplicativos isolados podem usar a funcionalidade fornecida pelos assemblies lado a lado disponibilizados pela Microsoft. Para obter mais informações, consulte [Assemblies lado a lado da Microsoft com suporte.](supported-microsoft-side-by-side-assemblies.md)
-   Aplicativos isolados não estão vinculados ao agendamento de envio de seus assemblies lado a lado porque os aplicativos e administradores podem atualizar a configuração após a implantação sem precisar reinstalar o aplicativo. Isso não se aplicaria no caso em que apenas uma versão do assembly está sendo disponibilizada.
-   Um aplicativo totalmente isolado pode ser instalado usando o **comando xcopy.** [Windows Instalador também](../msi/windows-installer-portal.md) pode ser usado para instalar um aplicativo isolado sem afetar o Registro. Para obter mais informações, [consulte Instalação de assemblies Win32](../msi/installation-of-win32-assemblies.md).

Em alguns casos, os aplicativos existentes podem ser atualizados em um aplicativo isolado sem a necessidade de reescrever o código do aplicativo. Um [manifesto do](application-manifests.md) aplicativo pode ser criado que descreve as dependências do aplicativo em [assemblies lado a lado.](about-side-by-side-assemblies-.md) Se o aplicativo usar componentes que não são assemblies lado a lado, eles poderão ser implantados como [assemblies privados.](/windows/desktop/Msi/private-assemblies) Observe que a possibilidade de fazer isso com componentes de terceiros pode depender do licenciamento, pois o componente precisará ser autor como um assembly. Por exemplo, criando um manifesto do aplicativo e especificando uma *dependência* dos controles comuns lado a lado (COMCTL32), um aplicativo em execução no Windows XP pode aproveitar Windows temas . Você sempre deve testar seu aplicativo para garantir que ele seja compatível com a nova versão do assembly COMCTL32.

Talvez não seja possível atualizar todos os aplicativos existentes em um aplicativo totalmente isolado. Por exemplo, alguns assemblies do sistema [WFP (Proteção](/windows/desktop/Wfp/windows-resource-protection-portal) de Arquivos Windows) não estão disponíveis como assemblies lado a lado e não podem ser instalados com o aplicativo como um assembly privado. Pode ser possível isolar parcialmente esses aplicativos especificando dependências de assembly lado a lado para alguns dos assemblies do aplicativo em um manifesto do aplicativo.

 

 
