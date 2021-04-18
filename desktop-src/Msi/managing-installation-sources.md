---
description: Usuários e aplicativos com privilégios administrativos podem recuperar e modificar informações de rede, URL e lista de origem de mídia para aplicativos Windows Installer e patches no sistema.
ms.assetid: e8c66bad-f594-4926-b3b4-c8b245dcfa83
title: Gerenciando fontes de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fc45253af20ae5f9792ee3a5ec7dd318c80295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757389"
---
# <a name="managing-installation-sources"></a>Gerenciando fontes de instalação

Usuários e aplicativos com privilégios administrativos podem recuperar e modificar informações de rede, URL e lista de origem de mídia para aplicativos Windows Installer e patches no sistema.

**Windows Installer 2,0:** Sem suporte. Os administradores não podem ler, reordenar ou substituir entradas na lista de origem e não podem modificar ou recuperar propriedades da lista de origem. É possível gerenciar fontes de rede, mas não URLs ou fontes de mídia. Os administradores só podem gerenciar listas de origem para aplicativos ou aplicativos por máquina instalados como por usuário para o usuário atual. Isso impede que os administradores que usam versões anteriores à Windows Installer versão 3,0 gerenciem informações da lista de origem para todos os usuários no sistema.

**Windows Installer 3,0 e posterior:** Usuários e aplicativos que têm privilégios de administrador podem recuperar e modificar informações de lista de origem para aplicativos Windows Installer e patches instalados no sistema para todos os usuários. As funções de lista de origem podem ser usadas para gerenciar listas de origem e propriedades de lista de origem para fontes de rede, URL e mídia. O instalador pode reordenar as listas de origem de um processo externo.

Usuários e aplicativos que têm privilégios administrativos podem ler e modificar os seguintes tipos de informações de lista de origem:

-   Listas de origem para aplicativos e patches instalados para todos os usuários no sistema.
-   Listas de origem para fontes de patch que existem além das fontes de aplicativo.
-   Listas de origem para URL e fontes de mídia que existem além de fontes de rede.
-   Propriedades da lista de origem, como [**MEDIAPACKAGEPATH**](mediapackagepath.md), [**DiskPrompt**](diskprompt.md), **LastUsedSource**, **LastUsedType** e **PackageName**.

As funções de listas de origem podem limitar o escopo das listas de origem encontradas especificando o contexto de instalação e o contexto do usuário. Há três contextos de instalação possíveis: por usuário (não gerenciado), por computador e gerenciado por usuário. O contexto do usuário pode ser um usuário específico ou todos os usuários no sistema.

Não administradores não podem modificar a lista de origem de uma instância de um aplicativo ou patch existente no contexto de outro usuário (gerenciado ou não gerenciado). Não administradores podem modificar as listas de origem de uma instância de um aplicativo ou patch instalados nos seguintes contextos:

-   Seu próprio contexto por usuário (não gerenciado).
-   O contexto da máquina, mas somente se as políticas [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)e [AlwaysInstallElevated](alwaysinstallelevated.md) permitirem que eles procurem um aplicativo ou uma origem de patch.
-   Seu próprio contexto gerenciado por usuário, mas somente se as políticas [DisableBrowse](disablebrowse.md), [AllowLockdownBrowse](allowlockdownbrowse.md)e [AlwaysInstallElevated](alwaysinstallelevated.md) permitirem que eles procurem um aplicativo ou uma origem de patch.

Os administradores podem modificar qualquer lista de origem que um não administrador possa modificar. Além disso, os administradores e os aplicativos que têm privilégios administrativos podem modificar as listas de origem de um aplicativo ou patch instalados nos seguintes contextos:

-   Contexto por máquina.
-   Seus próprios por usuário (não gerenciados) ou seu próprio contexto gerenciado por usuário.
-   Contexto gerenciado por usuário de outro usuário.

> [!Note]  
> Usuários e aplicativos que têm privilégios administrativos não podem modificar a lista de origem de uma instância de um aplicativo ou patch instalado no contexto por usuário (não gerenciado) de outro usuário.

 

## <a name="managing-network-and-url-sources-for-products-and-patches"></a>Gerenciando fontes de rede e de URL para produtos e patches

Use a função [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para adicionar ou reordenar a lista de origem de fontes de rede e URL para um patch ou aplicativo em um contexto específico. Use o parâmetro *dwContext* para especificar o contexto de instalação. Use o parâmetro *szUserSid* para especificar o contexto do usuário.

Use a função [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) para criar uma lista de origem para um patch que ainda não foi aplicado a nenhum aplicativo no contexto especificado. Isso pode ser útil ao registrar um patch para ter privilégios elevados. Para obter mais informações sobre como registrar privilégios elevados para um patch, consulte [aplicação de patch Per-User aplicativos gerenciados](patching-per-user-managed-applications.md).

Use a função [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea) para remover uma fonte existente de um aplicativo ou patch em um contexto especificado. A remoção da fonte atual de um aplicativo ou patch força o instalador a Pesquisar a lista de origem para uma origem na próxima vez que uma fonte for necessária.

Use a função [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) para enumerar fontes na lista de origem de um patch ou aplicativo especificado.

## <a name="managing-media-sources-for-products-and-patches"></a>Gerenciando fontes de mídia para produtos e patches

Use a função [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska) para adicionar ou atualizar as informações de disco da origem de mídia de um aplicativo registrado ou patch. Cada entrada é identificada exclusivamente por uma ID de disco. Se o disco já existir, ele será atualizado com o novo rótulo de volume e com os valores de prompt de disco. Se o disco não existir, uma nova entrada de disco será criada com os novos valores.

Use a função [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska) para remover um disco registrado existente sob a origem da mídia para um aplicativo ou patch em um contexto específico.

Use a função [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) para enumerar uma lista de discos registrados na origem de mídia para um aplicativo ou patch.

## <a name="retrieval-and-modification-of-source-list-information"></a>Recuperação e modificação de informações da lista de origem

Use as funções [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) e [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) para recuperar ou modificar informações sobre a lista de origem de um aplicativo ou patch em um contexto específico. Use o parâmetro *dwContext* para especificar o contexto de instalação. Use o parâmetro *szUserSid* para especificar o contexto do usuário.

As propriedades da lista de origem, como [**MEDIAPACKAGEPATH**](mediapackagepath.md), [**DiskPrompt**](diskprompt.md), **LastUsedSource**, **LastUsedType** e **PackageName** , podem ser acessadas.

> [!Note]  
> A propriedade da lista de origem **LastUsedType** só pode ser lida. Ele não pode ser definido diretamente usando a função [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa) .

 

## <a name="clearing-the-complete-source-list-or-forcing-a-source-resolution"></a>Limpando a lista de origem completa ou forçando uma resolução de origem

Use a função [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa) para remover todas as fontes existentes de um determinado tipo de origem para o aplicativo ou a instância de patch especificada. O registro do patch também será removido se o patch não for instalado por nenhum aplicativo no mesmo contexto. Use o parâmetro *dwContext* para especificar o contexto de instalação. Use o parâmetro *szUserSid* para especificar o contexto do usuário.

Use o [**MsiSourceListForceResolutionEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutionexa) para limpar a última entrada de origem usada para um aplicativo ou patch no contexto especificado. Essa função remove o registro da propriedade chamada **LastUsedSource**. Essa função não afeta a lista de origem registrada. Limpar o registro **LastUsedSource** força o instalador a realizar uma resolução de origem em relação às fontes registradas na próxima vez que precisar da origem.

 

 



