---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647160"
---
# <a name="f-volume-shadow-copy-service"></a><span data-ttu-id="35712-103">F (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="35712-103">F (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="35712-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="35712-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="35712-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**componente de grupo de arquivos**</span><span class="sxs-lookup"><span data-stu-id="35712-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**file group component**</span></span>
</dt> <dd>

<span data-ttu-id="35712-106">Um grupo de arquivos diferentes daqueles usados como um banco de dados e definido por um gravador que precisa ser tratado como uma unidade durante as operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="35712-106">A group of files other than those used as a database and defined by a writer as needing to be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="35712-107">Consulte também [*componente*](vssgloss-c.md), [*componente de banco de dados*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="35712-107">See also [*component*](vssgloss-c.md), [*database component*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="35712-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**conjunto de arquivos**</span><span class="sxs-lookup"><span data-stu-id="35712-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**file set**</span></span>
</dt> <dd>

<span data-ttu-id="35712-109">A combinação de um caminho, uma especificação de arquivo e um sinalizador recursivo que descreve um de um arquivo ou grupo de arquivos.</span><span class="sxs-lookup"><span data-stu-id="35712-109">The combination of a path, file specification, and recursive flag describing one of a file or group of files.</span></span> <span data-ttu-id="35712-110">Por exemplo, os arquivos são adicionados aos componentes em conjuntos de arquivos.</span><span class="sxs-lookup"><span data-stu-id="35712-110">For example, files are added to components in file sets.</span></span>

<span data-ttu-id="35712-111">Salvo indicação em contrário, os caminhos de um conjunto de arquivos são caminhos padrão do Windows e podem conter variáveis de ambiente (por exemplo,% SystemRoot%) Mas não pode conter caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="35712-111">Unless otherwise indicated, a file set's paths are standard Windows paths and can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.</span></span> <span data-ttu-id="35712-112">Não há nenhum requisito de que o caminho termine com uma barra invertida (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="35712-112">There is no requirement that the path end with a backslash ("\\").</span></span> <span data-ttu-id="35712-113">Cabe a aplicativos que recuperam essas informações para verificá-lo.</span><span class="sxs-lookup"><span data-stu-id="35712-113">It is up to applications that retrieve this information to check it.</span></span>

<span data-ttu-id="35712-114">A especificação de arquivo contida em um conjunto de arquivos indica o nome do arquivo ou dos arquivos que ele inclui.</span><span class="sxs-lookup"><span data-stu-id="35712-114">The file specification contained in a file set indicates the name of the file or files it includes.</span></span> <span data-ttu-id="35712-115">Esta especificação de arquivo não pode conter especificações de diretório (por exemplo, nenhuma barra invertida), mas pode conter o?</span><span class="sxs-lookup"><span data-stu-id="35712-115">This file specification cannot contain directory specifications (for example, no backslashes) but can contain the ?</span></span> <span data-ttu-id="35712-116">e \* caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="35712-116">and \* wildcard characters.</span></span>

<span data-ttu-id="35712-117">A marca recursiva é um booliano que especifica se o caminho do conjunto de arquivos deve ser tratado como um único diretório ou se ele indica uma hierarquia de diretórios a serem atravessados recursivamente.</span><span class="sxs-lookup"><span data-stu-id="35712-117">The recursive tag is a Boolean specifying whether the file set's path should be treated as a only a single directory or if it indicates a hierarchy of directories to be traversed recursively.</span></span> <span data-ttu-id="35712-118">O booliano será **true** se o caminho for tratado como uma hierarquia de diretórios a ser atravessado recursivamente ou **false** se não.</span><span class="sxs-lookup"><span data-stu-id="35712-118">The Boolean is **true** if the path is treated as a hierarchy of directories to be traversed recursively, or **false** if not.</span></span>

<span data-ttu-id="35712-119">As informações sobre um conjunto de arquivos são retornadas por meio de instâncias da interface **IVssWMFiledesc** e podem conter informações adicionais incluem caminhos alternativos, mapeamentos de local alternativos e configurações de suporte a esquema no nível de arquivo.</span><span class="sxs-lookup"><span data-stu-id="35712-119">Information about a file set is returned through instances of the **IVssWMFiledesc** interface, and can contain additional information includes alternate paths, alternate location mappings, and file-level schema support settings.</span></span>

<span data-ttu-id="35712-120">Consulte também [*caminho alternativo*](vssgloss-a.md), [*mapeamento de local alternativo*](vssgloss-a.md), [*componente*](vssgloss-c.md), *especificação de arquivo*.</span><span class="sxs-lookup"><span data-stu-id="35712-120">See also [*alternate path*](vssgloss-a.md), [*alternate location mapping*](vssgloss-a.md), [*component*](vssgloss-c.md), *file specification*.</span></span>

</dd> <dt>

<span data-ttu-id="35712-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**especificação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="35712-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**file specification**</span></span>
</dt> <dd>

<span data-ttu-id="35712-122">Usado para corresponder arquivos em um diretório e para definir um conjunto de arquivos.</span><span class="sxs-lookup"><span data-stu-id="35712-122">Used to match files within a directory and to define a file set.</span></span> <span data-ttu-id="35712-123">Ele não pode conter especificações de diretório (por exemplo, nenhuma barra invertida), mas pode conter o?</span><span class="sxs-lookup"><span data-stu-id="35712-123">It cannot contain directory specifications (for example, no backslashes) but it can contain the ?</span></span> <span data-ttu-id="35712-124">e \* caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="35712-124">and \* wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="35712-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Serviço de replicação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="35712-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**File Replication Service**</span></span>
</dt> <dd>

<span data-ttu-id="35712-126">Usado para replicar arquivos do sistema em um diretório de volume do sistema (SysVol) redundante para dar suporte à sustentabilidade do sistema de arquivos, especialmente para sistemas de arquivos distribuídos.</span><span class="sxs-lookup"><span data-stu-id="35712-126">Used to replicate system files in a redundant system volume (SysVol) directory to support file system survivability, particularly for distributed file systems.</span></span>

</dd> <dt>

<span data-ttu-id="35712-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**Trave**</span><span class="sxs-lookup"><span data-stu-id="35712-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**freeze**</span></span>
</dt> <dd>

<span data-ttu-id="35712-128">Um período de tempo durante o processo de criação de cópia de sombra quando todos os gravadores liberaram suas gravações para os volumes e não estão iniciando gravações adicionais.</span><span class="sxs-lookup"><span data-stu-id="35712-128">A period of time during the shadow copy creation process when all writers have flushed their writes to the volumes and are not initiating additional writes.</span></span>

</dd> <dt>

<span data-ttu-id="35712-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Congelar evento**</span><span class="sxs-lookup"><span data-stu-id="35712-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Freeze event**</span></span>
</dt> <dd>

<span data-ttu-id="35712-130">Um evento do VSS que indica que um congelamento de cópia de sombra está em andamento.</span><span class="sxs-lookup"><span data-stu-id="35712-130">A VSS event indicating that a shadow copy freeze is in progress.</span></span> <span data-ttu-id="35712-131">Consulte também *congelar*, [*cópia de sombra*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="35712-131">See also *freeze*, [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="35712-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**aplicativos de nível front-end**</span><span class="sxs-lookup"><span data-stu-id="35712-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**front-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="35712-133">Indica o ponto em que um gravador é notificado de um congelamento pelo VSS.</span><span class="sxs-lookup"><span data-stu-id="35712-133">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="35712-134">Gravadores que foram inicializados como aplicativos de nível front-end são notificados antes de os gravadores serem inicializados como aplicativos de nível de back-end ou como aplicativos de nível de sistema.</span><span class="sxs-lookup"><span data-stu-id="35712-134">Writers that were initialized as front-end level applications are notified prior to writers initialized either as back-end level applications or as system-level applications.</span></span> <span data-ttu-id="35712-135">Consulte também [*nível de aplicativo*](vssgloss-a.md), [*aplicativos de nível de back-end*](vssgloss-b.md), [*aplicativos de nível de sistema*](vssgloss-s.md), [*gravador*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="35712-135">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> </dl>

 

 



