---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781076"
---
# <a name="s-volume-shadow-copy-service"></a>S (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**seleção de backup**
</dt> <dd>

Um componente é considerado selecionável para backup se sua inclusão explícita em uma operação de backup for opcional. A seleção de backup será habilitada se o valor do membro **bSelectable** da estrutura [**\_ COMPONENTINFO do VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) for **true**. Não há valor padrão para a seleção de um componente para backup; um gravador sempre deve definir esse valor explicitamente.

Os gravadores também usam a seleção para restauração para organizar a participação do componente nas operações de restauração.

Consulte também *componente selecionável*, *seleção para restauração*, [*inclusão explícita de componentes*](vssgloss-e.md), [*inclusão de componente implícita*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**seleção de restauração**
</dt> <dd>

Um componente é considerado selecionável para restauração se puder ser feito o backup implicitamente como parte de um conjunto de componentes e, posteriormente, restaurado individualmente sem o restante do conjunto de componentes. A seleção de restauração será habilitada se o valor do membro **bSelectableForRestore** da estrutura [**\_ COMPONENTINFO do VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) for **true**. Por padrão, a seleção de um componente para restauração é **falsa**. A seleção de restauração tem significado apenas quando um componente não foi adicionado ao documento de backup.

Consulte também *componente selecionável*, *seleção para backup*, [*inclusão de componente explícita*](vssgloss-e.md), [*inclusão de componente implícita*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente selecionável**
</dt> <dd>

Um componente é considerado selecionável se sua inclusão explícita em uma operação de backup ou restauração for opcional.

A seleção de backup e a seleção de restauração são independentes umas das outras — um componente pode ser selecionável para ambas as operações, para restauração e não para backup, ou para backup e não restauração.

Os gravadores também usam a seleção para organizar seus componentes em grupos:

-   Componentes não selecionáveis sem ancestrais selecionáveis em seus caminhos lógicos devem sempre ser incluídos explicitamente se for necessário fazer backup ou restauração de um gravador.
-   Os componentes não selecionáveis com ancestrais selecionáveis só serão incluídos em um backup ou restauração se pelo menos um ancestral selecionável estiver incluído.
-   Componentes selecionáveis sem ancestrais selecionáveis só podem ser incluídos em uma operação de backup ou restauração explicitamente.
-   Componentes selecionáveis com ancestrais selecionáveis podem ser incluídos explicitamente em uma operação de backup ou restauração, ou podem ser incluídos implicitamente se um de seus ancestrais selecionáveis estiver incluído.

Consulte também [*componentes*](vssgloss-c.md), *a seleção de backup*, a *seleção de restauração, a* [*inclusão explícita de componentes*](vssgloss-e.md), a inclusão de [*componentes implícitos*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**cópia de sombra**
</dt> <dd>

Uma réplica de ponto no tempo somente leitura do conteúdo de um volume original. Cada cópia de sombra é codificada por um GUID persistente. Também chamada de cópia de sombra de volume. Consulte também *conjunto de cópias de sombra*.

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Cópias de Sombra para Pastas Compartilhadas**
</dt> <dd>

Um recurso do Windows que cria cópias de backup simples e online de volumes usando o VSS. Os clientes podem acessar esses backups por meio do shell do Windows para ver versões antigas de arquivos e desfazer erros sem a necessidade de uma restauração completa. Consulte também [*cópia de sombra acessível ao cliente*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**conjunto de cópias de sombra**
</dt> <dd>

Uma coleção de cópias de sombra de volume criadas ao mesmo tempo e identificada por um valor de ID de conjunto de cópias de sombra (um GUID persistente) comum. Esse é o mecanismo usado para permitir que uma operação de cópia de sombra seja gerenciada entre volumes. Consulte também *cópia de sombra*.

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**provedor de software**
</dt> <dd>

Um provedor que intercepta solicitações de e/s no nível de software entre o sistema de arquivos e o Gerenciador de volumes. Consulte também [*provedor de hardware*](vssgloss-h.md), [*provedor*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponente**
</dt> <dd>

Qualquer componente que tenha um caminho lógico contendo um componente do pai selecionável (para backup ou restauração). Os subcomponentes devem ter um caminho lógico no formato {nome do componente \_ } \\ {nome do subcomponente \_ }. Se o ancestral de um subcomponente selecionável (para backup ou restauração) for explicitamente incluído em um backup ou restauração, o subcomponente será incluído implicitamente na operação. Os subcomponentes incluídos implicitamente não têm seus dados incluídos no documento de componentes de backup, independentemente de serem selecionáveis (para restauração ou backup) ou não. Consulte também [*componente*](vssgloss-c.md), [*caminho lógico*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**cópia de sombra na superfície**
</dt> <dd>

Um volume copiado de sombra visível para o namespace do Gerenciador de montagem do sistema — significando que **FindFirstVolume** e **FindNextVolume** podem encontrá-lo e que as notificações de chegada e saída do volume são geradas. Todas as cópias de sombra expostas também são cópias de sombra em superfície. No entanto, uma cópia de sombra em superfície não precisa ser exposta. Se uma cópia de sombra for transportável, ela não poderá ser exposta. Consulte também [*cópia de sombra exposta*](vssgloss-e.md), [*cópia de sombra transportável*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Proteção de arquivo do sistema**
</dt> <dd>

Consulte [*proteção de arquivos do Windows*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**aplicativos de nível de sistema**
</dt> <dd>

Indica o ponto no qual o VSS notifica um escritor de um congelamento. Gravadores que são inicializados como aplicativos de nível de sistema são notificados depois que os gravadores são inicializados como aplicativos de nível front-end ou como aplicativos de nível back-end. Consulte também [*nível de aplicativo*](vssgloss-a.md), [*aplicativos de nível de back-end*](vssgloss-b.md), [*aplicativos de nível front-end*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**provedor do sistema**
</dt> <dd>

O provedor pré-instalado padrão fornecido como parte do Windows.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Pasta volume do sistema**
</dt> <dd>

Um diretório compartilhado que armazena as cópias compartilhadas dos arquivos públicos de um domínio, ou seja, os arquivos que são replicados entre todos os controladores de domínio no domínio.

</dd> </dl>

 

 



