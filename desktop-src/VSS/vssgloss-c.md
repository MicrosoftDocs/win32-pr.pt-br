---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647163"
---
# <a name="c-volume-shadow-copy-service"></a><span data-ttu-id="676c2-103">C (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="676c2-103">C (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="676c2-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="676c2-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="676c2-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**autoridade de certificação**</span><span class="sxs-lookup"><span data-stu-id="676c2-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="676c2-106">Uma entidade confiável para emitir certificados que declaram que o indivíduo, a máquina ou a organização do destinatário solicitando o certificado atende às condições de uma política estabelecida.</span><span class="sxs-lookup"><span data-stu-id="676c2-106">An entity entrusted to issue certificates asserting that the recipient individual, machine, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="676c2-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**cópia de sombra acessível pelo cliente**</span><span class="sxs-lookup"><span data-stu-id="676c2-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**client-accessible shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="676c2-108">Uma cópia de sombra criada pelo provedor do sistema para dar suporte a Cópias de Sombra para Pastas Compartilhadas e outros mecanismos de reversão, que permitem aos clientes ver versões antigas de arquivos e desfazer erros sem a necessidade de uma restauração completa.</span><span class="sxs-lookup"><span data-stu-id="676c2-108">A shadow copy created by the system provider to support Shadow Copies for Shared Folders and other rollback mechanisms, which allow clients to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="676c2-109">Uma cópia de sombra acessível pelo cliente é criada usando o valor **\_ acessível do \_ cliente \_ VSS CTX** da enumeração de [**\_ \_ \_ contexto de instantâneo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) .</span><span class="sxs-lookup"><span data-stu-id="676c2-109">A client-accessible shadow copy is created using the **VSS\_CTX\_CLIENT\_ACCESSIBLE** value of the [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) enumeration.</span></span> <span data-ttu-id="676c2-110">Além disso, o \_ \_ valor acessível do cliente de attr do VSS VOLSNAP \_ \_ da enumeração de [**\_ \_ atributos de \_ instantâneo \_ de volume do VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) é definido automaticamente para cópias de sombra acessíveis pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="676c2-110">In addition, the VSS\_VOLSNAP\_ATTR\_CLIENT\_ACCESSIBLE value of the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration is set automatically for client-accessible shadow copies.</span></span> <span data-ttu-id="676c2-111">Consulte também [*cópias de sombra para pastas compartilhadas*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="676c2-111">See also [*Shadow Copies for Shared Folders*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="676c2-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**componente**</span><span class="sxs-lookup"><span data-stu-id="676c2-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="676c2-113">Um grupo de arquivos, definido por um gravador, que deve ser tratado como uma unidade durante as operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="676c2-113">A group of files, defined by a writer, that must be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="676c2-114">Consulte também [*componente de banco de dados*](vssgloss-d.md), [*componente de grupo de arquivos*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="676c2-114">See also [*database component*](vssgloss-d.md), [*file group component*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="676c2-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dependência de componente**</span><span class="sxs-lookup"><span data-stu-id="676c2-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**component dependency**</span></span>
</dt> <dd>

<span data-ttu-id="676c2-116">Uma situação na qual um componente (e o conjunto de componentes definido por ele) gerenciado por um gravador não pode ser submetido a backup ou restauração independentemente de componentes gerenciados por outros gravadores.</span><span class="sxs-lookup"><span data-stu-id="676c2-116">A situation in which a component (and the component set it defines) managed by one writer cannot be backed up or restore independently of components managed by others writers.</span></span> <span data-ttu-id="676c2-117">Uma dependência não indica uma ordem de preferência entre o componente com as dependências documentadas e os componentes dos quais ela depende: uma dependência indica apenas que o componente e os componentes dos quais depende devem ser sempre submetidos a backup ou restaurados juntos.</span><span class="sxs-lookup"><span data-stu-id="676c2-117">A dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on: a dependency merely indicates that the component and the components it depends on must always be backed up or restored together.</span></span>

</dd> <dt>

<span data-ttu-id="676c2-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modo de componente**</span><span class="sxs-lookup"><span data-stu-id="676c2-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**component mode**</span></span>
</dt> <dd>

<span data-ttu-id="676c2-119">Um modo no qual uma operação de backup ou restauração usa as informações de componente do gravador.</span><span class="sxs-lookup"><span data-stu-id="676c2-119">A mode in which a backup or restore operation makes use of a writer's component information.</span></span> <span data-ttu-id="676c2-120">Consulte também [*componente selecionável*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="676c2-120">See also [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="676c2-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**conjunto de componentes**</span><span class="sxs-lookup"><span data-stu-id="676c2-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**component set**</span></span>
</dt> <dd>

<span data-ttu-id="676c2-122">Um grupo de componentes com pelo menos um componente selecionável (para backup ou restauração) e vários componentes não selecionáveis organizados em uma hierarquia por seus caminhos lógicos.</span><span class="sxs-lookup"><span data-stu-id="676c2-122">A group of components with at least one selectable (for either backup or restore) component and a number of nonselectable components organized in a hierarchy by their logical paths.</span></span> <span data-ttu-id="676c2-123">A participação implícita em uma operação de backup ou restauração depende da inclusão explícita do componente selecionável de nível superior.</span><span class="sxs-lookup"><span data-stu-id="676c2-123">The implicit participation in a backup or restore operation depends on the explicit inclusion of the top-level selectable component.</span></span> <span data-ttu-id="676c2-124">Somente as informações de componente desse componente selecionável estão incluídas no documento componentes de backup.</span><span class="sxs-lookup"><span data-stu-id="676c2-124">Only the component information of this selectable component is included in the Backup Components Document.</span></span> <span data-ttu-id="676c2-125">Um conjunto de componentes pode incluir subcomponentes selecionáveis e não selecionáveis.</span><span class="sxs-lookup"><span data-stu-id="676c2-125">A component set may include selectable and nonselectable subcomponents.</span></span> <span data-ttu-id="676c2-126">Consulte também [*caminho lógico*](vssgloss-l.md), [*componente selecionável*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="676c2-126">See also [*logical path*](vssgloss-l.md), [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="676c2-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**cópia de sombra de cópia em gravação**</span><span class="sxs-lookup"><span data-stu-id="676c2-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copy-on-write shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="676c2-128">Uma cópia de sombra criada salvando apenas as diferenças do volume original.</span><span class="sxs-lookup"><span data-stu-id="676c2-128">A shadow copy created by saving only the differences from the original volume.</span></span>

</dd> <dt>

<span data-ttu-id="676c2-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**estado consistente de falha**</span><span class="sxs-lookup"><span data-stu-id="676c2-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**crash consistent state**</span></span>
</dt> <dd>

<span data-ttu-id="676c2-130">O estado dos discos é equivalente ao que seria encontrado após uma falha catastrófica que desliga abruptamente o sistema.</span><span class="sxs-lookup"><span data-stu-id="676c2-130">The state of disks equivalent to what would be found following a catastrophic failure that abruptly shuts down the system.</span></span> <span data-ttu-id="676c2-131">Uma restauração desse conjunto de cópia de sombra seria equivalente a uma reinicialização após um desligamento abrupta.</span><span class="sxs-lookup"><span data-stu-id="676c2-131">A restore from such a shadow copy set would be equivalent to a reboot following an abrupt shutdown.</span></span> <span data-ttu-id="676c2-132">Esse é o estado padrão dos dados que foram copiados em sombra sem o suporte de gravadores.</span><span class="sxs-lookup"><span data-stu-id="676c2-132">This is the default state of data that has been shadow copied without the support of writers.</span></span>

</dd> </dl>

 

 



