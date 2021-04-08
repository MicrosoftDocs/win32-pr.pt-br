---
description: Os aplicativos que dependem de recursos de rede para instalação sob demanda são suscetíveis a falhas de origem se o local de origem deve ser alterado por qualquer motivo ou se for danificado.
ms.assetid: 3d6a0524-d5df-4d4c-b861-d4a7da95ce40
title: Resiliência de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46944804db1c4b91c6c6757303fd2af90638b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920717"
---
# <a name="source-resiliency"></a>Resiliência de origem

Os aplicativos que dependem de recursos de rede para [instalação sob demanda](installation-on-demand.md) são suscetíveis a falhas de origem se o local de origem deve ser alterado por qualquer motivo ou se for danificado. O Windows Installer fornece resiliência de origem para recursos que são instalados sob demanda usando uma lista de origem. A lista origem contém os locais pesquisados pelo instalador para pacotes de instalação. As entradas nessa lista podem ser locais de rede, URLs (Uniform Resource Locators) ou CDs. Se uma dessas origens falhar, o instalador poderá tentar a próxima de maneira rápida e direta.

O desenvolvedor do aplicativo não precisa incorporar nenhuma informação especial ao pacote do instalador para garantir a resiliência da origem. Depois que o aplicativo é instalado, o instalador tem o comportamento de adicionar a última fonte usada com êxito como uma entrada na lista de origem. Por padrão, essa origem é o local do qual o pacote do instalador está inicialmente instalado e é o mesmo que a propriedade [**SourceDir**](sourcedir.md) .

Um administrador do sistema pode alterar a lista de origem aplicando uma [transformação](merges-and-transforms.md) ou alterando a propriedade [**SourceList**](sourcelist.md) da linha de comando ou da [tabela de propriedades](property-table.md).

O instalador começa a procurar uma fonte verificando o local de origem usado mais recentemente na lista de origem. Se essa pesquisa falhar, o instalador pesquisará a lista de fontes de rede, as fontes de mídia e, por fim, fontes de URL. Os administradores do sistema podem alterar essa ordem de pesquisa usando a política do sistema [SearchOrder](searchorder.md) . Se essas pesquisas falharem, o instalador poderá apresentar uma [caixa de diálogo de procura](browse-dialog.md) para que o usuário possa procurar a origem manualmente. A caixa de diálogo procurar não poderá ser exibida se o nível da interface do usuário estiver definido como nenhum. Para obter detalhes, consulte [níveis de interface do usuário](user-interface-levels.md).

Normalmente, o instalador só deve exibir uma caixa de diálogo de procura se o usuário atual for um administrador ou se a instalação não exigir privilégios elevados. Um administrador pode controlar a exibição da caixa de diálogo Procurar para os usuários com as políticas [DisableBrowse](disablebrowse.md) e [AllowLockDownBrowse](allowlockdownbrowse.md) . Um administrador também controla se os usuários podem instalar aplicativos de fontes localizadas na mídia usando as políticas [DisableMedia](disablemedia.md) e [AllowLockDownMedia](allowlockdownmedia.md) . O uso dessas políticas depende da versão do Windows Installer. Para obter detalhes, consulte o seguinte:

-   [Política de resiliência de origem](source-resiliency-policy-windows-installer-version-2-0.md)

 

 



