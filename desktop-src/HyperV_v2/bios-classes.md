---
description: O BIOS virtual é uma imagem de software que é carregada na RAM para configurar alguns dos aspectos básicos do e a inicialização de um sistema de computador. Há um elemento BIOS por sistema de computador e esse elemento não pode ser substituído ou removido.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Classes do BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921785"
---
# <a name="bios-classes"></a><span data-ttu-id="9b19b-104">Classes do BIOS</span><span class="sxs-lookup"><span data-stu-id="9b19b-104">BIOS classes</span></span>

<span data-ttu-id="9b19b-105">O BIOS virtual é uma imagem de software que é carregada na RAM para configurar alguns dos aspectos básicos do e a inicialização de um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="9b19b-105">The virtual BIOS is a software image that is loaded into RAM to configure some of the basic aspects of and boot a computer system.</span></span> <span data-ttu-id="9b19b-106">Há um elemento BIOS por sistema de computador e esse elemento não pode ser substituído ou removido.</span><span class="sxs-lookup"><span data-stu-id="9b19b-106">There is one BIOS element per computer system and that element cannot be replaced or removed.</span></span> <span data-ttu-id="9b19b-107">Portanto, não há nenhum pool de recursos para adicionar novos elementos BIOS à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b19b-107">Thus, there is no resource pool for adding new BIOS elements to the virtual machine.</span></span> <span data-ttu-id="9b19b-108">O elemento BIOS também não tem sua própria classe SettingData para descrever as configurações do BIOS.</span><span class="sxs-lookup"><span data-stu-id="9b19b-108">The BIOS element also does not have its own SettingData class to describe the settings for the BIOS.</span></span> <span data-ttu-id="9b19b-109">As configurações do BIOS, como números de série, ordem de inicialização e estado de bloqueio num, são encontradas na classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="9b19b-109">Settings for the BIOS, such as serial numbers, boot order, and num lock state, are found in the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span>

<span data-ttu-id="9b19b-110">Veja a seguir as classes WMI de virtualização relacionadas ao BIOS.</span><span class="sxs-lookup"><span data-stu-id="9b19b-110">The following are virtualization WMI classes related to the BIOS.</span></span> <span data-ttu-id="9b19b-111">Essas classes estão no \\ \\ . \\ \\Namespace de virtualização de raiz.</span><span class="sxs-lookup"><span data-stu-id="9b19b-111">These classes are in the \\\\.\\Root\\Virtualization namespace.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b19b-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9b19b-112">In this section</span></span>



| <span data-ttu-id="9b19b-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="9b19b-113">Topic</span></span>                                                    | <span data-ttu-id="9b19b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9b19b-114">Description</span></span>                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b19b-115">**\_Bioselement Msvm**</span><span class="sxs-lookup"><span data-stu-id="9b19b-115">**Msvm\_BIOSElement**</span></span>](msvm-bioselement.md)<br/> | <span data-ttu-id="9b19b-116">Representa o software de nível baixo que é carregado na RAM para configurar e iniciar o sistema.</span><span class="sxs-lookup"><span data-stu-id="9b19b-116">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span><br/> |
| [<span data-ttu-id="9b19b-117">**Msvm \_ SystemBIOS**</span><span class="sxs-lookup"><span data-stu-id="9b19b-117">**Msvm\_SystemBIOS**</span></span>](msvm-systembios.md)<br/>   | <span data-ttu-id="9b19b-118">Usado para associar uma máquina virtual a seu BIOS.</span><span class="sxs-lookup"><span data-stu-id="9b19b-118">Used to associate a virtual machine with its BIOS.</span></span><br/>                                           |



 

 

 




