---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501727"
---
# <a name="w-volume-shadow-copy-service"></a><span data-ttu-id="f3c62-103">W (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="f3c62-103">W (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="f3c62-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="f3c62-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f3c62-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Proteção de arquivo do Windows**</span><span class="sxs-lookup"><span data-stu-id="f3c62-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="f3c62-106">Um serviço do sistema que protege arquivos especiais do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f3c62-106">A system service that protects special operating system files.</span></span> <span data-ttu-id="f3c62-107">Se um desses arquivos for excluído ou substituído, a proteção de arquivo do Windows substituirá o arquivo pelo original do cache.</span><span class="sxs-lookup"><span data-stu-id="f3c62-107">If one of these files is deleted or overwritten, Windows File Protection replaces the file with the original from its cache.</span></span>

</dd> <dt>

<span data-ttu-id="f3c62-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**escritor**</span><span class="sxs-lookup"><span data-stu-id="f3c62-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**writer**</span></span>
</dt> <dd>

<span data-ttu-id="f3c62-109">Um aplicativo que coordena suas operações de e/s com operações relacionadas à cópia de sombra e cópia de sombra do VSS (como backups e restaurações) para que os dados contidos no volume copiado de sombra estejam em um estado consistente.</span><span class="sxs-lookup"><span data-stu-id="f3c62-109">An application that coordinates its I/O operations with VSS shadow copy and shadow copy related operations (such as backups and restores) so that their data contained on the shadow copied volume is in a consistent state.</span></span>

<span data-ttu-id="f3c62-110">Para dar suporte a essa coordenação, um gravador deve implementar uma instância de uma classe derivada da classe base abstrata **CVssWriter** para se comunicar com a infraestrutura do VSS.</span><span class="sxs-lookup"><span data-stu-id="f3c62-110">To support this coordination, a writer must implement an instance of a class derived from the abstract base class **CVssWriter** to communicate with the VSS infrastructure.</span></span> <span data-ttu-id="f3c62-111">Consulte também [*cópia de sombra*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="f3c62-111">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3c62-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**classe de gravador**</span><span class="sxs-lookup"><span data-stu-id="f3c62-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**writer class**</span></span>
</dt> <dd>

<span data-ttu-id="f3c62-113">Um GUID (identificador global exclusivo) fornecido por um gravador durante a inicialização para indicar que ele pertence a um determinado tipo de gravadores.</span><span class="sxs-lookup"><span data-stu-id="f3c62-113">A globally unique identifier (GUID) supplied by a writer during initialization to indicate that it belongs to a given type of writers.</span></span> <span data-ttu-id="f3c62-114">Por exemplo, várias implementações de um gravador podem compartilhar a mesma ID de classe do gravador.</span><span class="sxs-lookup"><span data-stu-id="f3c62-114">For instance, multiple implementations of a writer could share the same writer class ID.</span></span>

<span data-ttu-id="f3c62-115">Os gravadores da mesma classe podem ser diferenciados por suas instâncias do gravador.</span><span class="sxs-lookup"><span data-stu-id="f3c62-115">Writers of the same class may be distinguished by their writer instances.</span></span> <span data-ttu-id="f3c62-116">Cabe a um desenvolvedor de aplicativos especificar classes de gravador.</span><span class="sxs-lookup"><span data-stu-id="f3c62-116">It is up to an application developer to specify writer classes.</span></span> <span data-ttu-id="f3c62-117">Consulte também *instância do gravador*.</span><span class="sxs-lookup"><span data-stu-id="f3c62-117">See also *writer instance*.</span></span>

</dd> <dt>

<span data-ttu-id="f3c62-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**instância do gravador**</span><span class="sxs-lookup"><span data-stu-id="f3c62-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**writer instance**</span></span>
</dt> <dd>

<span data-ttu-id="f3c62-119">Um GUID (identificador global exclusivo) fornecido pelo VSS para cada processo do gravador em execução em um sistema.</span><span class="sxs-lookup"><span data-stu-id="f3c62-119">A globally unique identifier (GUID) supplied by VSS for each writer process running on a system.</span></span> <span data-ttu-id="f3c62-120">Um valor exclusivo para a instância do gravador é gerado cada vez que o gravador é iniciado.</span><span class="sxs-lookup"><span data-stu-id="f3c62-120">A unique value for the writer instance is generated each time the writer starts.</span></span>

</dd> <dt>

<span data-ttu-id="f3c62-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Documento de metadados do gravador**</span><span class="sxs-lookup"><span data-stu-id="f3c62-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer Metadata Document**</span></span>
</dt> <dd>

<span data-ttu-id="f3c62-122">Um documento XML criado por um gravador (usando a interface **IVssCreateWriterMetadata** ) que contém informações sobre o estado e os componentes do gravador.</span><span class="sxs-lookup"><span data-stu-id="f3c62-122">An XML document created by a writer (using the **IVssCreateWriterMetadata** interface) containing information about the writer's state and components.</span></span> <span data-ttu-id="f3c62-123">Um solicitante pode consultar documentos de metadados do gravador (usando a interface **IVssExamineWriterMetadata** ) ao executar uma operação de restauração ou backup.</span><span class="sxs-lookup"><span data-stu-id="f3c62-123">A requester can query Writer Metadata Documents (using the **IVssExamineWriterMetadata** interface) when performing a restore or backup operation.</span></span>

<span data-ttu-id="f3c62-124">Um documento de metadados do gravador contém a lista de todos os componentes de um gravador, qualquer um dos quais pode participar de um backup.</span><span class="sxs-lookup"><span data-stu-id="f3c62-124">A Writer Metadata Document contains the list of all of a writer's components, any one of which might participate in a backup.</span></span> <span data-ttu-id="f3c62-125">Isso é diferente do documento de componentes de backup do solicitante, que contém apenas os componentes explicitamente incluídos para uma operação de backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="f3c62-125">This differs from the requester's Backup Components Document, which contains only those components explicitly included for a backup or restore operation.</span></span>

<span data-ttu-id="f3c62-126">Depois de construído, o documento de metadados do gravador deve ser exibido como um objeto somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f3c62-126">Once constructed, the Writer Metadata Document should be viewed as a read-only object.</span></span> <span data-ttu-id="f3c62-127">Ele pode ser salvo em disco.</span><span class="sxs-lookup"><span data-stu-id="f3c62-127">It can be saved to disk.</span></span> <span data-ttu-id="f3c62-128">Consulte também [*documento de componentes de backup*](vssgloss-b.md), [*inclusão explícita de componentes*](vssgloss-e.md), inclusão de [*componentes implícitos*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="f3c62-128">See also [*Backup Components Document*](vssgloss-b.md), [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> </dl>

 

 



