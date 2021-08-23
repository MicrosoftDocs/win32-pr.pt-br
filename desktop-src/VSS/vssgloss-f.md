---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56eef69a16a77fce7f557ae0ff02ff0e5d84d0225d082fd486af629b9804aeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056194"
---
# <a name="f-volume-shadow-copy-service"></a>F (Serviço de Cópias de Sombra de Volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**componente de grupo de arquivos**
</dt> <dd>

Um grupo de arquivos diferentes daqueles usados como um banco de dados e definido por um gravador que precisa ser tratado como uma unidade durante as operações de backup e restauração. Consulte também [*componente*](vssgloss-c.md), [*componente de banco de dados*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**conjunto de arquivos**
</dt> <dd>

A combinação de um caminho, uma especificação de arquivo e um sinalizador recursivo que descreve um de um arquivo ou grupo de arquivos. Por exemplo, os arquivos são adicionados aos componentes em conjuntos de arquivos.

salvo indicação em contrário, os caminhos de um conjunto de arquivos são caminhos de Windows padrão e podem conter variáveis de ambiente (por exemplo,% SystemRoot%), mas não podem conter caracteres curinga. Não há nenhum requisito de que o caminho termine com uma barra invertida (" \\ "). Cabe a aplicativos que recuperam essas informações para verificá-lo.

A especificação de arquivo contida em um conjunto de arquivos indica o nome do arquivo ou dos arquivos que ele inclui. Esta especificação de arquivo não pode conter especificações de diretório (por exemplo, nenhuma barra invertida), mas pode conter o? e \* caracteres curinga.

A marca recursiva é um booliano que especifica se o caminho do conjunto de arquivos deve ser tratado como um único diretório ou se ele indica uma hierarquia de diretórios a serem atravessados recursivamente. O booliano será **true** se o caminho for tratado como uma hierarquia de diretórios a ser atravessado recursivamente ou **false** se não.

As informações sobre um conjunto de arquivos são retornadas por meio de instâncias da interface **IVssWMFiledesc** e podem conter informações adicionais incluem caminhos alternativos, mapeamentos de local alternativos e configurações de suporte a esquema no nível de arquivo.

Consulte também [*caminho alternativo*](vssgloss-a.md), [*mapeamento de local alternativo*](vssgloss-a.md), [*componente*](vssgloss-c.md), *especificação de arquivo*.

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**especificação de arquivo**
</dt> <dd>

Usado para corresponder arquivos em um diretório e para definir um conjunto de arquivos. Ele não pode conter especificações de diretório (por exemplo, nenhuma barra invertida), mas pode conter o? e \* caracteres curinga.

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Serviço de replicação de arquivo**
</dt> <dd>

Usado para replicar arquivos do sistema em um diretório de volume do sistema (SysVol) redundante para dar suporte à sustentabilidade do sistema de arquivos, especialmente para sistemas de arquivos distribuídos.

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**Trave**
</dt> <dd>

Um período de tempo durante o processo de criação de cópia de sombra quando todos os gravadores liberaram suas gravações para os volumes e não estão iniciando gravações adicionais.

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Congelar evento**
</dt> <dd>

Um evento do VSS que indica que um congelamento de cópia de sombra está em andamento. Consulte também *congelar*, [*cópia de sombra*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**aplicativos de nível front-end**
</dt> <dd>

Indica o ponto em que um gravador é notificado de um congelamento pelo VSS. Gravadores que foram inicializados como aplicativos de nível front-end são notificados antes de os gravadores serem inicializados como aplicativos de nível de back-end ou como aplicativos de nível de sistema. Consulte também [*nível de aplicativo*](vssgloss-a.md), [*aplicativos de nível de back-end*](vssgloss-b.md), [*aplicativos de nível de sistema*](vssgloss-s.md), [*gravador*](vssgloss-w.md).

</dd> </dl>

 

 



