---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794549"
---
# <a name="a-volume-shadow-copy-service"></a><span data-ttu-id="bef0d-103">A (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="bef0d-103">A (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="bef0d-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="bef0d-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bef0d-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Anular evento**</span><span class="sxs-lookup"><span data-stu-id="bef0d-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abort event**</span></span>
</dt> <dd>

<span data-ttu-id="bef0d-106">Um evento VSS emitido pelo Serviço de Cópias de Sombra de Volume indicando que uma operação de backup ou restauração em conformidade foi anulada.</span><span class="sxs-lookup"><span data-stu-id="bef0d-106">A VSS event issued by the Volume Shadow Copy Service indicating that a compliant backup or restore operation has been aborted.</span></span> <span data-ttu-id="bef0d-107">O manipulador de eventos é **CVssWriter:: OnAbort**.</span><span class="sxs-lookup"><span data-stu-id="bef0d-107">The event handler is **CVssWriter::OnAbort**.</span></span>

</dd> <dt>

<span data-ttu-id="bef0d-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="bef0d-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span></span>
</dt> <dd>

<span data-ttu-id="bef0d-109">O serviço de Active Directory (ADSI) é um serviço baseado em COM que fornece um mecanismo para localizar, identificar e acessar os usuários e os recursos disponíveis em um sistema de ambiente de computação distribuído.</span><span class="sxs-lookup"><span data-stu-id="bef0d-109">Active Directory Service (ADSI) is a COM-based service providing a mechanism for locating, identifying, and accessing the users and resources available in a distributed computing environment system.</span></span> <span data-ttu-id="bef0d-110">Em particular, o serviço Active Directory é usado para gerenciar informações de diretório da empresa para distribuição por um servidor de domínio do Windows.</span><span class="sxs-lookup"><span data-stu-id="bef0d-110">In particular, the Active Directory service is used to manage enterprise directory information for distribution by a Windows domain server.</span></span>

</dd> <dt>

<span data-ttu-id="bef0d-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**mapeamento de local alternativo**</span><span class="sxs-lookup"><span data-stu-id="bef0d-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**alternate location mapping**</span></span>
</dt> <dd>

<span data-ttu-id="bef0d-112">Um caminho, diferente do caminho original de um arquivo, no qual o arquivo pode ser restaurado em determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="bef0d-112">A path, other than a file's original path, to which the file may be restored under certain conditions.</span></span> <span data-ttu-id="bef0d-113">Normalmente, mapeamentos de local alternativos não são definidos para um único arquivo bem definido, mas para um par de especificação de caminho/arquivo e podem ser recursivos.</span><span class="sxs-lookup"><span data-stu-id="bef0d-113">Typically, alternate location mappings are not defined for a single well-defined file, but for a path/file specification pair, and may be recursive.</span></span>

<span data-ttu-id="bef0d-114">Um mapeamento de local alternativo é usado somente durante uma operação de restauração e não deve ser confundido com um caminho alternativo, que é usado somente durante uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="bef0d-114">An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.</span></span> <span data-ttu-id="bef0d-115">Consulte também *caminho alternativo*.</span><span class="sxs-lookup"><span data-stu-id="bef0d-115">See also *alternate path*.</span></span>

</dd> <dt>

<span data-ttu-id="bef0d-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**caminho alternativo**</span><span class="sxs-lookup"><span data-stu-id="bef0d-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**alternate path**</span></span>
</dt> <dd>

<span data-ttu-id="bef0d-117">Durante as operações de backup, um par de especificação de caminho/arquivo (manipulado por uma instância da interface **IVssWMFiledesc** ) é considerado como um caminho alternativo se seu descritor de arquivo (como retornado por **IVssWMFiledesc:: GetAlternateLocation**) for não nulo.</span><span class="sxs-lookup"><span data-stu-id="bef0d-117">During backup operations, a path/file specification pair (handled by an instance of the **IVssWMFiledesc** interface) is said to have an alternate path if its file descriptor (as returned by **IVssWMFiledesc::GetAlternateLocation**) is non-NULL.</span></span> <span data-ttu-id="bef0d-118">É desse caminho, em vez do caminho especificado padrão, que os arquivos devem ser copiados quando um volume é submetido a backup.</span><span class="sxs-lookup"><span data-stu-id="bef0d-118">It is from this path, rather than the default specified path, that files are to be copied when a volume is backed up.</span></span>

