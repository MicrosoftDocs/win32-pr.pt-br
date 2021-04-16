---
description: Quando uma operação de backup do VSS é realizada sem o envolvimento de um gravador, a criação da cópia de sombra ainda pode ocorrer.
ms.assetid: 2058e894-bde5-4690-a7aa-849d2e9cdc71
title: Backups sem participação no gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a782fbcb9afe532f2f123151dc7998307157b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750187"
---
# <a name="backups-without-writer-participation"></a><span data-ttu-id="2a514-103">Backups sem participação no gravador</span><span class="sxs-lookup"><span data-stu-id="2a514-103">Backups without Writer Participation</span></span>

<span data-ttu-id="2a514-104">Quando uma operação de backup do VSS é realizada sem o envolvimento de um gravador, a criação da cópia de sombra ainda pode ocorrer.</span><span class="sxs-lookup"><span data-stu-id="2a514-104">When a VSS backup operation is conducted without the involvement of a writer, the shadow copy creation can still occur.</span></span>

<span data-ttu-id="2a514-105">Conforme observado em outro lugar (consulte o [estado de cópia de sombra padrão](shadow-copies-and-shadow-copy-sets.md)), o resultado desse tipo de cópia de sombra é um volume que reflete o estado de um disco no momento da cópia de sombra: os dados no volume copiado por sombra podem refletir operações de e/s incompletas ou parciais e são descritos como estando em um [*estado consistente de falha*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="2a514-105">As noted elsewhere (see [Default Shadow Copy State](shadow-copies-and-shadow-copy-sets.md)), the result of this type of shadow copy is a volume reflecting the state of a disk at the time of the shadow copy: data on the shadow-copied volume may reflect incomplete or partial I/O operations and is described as being in a [*crash-consistent state*](vssgloss-c.md).</span></span>

<span data-ttu-id="2a514-106">Há várias situações que exigirão que um aplicativo de backup funcione com dados copiados de sombra consistente com falhas:</span><span class="sxs-lookup"><span data-stu-id="2a514-106">There are several situations that will require a backup application to work with crash consistent shadow copied data:</span></span>

-   <span data-ttu-id="2a514-107">**Os dados são gerenciados por aplicativos sem reconhecimento de VSS**</span><span class="sxs-lookup"><span data-stu-id="2a514-107">**Data is managed by VSS-unaware applications**</span></span>

    <span data-ttu-id="2a514-108">Quase todos os sistemas terão alguns aplicativos: editores de texto, leitores de email, processadores de texto e assim por diante – que não sabem VSS, portanto, é sempre provável que alguns dos dados em uma cópia de sombra precisem ser considerados como estando em um estado consistente de falha.</span><span class="sxs-lookup"><span data-stu-id="2a514-108">Almost every system will have some applications—text editors, mail readers, word processors, and so forth—that are VSS unaware, so it is always likely that some of the data on a shadow copy will need to be thought of as being in a crash consistent state.</span></span>

    <span data-ttu-id="2a514-109">Esse tipo de dados normalmente não é crítico ao sistema ou ao serviço, portanto, o backup dele não deve ser problemático ou, pelo menos, não mais problemático do que durante um backup convencional.</span><span class="sxs-lookup"><span data-stu-id="2a514-109">This sort of data is not typically system- or service-critical, so backing it up should not be problematic, or at least no more problematic than during a conventional backup.</span></span>

    <span data-ttu-id="2a514-110">Assim como acontece com os backups convencionais, se possível, os operadores de backup devem tentar suspender ou encerrar esses aplicativos antes de iniciar um trabalho de backup do VSS.</span><span class="sxs-lookup"><span data-stu-id="2a514-110">As with preparations for conventional backups, if possible, backup operators should attempt to suspend or terminate such applications prior to starting a VSS backup job.</span></span>

-   <span data-ttu-id="2a514-111">**Sistema sem gravadores compatíveis com VSS**</span><span class="sxs-lookup"><span data-stu-id="2a514-111">**System with no VSS-compatible writers**</span></span>

    <span data-ttu-id="2a514-112">Essa situação pode ser relativamente rara, pois a maioria dos sistemas cujo backup pode ser feito por um aplicativo de backup do VSS terá uma versão do Windows habilitada para o VSS, que deve conter gravadores.</span><span class="sxs-lookup"><span data-stu-id="2a514-112">This situation may be relatively rare because most systems that can be backed up by a VSS backup application will have a VSS-enabled version of Windows, which should contain writers.</span></span>

    <span data-ttu-id="2a514-113">No entanto, há determinadas circunstâncias em que esse problema pode surgir — por exemplo, se você estiver fazendo backup de um sistema sem suporte a VSS, mas o sistema usar um dispositivo em rede habilitado para VSS para seu armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2a514-113">However, there are certain circumstances where this problem could arise—for instance, if you are backing up a system without VSS support but the system uses a VSS-enabled networked appliance for its storage.</span></span>

    <span data-ttu-id="2a514-114">Embora o backup do estado do sistema de uma imagem consistente com falhas não seja o ideal, pode ser suficiente para um computador reiniciar a um status operacional.</span><span class="sxs-lookup"><span data-stu-id="2a514-114">Although backing up a system's state from a crash-consistent image is not optimal, it may be sufficient for a computer to reboot to an operational status.</span></span> <span data-ttu-id="2a514-115">Em muitos casos, o computador será recuperado de todas as operações de e/s incompletas para os sistemas de arquivos e funcionará normalmente.</span><span class="sxs-lookup"><span data-stu-id="2a514-115">In many cases, the computer will recover from any incomplete I/O operations to the file systems and will operate normally.</span></span>

-   <span data-ttu-id="2a514-116">**Um solicitante optando por não trabalhar com os gravadores de sistema**</span><span class="sxs-lookup"><span data-stu-id="2a514-116">**A requester choosing not to work with the system writers**</span></span>

    <span data-ttu-id="2a514-117">Essa circunstância ocorreria se um solicitante optasse por não adicionar nenhum componente de gravador ou desabilitar todos os gravadores.</span><span class="sxs-lookup"><span data-stu-id="2a514-117">This circumstance would occur if a requester chose to add no writer components, or disabling all writers.</span></span>

    <span data-ttu-id="2a514-118">A realização de backups dessa maneira geralmente não é recomendável.</span><span class="sxs-lookup"><span data-stu-id="2a514-118">Performing backups in this way is generally discouraged.</span></span> <span data-ttu-id="2a514-119">Embora o volume de sombra copiado para backup possa ser suficiente para restaurar um sistema para em execução, ele não é desejável.</span><span class="sxs-lookup"><span data-stu-id="2a514-119">Although the shadow-copied volume to back up might be sufficient to restore a system to running, it is not desirable.</span></span> <span data-ttu-id="2a514-120">Na verdade, como os gravadores em execução no sistema são projetados com a funcionalidade para cooperar com as cópias de sombra e VSS, o backup de seus dados dessa maneira pode resultar em instabilidade.</span><span class="sxs-lookup"><span data-stu-id="2a514-120">In fact, given that the writers running on the system are designed with functionality to cooperate with VSS and shadow copies, backing up their data in this way might result in instability.</span></span>

 

 



