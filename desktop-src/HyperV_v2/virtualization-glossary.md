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
# <a name="hyper-v-glossary"></a>Glossário do Hyper-V

Este tópico fornece um glossário de termos usados na documentação do SDK de virtualização do Windows.

<dl> <dt>

<span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**vinculação**
</dt> <dd>

Um processo pelo qual os serviços de software e as camadas são vinculados juntos. Quando um serviço de rede é instalado, as relações de associação e dependências para os serviços são estabelecidas.

</dd> <dt>

<span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**verifica**
</dt> <dd>

Um instantâneo de uma máquina virtual que permite que um administrador role a máquina virtual de volta para seu estado no momento em que o ponto de verificação foi criado.

</dd> <dt>

<span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compactá**
</dt> <dd>

Para reduzir o tamanho de um disco rígido virtual de expansão dinâmica removendo o espaço não utilizado do arquivo. vhd.

</dd> <dt>

<span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**disco rígido virtual diferencial**
</dt> <dd>

Um disco rígido virtual que armazena as alterações em um disco rígido virtual pai associado com a finalidade de manter o pai intacto. O disco diferencial é um arquivo. vhd separado que está associado ao arquivo. vhd do disco pai. As alterações continuam a se acumular no disco diferencial até que ele seja mesclado ao disco pai.

</dd> <dt>

<span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**disco rígido virtual de expansão dinâmica**
</dt> <dd>

Um disco rígido virtual que cresce em tamanho cada vez que é modificado. Esse tipo de disco rígido virtual é iniciado como um arquivo. VHD de 3 KB e pode crescer tão grande quanto o tamanho máximo especificado quando o arquivo foi criado. A única maneira de reduzir o tamanho do arquivo é zerar os dados excluídos e, em seguida, compactar o disco rígido virtual.

</dd> <dt>

<span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**disco rígido virtual de tamanho fixo**
</dt> <dd>

Um disco rígido virtual com um tamanho fixo que é determinado e para o qual todo o espaço é alocado quando o disco é criado. O tamanho do disco não é alterado quando os dados são adicionados ou excluídos.

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Máquina virtual de geração 1**
</dt> <dd>

Uma VM (máquina virtual) que contém o mesmo hardware virtual presente nas versões do Hyper-V anteriores ao Windows 8.1 e ao Windows Server 2012 R2

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Máquina virtual de geração 2**
</dt> <dd>

Uma VM (máquina virtual) que contém um modelo de hardware virtual simplificado e usa o firmware UEFI em vez do BIOS. Nessa VM, a maioria dos dispositivos emulados é removida, o que reduz a complexidade de gerenciamento e a superfície de ataque de segurança.

</dd> <dt>

<span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**sistema operacional convidado**
</dt> <dd>

O sistema operacional em execução em uma máquina virtual.

</dd> <dt>

<span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**serviços de integração**
</dt> <dd>

Uma coleção de serviços e drivers de software que maximizam o desempenho e fornecem uma melhor experiência de usuário em uma máquina virtual. O Integration Services só está disponível para sistemas operacionais convidados com suporte.

</dd> <dt>

<span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**par chave-valor**
</dt> <dd>

Um conjunto de itens de dados que contém um identificador exclusivo, chamado de chave, e um valor que são os dados reais para a chave.

</dd> <dt>

<span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**computador físico**
</dt> <dd>

Um computador baseado em hardware, em oposição a uma máquina virtual baseada em software.

</dd> <dt>

<span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**estado salvo**
</dt> <dd>

Uma maneira de armazenar uma máquina virtual para que ela possa ser retomada rapidamente, semelhante a um laptop hibernado. Quando você coloca uma máquina virtual em execução em um estado salvo, o Virtual Server e o Hyper-V param a máquina virtual, gravam os dados que existem na memória em arquivos temporários e param o consumo dos recursos do sistema. A restauração de uma máquina virtual de um estado salvo a retorna para a mesma condição em que estava quando seu estado foi salvo.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**disquete virtual**
</dt> <dd>

Uma versão baseada em arquivo de um disquete físico. Um disquete virtual é armazenado como um arquivo com uma extensão de nome de arquivo. VFD.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**disco rígido virtual**
</dt> <dd>

O meio de armazenamento para uma máquina virtual. Ele pode residir em qualquer topologia de armazenamento que o sistema operacional do host possa acessar, incluindo dispositivos externos, redes de área de armazenamento e armazenamento anexado à rede. A extensão de nome de arquivo é. vhd.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**máquina virtual**
</dt> <dd>

Um computador em um computador, implementado em software. Uma máquina virtual emula um sistema de hardware completo, do processador para a placa de rede, em um ambiente de software isolado e independente, permitindo a operação simultânea de sistemas operacionais incompatíveis de outra forma. Cada sistema operacional filho é executado em sua própria máquina virtual de software isolado.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**configuração de máquina virtual**
</dt> <dd>

A configuração dos recursos atribuídos a uma máquina virtual. Os exemplos incluem dispositivos como discos e adaptadores de rede, bem como memória e processadores.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Serviço de gerenciamento de máquinas virtuais**
</dt> <dd>

O serviço do Hyper-V que fornece acesso de gerenciamento a máquinas virtuais.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**instantâneo da máquina virtual**
</dt> <dd>

Um instantâneo baseado em arquivo do estado, dos dados do disco e da configuração de uma máquina virtual em um ponto específico no tempo.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**rede virtual**
</dt> <dd>

Uma versão virtual de um comutador de rede física. Uma rede virtual pode ser configurada para fornecer acesso a recursos de rede locais ou externos para uma ou mais máquinas virtuais.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Gerenciador de rede virtual**
</dt> <dd>

Um serviço do Hyper-V usado para criar e gerenciar redes virtuais.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**comutador virtual**
</dt> <dd>

Consulte rede virtual.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Redimensionamento de VHDX**
</dt> <dd>

A operação que reduz ou expande um disco rígido virtual.

</dd> </dl>

 

 



