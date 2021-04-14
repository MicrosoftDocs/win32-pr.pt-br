---
description: Aplicativos isolados são aplicativos autodescritivos instalados com manifestos. Os aplicativos isolados podem usar assemblies privados e compartilhados.
ms.assetid: 66c65b92-7c49-4932-b8c5-91b20fb0a038
title: Aplicativos isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10c1b3f175ec05751bfc84e3826b19c9c9db01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461038"
---
# <a name="isolated-applications"></a>Aplicativos isolados

Aplicativos isolados são aplicativos autodescritivos instalados com [manifestos](manifests.md). Os aplicativos isolados podem usar [assemblies privados](/windows/desktop/Msi/private-assemblies) e [compartilhados](/windows/desktop/Msi/shared-assemblies).

Um aplicativo será considerado totalmente isolado se todos os seus componentes forem compartilhados [lado a lado](about-side-by-side-assemblies-.md) ou assemblies privados. Ele será chamado parcialmente isolado se usar alguns componentes que não são assemblies lado a lado. Observe que, se um aplicativo usar alguns componentes que não são assemblies lado a lado, ou usar assemblies privados, o aplicativo poderá ser afetado pela instalação ou remoção de outros aplicativos no sistema. Para obter mais informações, consulte [compartilhamento de assembly lado a lado](side-by-side-assembly-sharing.md).

Os desenvolvedores são incentivados a projetar aplicativos isolados e atualizar aplicativos existentes em aplicativos isolados pelos seguintes motivos:

-   Os aplicativos isolados são mais estáveis e atualizados de forma confiável porque não são afetados pela instalação, remoção ou atualização de outros aplicativos no sistema.
-   Os aplicativos isolados podem ser projetados para que sejam sempre executados usando as mesmas versões de assembly com as quais foram criados e testados.
-   Os aplicativos isolados podem usar a funcionalidade fornecida pelos assemblies lado a lado disponibilizados pela Microsoft. Para obter mais informações, consulte [assemblies da Microsoft lado a lado com suporte](supported-microsoft-side-by-side-assemblies.md).
-   Os aplicativos isolados não estão vinculados à agenda de envio de seus assemblies lado a lado, pois os aplicativos e os administradores podem atualizar a configuração após a implantação sem precisar reinstalar o aplicativo. Isso não se aplicaria no caso em que apenas uma versão do assembly está sendo disponibilizada.
-   Um aplicativo totalmente isolado pode ser instalado usando o comando **xcopy** . [Windows Installer](../msi/windows-installer-portal.md) também pode ser usado para instalar um aplicativo isolado sem afetar o registro. Para obter mais informações, consulte [instalação de assemblies do Win32](../msi/installation-of-win32-assemblies.md).

Em alguns casos, os aplicativos existentes podem ser atualizados em um aplicativo isolado sem a necessidade de reescrever o código do aplicativo. Um [manifesto de aplicativo](application-manifests.md) pode ser criado para descrever as dependências do aplicativo em assemblies lado a [lado](about-side-by-side-assemblies-.md). Se o aplicativo usar componentes que não são assemblies lado a lado, eles poderão ser implantados como [assemblies privados](/windows/desktop/Msi/private-assemblies). Observe que a possibilidade de fazer isso com componentes de terceiros pode depender do licenciamento, pois o componente precisará ser criado como um assembly. Por exemplo, ao criar um manifesto do aplicativo e especificar uma dependência nos controles comuns lado a lado (COMCTL32), um aplicativo em execução no Windows XP pode *aproveitar as vantagens do Windows.* Você deve sempre testar seu aplicativo para garantir que ele seja compatível com a nova versão do assembly COMCTL32.

Talvez não seja possível atualizar todos os aplicativos existentes em um aplicativo totalmente isolado. Por exemplo, alguns assemblies do sistema de [proteção de arquivos do Windows (WFP)](/windows/desktop/Wfp/windows-resource-protection-portal) não estão disponíveis como assemblies lado a lado e não podem ser instalados com o aplicativo como um assembly privado. Pode ser possível isolar parcialmente esses aplicativos especificando dependências de assembly lado a lado para alguns dos assemblies do aplicativo em um manifesto do aplicativo.

 

 
