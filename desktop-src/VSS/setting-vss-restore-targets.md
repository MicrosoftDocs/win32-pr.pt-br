---
description: A interface IVssComponent permite que um gravador ajuste exatamente como os arquivos são restaurados em uma base componente por componente.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Definindo destinos de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797488"
---
# <a name="setting-vss-restore-targets"></a><span data-ttu-id="648b0-103">Definindo destinos de restauração do VSS</span><span class="sxs-lookup"><span data-stu-id="648b0-103">Setting VSS Restore Targets</span></span>

<span data-ttu-id="648b0-104">A interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permite que um gravador ajuste exatamente como os arquivos são restaurados em uma base componente por componente.</span><span class="sxs-lookup"><span data-stu-id="648b0-104">The [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface enables a writer to fine-tune exactly how files are restored on a component-by-component basis.</span></span>

<span data-ttu-id="648b0-105">Como é possível que a configuração do sistema durante a restauração seja algo diferente daquele previsto durante o backup, o mecanismo de destino de restauração é fornecido.</span><span class="sxs-lookup"><span data-stu-id="648b0-105">Because it is possible that the system configuration during restore is something other than that anticipated during backup, the restore target mechanism is provided.</span></span>

<span data-ttu-id="648b0-106">Ele permite que os gravadores chamem [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) para alterar a forma como os componentes [*incluídos explicitamente*](vssgloss-e.md) no documento de componentes de backup são restaurados.</span><span class="sxs-lookup"><span data-stu-id="648b0-106">It allows writers to call [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) to change how those components that are [*explicitly included*](vssgloss-e.md) in the Backup Components Document are restored.</span></span> <span data-ttu-id="648b0-107">Isso também altera o mecanismo de restauração usado nesses componentes que são [*incluídos implicitamente*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="648b0-107">This also changes the restoration mechanism used on those components that are [*implicitly included*](vssgloss-i.md).</span></span>

<span data-ttu-id="648b0-108">Restauração de arquivo que ocorre durante uma reinicialização do sistema (sob os valores de enumeração de enumeração do [**VSS \_ \_ RESTOREMETHOD**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) o VSS \_ RME \_ Restore \_ na \_ reinicialização e o VSS \_ RME \_ Restore \_ na \_ reinicialização \_ se \_ não puder \_ substituir) não pode ser afetado por destinos de restauração porque não há serviços VSS em execução quando **MoveFileEx** copia arquivos para o local final.</span><span class="sxs-lookup"><span data-stu-id="648b0-108">File restoration that takes place during a system reboot (under the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration values VSS\_RME\_RESTORE\_AT\_REBOOT and VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE) cannot be affected by restore targets because there are no running VSS services when **MoveFileEx** copies files to their final location.</span></span>

<span data-ttu-id="648b0-109">Da mesma forma, as \_ \_ restaurações personalizadas do VSS RME podem ou não ser afetadas, porque cada restauração personalizada é específica para um determinado gravador e pode optar por respeitar ou ignorar destinos de restauração.</span><span class="sxs-lookup"><span data-stu-id="648b0-109">Similarly, VSS\_RME\_CUSTOM restores may or may not be affected, because each custom restore is specific to a given writer and can choose to respect or ignore restore targets.</span></span>

<span data-ttu-id="648b0-110">Os solicitantes e gravadores podem usar [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) para verificar o destino de restauração de um conjunto de componentes.</span><span class="sxs-lookup"><span data-stu-id="648b0-110">Requesters and writers can use [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) to check the restore target of a component set.</span></span>

<span data-ttu-id="648b0-111">O [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) dá suporte aos seguintes destinos de restauração, que podem ser definidos em um conjunto de componentes pela base do conjunto de componentes:</span><span class="sxs-lookup"><span data-stu-id="648b0-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supports the following restore targets, which can be set on a component set by component set basis:</span></span>

-   <span data-ttu-id="648b0-112">ORIGINAL do VSS \_ RT \_ .</span><span class="sxs-lookup"><span data-stu-id="648b0-112">VSS\_RT\_ORIGINAL.</span></span> <span data-ttu-id="648b0-113">O método de restauração especificado pela enumeração de [**\_ \_ Enumeração RESTOREMETHOD do VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) será respeitado.</span><span class="sxs-lookup"><span data-stu-id="648b0-113">The restore method specified by the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration will be respected.</span></span>
-   <span data-ttu-id="648b0-114">alternativa do VSS \_ RT \_ .</span><span class="sxs-lookup"><span data-stu-id="648b0-114">VSS\_RT\_ALTERNATE.</span></span> <span data-ttu-id="648b0-115">Os arquivos são restaurados em um local determinado a partir de um mapeamento de local alternativo existente.</span><span class="sxs-lookup"><span data-stu-id="648b0-115">The files are restored to a location determined from an existing alternate location mapping.</span></span> <span data-ttu-id="648b0-116">Se houver um mapeamento de local alternativo correspondente a um caminho em um subcomponente do conjunto de componentes, restaure para o local alternativo, se possível; caso contrário, retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="648b0-116">If an alternate location mapping matching a path in a component set subcomponent exists, restore to the alternate location if possible; otherwise, return an error.</span></span>

 

 