<span data-ttu-id="bef0d-119">Um caminho alternativo é usado somente durante uma operação de backup e não deve ser confundido com um mapeamento de local alternativo.</span><span class="sxs-lookup"><span data-stu-id="bef0d-119">An alternate path is used only during a backup operation and should not be confused with an alternate location mapping.</span></span> <span data-ttu-id="bef0d-120">Um mapeamento de local alternativo é usado somente durante as operações de restauração.</span><span class="sxs-lookup"><span data-stu-id="bef0d-120">An alternate location mapping is used only during restore operations.</span></span> <span data-ttu-id="bef0d-121">Consulte também *mapeamento de local alternativo*.</span><span class="sxs-lookup"><span data-stu-id="bef0d-121">See also *alternate location mapping*.</span></span>

</dd> <dt>

<span data-ttu-id="bef0d-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**nível do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="bef0d-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**application level**</span></span>
</dt> <dd>

<span data-ttu-id="bef0d-123">Usado pelo VSS para indicar o ponto no curso da criação de uma cópia de sombra que um gravador é notificado de um congelamento.</span><span class="sxs-lookup"><span data-stu-id="bef0d-123">Used by VSS to indicate the point in the course of the creation of a shadow copy that a writer is notified of a freeze.</span></span> <span data-ttu-id="bef0d-124">Consulte também [*aplicativos de nível de back-end*](vssgloss-b.md), [*congelamento*](vssgloss-f.md), [*aplicativos de nível front-end*](vssgloss-f.md), [*cópia de sombra*](vssgloss-s.md), [*aplicativos de nível de sistema*](vssgloss-s.md), [*gravador*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="bef0d-124">See also [*back-end level applications*](vssgloss-b.md), [*freeze*](vssgloss-f.md), [*front-end level applications*](vssgloss-f.md), [*shadow copy*](vssgloss-s.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="bef0d-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**cópia de sombra recuperada automaticamente**</span><span class="sxs-lookup"><span data-stu-id="bef0d-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**auto-recovered shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="bef0d-126">Uma cópia de sombra que tinha processamento adicional por um gravador está em um estado completamente consistente para backup ou Data Mining ações (por exemplo, reverter todas as transações que ainda não foram concluídas no ponto em que a cópia de sombra foi criada.) Isso pode ser iniciado por um gravador, especificando um sinalizador apropriado da enumeração **de \_ \_ sinalizadores de componente do VSS** no membro **DwComponentFlags** da **estrutura \_ COMPONENTINFO do VSS** ou por um solicitante, adicionando o sinalizador de **\_ \_ \_ \_ recuperação de reversão do atributo VOLSNAP do VSS** para o contexto da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="bef0d-126">A shadow copy that has had additional processing by a writer to be in a completely consistent state for backup or data mining actions (for example, rolling back all transactions that did not yet complete at the point that the shadow copy was created.) This can be initiated by a writer by specifying an appropriate flag from the **VSS\_COMPONENT\_FLAGS** enumeration in the **dwComponentFlags** member of the **VSS\_COMPONENTINFO** structure or by a requester by adding the **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** flag to the context for the shadow copy.</span></span> <span data-ttu-id="bef0d-127">A recuperação automática permite que os dados copiados de sombra sejam usados em um volume somente leitura, por Data Mining, restaurações parciais (por exemplo, itens selecionados em um banco de dados) ou outras finalidades.</span><span class="sxs-lookup"><span data-stu-id="bef0d-127">Auto-recovery allows the shadow copied data to be used on a read-only volume, for data mining, partial restores (for example selected items in a database), or other purposes.</span></span>

<span data-ttu-id="bef0d-128">Consulte também [*cópia de sombra transportável*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="bef0d-128">See also [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="bef0d-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**cópia de sombra de lançamento automático**</span><span class="sxs-lookup"><span data-stu-id="bef0d-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**auto-release shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="bef0d-130">Uma cópia de sombra que será excluída após o encerramento de uma operação de backup.</span><span class="sxs-lookup"><span data-stu-id="bef0d-130">A shadow copy that will be deleted upon the termination of a backup operation.</span></span> <span data-ttu-id="bef0d-131">Programaticamente, isso significa que a cópia de sombra será excluída quando a interface **IVssBackupComponents** for liberada.</span><span class="sxs-lookup"><span data-stu-id="bef0d-131">Programmatically, this means the shadow copy will be deleted when the **IVssBackupComponents** interface is released.</span></span> <span data-ttu-id="bef0d-132">Uma cópia de sombra de lançamento automático não pode ser persistente.</span><span class="sxs-lookup"><span data-stu-id="bef0d-132">An auto-release shadow copy cannot be persistent.</span></span>

<span data-ttu-id="bef0d-133">Por padrão, todas as cópias de sombra são lançadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bef0d-133">By default, all shadow copies are auto-release.</span></span> <span data-ttu-id="bef0d-134">Consulte também [*cópia de sombra persistente*](vssgloss-p.md), [*cópia de sombra transportável*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="bef0d-134">See also [*persistent shadow copy*](vssgloss-p.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> </dl>

 

 



