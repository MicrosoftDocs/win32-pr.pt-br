---
description: Glossário de termos usados na documentação do SDK de virtualização do Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Glossário do Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171298"
---
# <a name="hyper-v-glossary"></a><span data-ttu-id="c04b7-103">Glossário do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="c04b7-103">Hyper-V glossary</span></span>

<span data-ttu-id="c04b7-104">Este tópico fornece um glossário de termos usados na documentação do SDK de virtualização do Windows.</span><span class="sxs-lookup"><span data-stu-id="c04b7-104">This topic provides a glossary of terms used in the Windows Virtualization SDK documentation.</span></span>

<dl> <dt>

<span data-ttu-id="c04b7-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**vinculação**</span><span class="sxs-lookup"><span data-stu-id="c04b7-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-106">Um processo pelo qual os serviços de software e as camadas são vinculados juntos.</span><span class="sxs-lookup"><span data-stu-id="c04b7-106">A process by which software services and layers are linked together.</span></span> <span data-ttu-id="c04b7-107">Quando um serviço de rede é instalado, as relações de associação e dependências para os serviços são estabelecidas.</span><span class="sxs-lookup"><span data-stu-id="c04b7-107">When a network service is installed, the binding relationships and dependencies for the services are established.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**verifica**</span><span class="sxs-lookup"><span data-stu-id="c04b7-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**checkpoint**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-109">Um instantâneo de uma máquina virtual que permite que um administrador role a máquina virtual de volta para seu estado no momento em que o ponto de verificação foi criado.</span><span class="sxs-lookup"><span data-stu-id="c04b7-109">A snapshot of a virtual machine that enables an administrator to roll the virtual machine back to its state at the moment the checkpoint was created.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compactá**</span><span class="sxs-lookup"><span data-stu-id="c04b7-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compact**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-111">Para reduzir o tamanho de um disco rígido virtual de expansão dinâmica removendo o espaço não utilizado do arquivo. vhd.</span><span class="sxs-lookup"><span data-stu-id="c04b7-111">To reduce the size of a dynamically expanding virtual hard disk by removing unused space from the .vhd file.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**disco rígido virtual diferencial**</span><span class="sxs-lookup"><span data-stu-id="c04b7-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differencing virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-113">Um disco rígido virtual que armazena as alterações em um disco rígido virtual pai associado com a finalidade de manter o pai intacto.</span><span class="sxs-lookup"><span data-stu-id="c04b7-113">A virtual hard disk that stores the changes to an associated parent virtual hard disk for the purpose of keeping the parent intact.</span></span> <span data-ttu-id="c04b7-114">O disco diferencial é um arquivo. vhd separado que está associado ao arquivo. vhd do disco pai.</span><span class="sxs-lookup"><span data-stu-id="c04b7-114">The differencing disk is a separate .vhd file that is associated with the .vhd file of the parent disk.</span></span> <span data-ttu-id="c04b7-115">As alterações continuam a se acumular no disco diferencial até que ele seja mesclado ao disco pai.</span><span class="sxs-lookup"><span data-stu-id="c04b7-115">Changes continue to accumulate in the differencing disk until it is merged to the parent disk.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**disco rígido virtual de expansão dinâmica**</span><span class="sxs-lookup"><span data-stu-id="c04b7-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamically expanding virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-117">Um disco rígido virtual que cresce em tamanho cada vez que é modificado.</span><span class="sxs-lookup"><span data-stu-id="c04b7-117">A virtual hard disk that grows in size each time it is modified.</span></span> <span data-ttu-id="c04b7-118">Esse tipo de disco rígido virtual é iniciado como um arquivo. VHD de 3 KB e pode crescer tão grande quanto o tamanho máximo especificado quando o arquivo foi criado.</span><span class="sxs-lookup"><span data-stu-id="c04b7-118">This type of virtual hard disk starts as a 3 KB .vhd file and can grow as large as the maximum size specified when the file was created.</span></span> <span data-ttu-id="c04b7-119">A única maneira de reduzir o tamanho do arquivo é zerar os dados excluídos e, em seguida, compactar o disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="c04b7-119">The only way to reduce the file size is to zero out the deleted data and then compact the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**disco rígido virtual de tamanho fixo**</span><span class="sxs-lookup"><span data-stu-id="c04b7-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**fixed-size virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-121">Um disco rígido virtual com um tamanho fixo que é determinado e para o qual todo o espaço é alocado quando o disco é criado.</span><span class="sxs-lookup"><span data-stu-id="c04b7-121">A virtual hard disk with a fixed size that is determined and for which all space is allocated when the disk is created.</span></span> <span data-ttu-id="c04b7-122">O tamanho do disco não é alterado quando os dados são adicionados ou excluídos.</span><span class="sxs-lookup"><span data-stu-id="c04b7-122">The size of the disk does not change when data is added or deleted.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Máquina virtual de geração 1**</span><span class="sxs-lookup"><span data-stu-id="c04b7-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Generation 1 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-124">Uma VM (máquina virtual) que contém o mesmo hardware virtual presente nas versões do Hyper-V anteriores ao Windows 8.1 e ao Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c04b7-124">A virtual machine (VM) that contains the same virtual hardware present in versions of Hyper-V prior to Windows 8.1 and Windows Server 2012 R2</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Máquina virtual de geração 2**</span><span class="sxs-lookup"><span data-stu-id="c04b7-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Generation 2 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-126">Uma VM (máquina virtual) que contém um modelo de hardware virtual simplificado e usa o firmware UEFI em vez do BIOS.</span><span class="sxs-lookup"><span data-stu-id="c04b7-126">A virtual machine (VM) that contains a simplified virtual hardware model and uses UEFI firmware instead of BIOS.</span></span> <span data-ttu-id="c04b7-127">Nessa VM, a maioria dos dispositivos emulados é removida, o que reduz a complexidade de gerenciamento e a superfície de ataque de segurança.</span><span class="sxs-lookup"><span data-stu-id="c04b7-127">In this VM, most of the emulated devices are removed, which reduces management complexity and security attack surface.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**sistema operacional convidado**</span><span class="sxs-lookup"><span data-stu-id="c04b7-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**guest operating system**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-129">O sistema operacional em execução em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c04b7-129">The operating system running on a virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**serviços de integração**</span><span class="sxs-lookup"><span data-stu-id="c04b7-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-131">Uma coleção de serviços e drivers de software que maximizam o desempenho e fornecem uma melhor experiência de usuário em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c04b7-131">A collection of services and software drivers that maximize performance and provide a better user experience within a virtual machine.</span></span> <span data-ttu-id="c04b7-132">O Integration Services só está disponível para sistemas operacionais convidados com suporte.</span><span class="sxs-lookup"><span data-stu-id="c04b7-132">Integration services are only available for supported guest operating systems.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**par chave-valor**</span><span class="sxs-lookup"><span data-stu-id="c04b7-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**key-value pair**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-134">Um conjunto de itens de dados que contém um identificador exclusivo, chamado de chave, e um valor que são os dados reais para a chave.</span><span class="sxs-lookup"><span data-stu-id="c04b7-134">A set of data items that contains a unique identifier, called a key, and a value that is the actual data for the key.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**computador físico**</span><span class="sxs-lookup"><span data-stu-id="c04b7-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physical computer**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-136">Um computador baseado em hardware, em oposição a uma máquina virtual baseada em software.</span><span class="sxs-lookup"><span data-stu-id="c04b7-136">A hardware-based computer, as opposed to a software-based virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**estado salvo**</span><span class="sxs-lookup"><span data-stu-id="c04b7-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**saved state**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-138">Uma maneira de armazenar uma máquina virtual para que ela possa ser retomada rapidamente, semelhante a um laptop hibernado.</span><span class="sxs-lookup"><span data-stu-id="c04b7-138">A manner of storing a virtual machine so that it can be quickly resumed, similar to a hibernated laptop.</span></span> <span data-ttu-id="c04b7-139">Quando você coloca uma máquina virtual em execução em um estado salvo, o Virtual Server e o Hyper-V param a máquina virtual, gravam os dados que existem na memória em arquivos temporários e param o consumo dos recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="c04b7-139">When you place a running virtual machine in a saved state, Virtual Server and Hyper-V stop the virtual machine, write the data that exists in memory to temporary files, and stop the consumption of system resources.</span></span> <span data-ttu-id="c04b7-140">A restauração de uma máquina virtual de um estado salvo a retorna para a mesma condição em que estava quando seu estado foi salvo.</span><span class="sxs-lookup"><span data-stu-id="c04b7-140">Restoring a virtual machine from a saved state returns it to the same condition it was in when its state was saved.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**disquete virtual**</span><span class="sxs-lookup"><span data-stu-id="c04b7-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtual floppy disk**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-142">Uma versão baseada em arquivo de um disquete físico.</span><span class="sxs-lookup"><span data-stu-id="c04b7-142">A file-based version of a physical floppy disk.</span></span> <span data-ttu-id="c04b7-143">Um disquete virtual é armazenado como um arquivo com uma extensão de nome de arquivo. VFD.</span><span class="sxs-lookup"><span data-stu-id="c04b7-143">A virtual floppy disk is stored as a file with a .vfd file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**disco rígido virtual**</span><span class="sxs-lookup"><span data-stu-id="c04b7-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-145">O meio de armazenamento para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c04b7-145">The storage medium for a virtual machine.</span></span> <span data-ttu-id="c04b7-146">Ele pode residir em qualquer topologia de armazenamento que o sistema operacional do host possa acessar, incluindo dispositivos externos, redes de área de armazenamento e armazenamento anexado à rede.</span><span class="sxs-lookup"><span data-stu-id="c04b7-146">It can reside on any storage topology that the host operating system can access, including external devices, storage area networks, and network-attached storage.</span></span> <span data-ttu-id="c04b7-147">A extensão de nome de arquivo é. vhd.</span><span class="sxs-lookup"><span data-stu-id="c04b7-147">The file name extension is .vhd.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**máquina virtual**</span><span class="sxs-lookup"><span data-stu-id="c04b7-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-149">Um computador em um computador, implementado em software.</span><span class="sxs-lookup"><span data-stu-id="c04b7-149">A computer within a computer, implemented in software.</span></span> <span data-ttu-id="c04b7-150">Uma máquina virtual emula um sistema de hardware completo, do processador para a placa de rede, em um ambiente de software isolado e independente, permitindo a operação simultânea de sistemas operacionais incompatíveis de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c04b7-150">A virtual machine emulates a complete hardware system, from processor to network card, in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible operating systems.</span></span> <span data-ttu-id="c04b7-151">Cada sistema operacional filho é executado em sua própria máquina virtual de software isolado.</span><span class="sxs-lookup"><span data-stu-id="c04b7-151">Each child operating system runs in its own isolated software virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**configuração de máquina virtual**</span><span class="sxs-lookup"><span data-stu-id="c04b7-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**virtual machine configuration**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-153">A configuração dos recursos atribuídos a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c04b7-153">The configuration of the resources assigned to a virtual machine.</span></span> <span data-ttu-id="c04b7-154">Os exemplos incluem dispositivos como discos e adaptadores de rede, bem como memória e processadores.</span><span class="sxs-lookup"><span data-stu-id="c04b7-154">Examples include devices such as disks and network adapters, as well as memory and processors.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Serviço de gerenciamento de máquinas virtuais**</span><span class="sxs-lookup"><span data-stu-id="c04b7-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Virtual Machine Management Service**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-156">O serviço do Hyper-V que fornece acesso de gerenciamento a máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="c04b7-156">The Hyper-V service that provides management access to virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**instantâneo da máquina virtual**</span><span class="sxs-lookup"><span data-stu-id="c04b7-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**virtual machine snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-158">Um instantâneo baseado em arquivo do estado, dos dados do disco e da configuração de uma máquina virtual em um ponto específico no tempo.</span><span class="sxs-lookup"><span data-stu-id="c04b7-158">A file-based snapshot of the state, disk data, and configuration of a virtual machine at a specific point in time.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**rede virtual**</span><span class="sxs-lookup"><span data-stu-id="c04b7-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtual network**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-160">Uma versão virtual de um comutador de rede física.</span><span class="sxs-lookup"><span data-stu-id="c04b7-160">A virtual version of a physical network switch.</span></span> <span data-ttu-id="c04b7-161">Uma rede virtual pode ser configurada para fornecer acesso a recursos de rede locais ou externos para uma ou mais máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="c04b7-161">A virtual network can be configured to provide access to local or external network resources for one or more virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Gerenciador de rede virtual**</span><span class="sxs-lookup"><span data-stu-id="c04b7-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network Manager**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-163">Um serviço do Hyper-V usado para criar e gerenciar redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="c04b7-163">A Hyper-V service used to create and manage virtual networks.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**comutador virtual**</span><span class="sxs-lookup"><span data-stu-id="c04b7-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtual switch**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-165">Consulte rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c04b7-165">See virtual network.</span></span>

</dd> <dt>

<span data-ttu-id="c04b7-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Redimensionamento de VHDX**</span><span class="sxs-lookup"><span data-stu-id="c04b7-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX resize**</span></span>
</dt> <dd>

<span data-ttu-id="c04b7-167">A operação que reduz ou expande um disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="c04b7-167">The operation that shrinks or expands a virtual hard disk.</span></span>

</dd> </dl>

 

 



