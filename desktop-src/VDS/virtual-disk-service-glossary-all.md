---
description: Esta seção fornece um glossário de termos técnicos usados na documentação do VDS (serviço de disco virtual).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossário do serviço de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc8804f1aea832f59fcbcab65423e92e134939f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921826"
---
# <a name="virtual-disk-service-glossary"></a>Glossário do serviço de disco virtual

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Esta seção fornece um glossário de termos técnicos usados na documentação do VDS (serviço de disco virtual).

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configuração do automagic**
</dt> <dd>

Provedor de RAID de hardware que fornece um conjunto de regras para escolher o remapeamento de bloco lógico LUN com base em atributos simples. Os provedores automagic também podem alterar dinamicamente o mapeamento para desempenho ou gerenciamento de falhas.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**Dicas do automagic**
</dt> <dd>

Informações fornecidas a um provedor automagic para orientar a configuração de bloco lógico de LUN. As dicas incluem informações sobre a tolerância a falhas, a atomicidade física e o padrão de acesso de e/s desejado.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco básico**
</dt> <dd>

Um disco gerenciado pelo provedor de software mais simples possível. O provedor de disco básico dá suporte apenas a volumes que são mapeados diretamente para as estruturas de dados de configuração de partição.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**vinculação**
</dt> <dd>

Selecionando um conjunto de mapeamentos para recursos físicos.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**vertê**
</dt> <dd>

O processo de converter um disco básico em um disco dinâmico.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuração**
</dt> <dd>

Uma coleção de parâmetros operacionais que fornecem o mapeamento de um volume, ou LUN, para recursos físicos.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controle**
</dt> <dd>

Um programa de software que contém a inteligência de tempo de execução para um provedor de hardware.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**disco**
</dt> <dd>

Um disco físico ou LUN RAID de hardware. Os discos são destinos para carga de e/s de armazenamento em tempo de execução; A Plug and Play (PNP) não faz distinção entre JBOD e LUNs.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**platter de disco**
</dt> <dd>

Um subconjunto de um pacote usado para exportar ou importar volumes de um pacote.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**pacote de disco**
</dt> <dd>

Consulte o *pacote*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**Dirigir**
</dt> <dd>

Um eixo de disco físico em um subsistema RAID de hardware. As unidades são associadas a LUNs pelo subsistema.

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinâmico**
</dt> <dd>

Um disco gerenciado por um provedor de RAID de software com suporte para reconfiguração de volume flexível. Um disco dinâmico usa uma partição como um contêiner para volumes; Não há nenhum mapeamento garantido.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configuração explícita**
</dt> <dd>

Uma configuração com os parâmetros, incluindo o tipo de volume e o layout exato, para uma coleção de volumes de destino.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**Export**
</dt> <dd>

O ato de mover um platter de disco e todos os volumes contidos nesse platter para fora de um pacote.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**tention**
</dt> <dd>

Um intervalo contíguo de setores lógicos que contribuem para um único volume ou disco. Uma extensão também pode ser um intervalo de setores não alocados. Normalmente, um sistema de arquivos exibe os detalhes de extensão para um usuário final.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabela de partição GUID (GPT)**
</dt> <dd>

Estruturas usadas pelo firmware EFI. O GPT é um dos dois formatos de dados de configuração de software de nível mais baixo usados pelo firmware de plataforma para localizar um sistema operacional inicializável ou outra imagem executável.

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**provedor de hardware**
</dt> <dd>

Uma coleção de software que é executada no host, um adaptador de barramento e, possivelmente, um subsistema de armazenamento externo que funciona em conjunto para a superfície e o gerenciamento de LUNs RAID. Os provedores de hardware para a maioria dos subsistemas de armazenamento externos contêm apenas o software de modo de usuário, baseado em host.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**monitoramento**
</dt> <dd>

O status atual de gerenciamento de falhas de um volume ou LUN.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**Hot Sparing**
</dt> <dd>

Adicionando temporariamente um plex de volume a um volume.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**importe**
</dt> <dd>

O ato de mover um platter de disco e todos os seus volumes para um pacote existente.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**apenas um monte de discos (JBOD)**
</dt> <dd>

Uma coleção de eixos físicos sem o controle coordenado fornecido por um dispositivo RAID de hardware.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**número de bloco lógico (LBN)**
</dt> <dd>

A menor unidade endereçável de dados de armazenamento. LBN é usado com protocolos de comando de e/s.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**mapeamento de bloco lógico**
</dt> <dd>

A transformação dos blocos lógicos apresentados a um provedor para aqueles expostos pelo provedor.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**LUN (número de unidade lógica)**
</dt> <dd>

Uma unidade de armazenamento fisicamente endereçável, como na superfície de um subsistema RAID de hardware. Esse termo também pode se referir ao identificador SCSI para a unidade de armazenamento.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Número de LUN**
</dt> <dd>

Um número que um provedor de hardware VDS atribui a um LUN em uma matriz. Isso não é o mesmo que o "número de unidade lógica" no endereço SCSI do disco.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**serviço de gerenciamento**
</dt> <dd>

Um programa de software que é executado conforme necessário para executar a configuração, o monitoramento ou o tratamento de falhas do volume.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**correlação**
</dt> <dd>

Um volume que é exposto ao sistema operacional e tem um nome de volume associado (uma letra de unidade). Um volume pode ser acessado por um sistema de arquivos.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**mascaramento**
</dt> <dd>

Um disco não reconhecido pelo sistema operacional. Um disco pode ser mascarado pelo subsistema RAID de hardware, comutador, reserva SCSI por outro host de computador ou software na pilha de discos.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**particionamento mestre de registro de inicialização (MBR)**
</dt> <dd>

MBR é um dos dois formatos de dados de configuração de software de nível mais baixo e é usado pelo firmware do BIOS para localizar uma imagem do sistema operacional inicializável.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**associado**
</dt> <dd>

Uma coleção de extensões de disco concatenadas contidas em um ou mais discos. Um disco pode contribuir para apenas um membro de um volume.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**espelho**
</dt> <dd>

Um volume ou mapeamento de disco que mantém duas ou mais cópias de dados idênticas. O tipo de mapeamento também é chamado de nível de RAID 1.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**pacotes**
</dt> <dd>

Uma coleção de volumes lógicos e discos subjacentes. Um pacote é a unidade de fechamento transitório de um volume. Os pacotes de disco dinâmico e os grupos de discos são os termos do mesmo item.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**faixa de paridade**
</dt> <dd>

Um volume ou mapeamento de disco que mantém informações de verificação de paridade, bem como dados. Cada fornecedor fornece o mapeamento exato e o esquema de proteção. Inclui RAID 3, 4, 5 e 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configuração parcialmente direcionada**
</dt> <dd>

Uma configuração de volume ou disco que não é totalmente explícita. O tipo de associação e uma coleção de recursos de destino são especificados; o layout real não é. A configuração parcialmente direcionada é a configuração de volume mais comum.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**particion**
</dt> <dd>

Um intervalo contíguo de setores lógicos descrito por uma única entrada na estrutura MBR ou GPT. Em discos básicos, as partições correspondem diretamente aos volumes simples. As estruturas de partição são compartilhadas entre o firmware da plataforma BIOS ou EFI e um sistema operacional ou outra imagem inicializável.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**Multi-Path**
</dt> <dd>

O caminho de acesso de um computador para um disco ou LUN de hardware externo.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**plexos**
</dt> <dd>

Um membro de um volume espelhado ou LUN.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**Porto**
</dt> <dd>

O ponto de extremidade de um caminho em um disco.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**matriz redundante de discos independentes (RAID)**
</dt> <dd>

Uma coleção de técnicas para gerenciar vários discos.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**serviço de tempo de execução**
</dt> <dd>

Um programa de software que é executado em uma base de solicitação de e/s.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco simples**
</dt> <dd>

Um eixo que não está conectado a um controlador RAID de hardware. Consulte também apenas um monte de discos (JBOD).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**provedor de software**
</dt> <dd>

Software baseado em host que expõe volumes lógicos e opera em discos. Um provedor de software inclui serviços de tempo de execução de modo kernel, dados de configuração e serviços de gerenciamento de modo de usuário.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**compreende**
</dt> <dd>

Um mapeamento linear de volume ou disco de várias extensões de disco ou unidade descontínuas. As extensões podem estar em um ou mais eixos ou LUNs.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**eixo**
</dt> <dd>

Uma unidade física de armazenamento em disco.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**empilhamento**
</dt> <dd>

O ato de construir um volume ou LUN executando mais de uma operação de mapeamento de bloco lógico. Um exemplo é um volume distribuído espelhado. A pilha mais comum ocorre quando o RAID de software é usado em LUNs construídos pelo RAID de hardware.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Stripe**
</dt> <dd>

Um volume ou mapeamento de disco que intercala extensões contíguas em vários volumes, discos ou unidades. Esse mapeamento também é chamado de RAID 0.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**Estado**
</dt> <dd>

A disponibilidade atual de um volume, disco ou unidade.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsistema**
</dt> <dd>

A instanciação do software do provedor de hardware. Um subsistema contém pelo menos um controlador e uma unidade. Se o subsistema for externo ao computador, um ou mais caminhos de rede conectarão o subsistema ao computador.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**Estado de transição**
</dt> <dd>

Status do mapeamento lógico para físico que está sendo alterado.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco não inicializado**
</dt> <dd>

Um disco que não é um membro de um pacote.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco não mascarado**
</dt> <dd>

Um disco que é visível para o sistema operacional. O conteúdo de um disco não mascarado é visível para gerenciadores de volume de software, sistemas de arquivos e assim por diante.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**
</dt> <dd>

Várias extensões de disco associadas a um intervalo praticamente contíguo de blocos lógicos. Um volume pode ser acessado por meio de uma letra de unidade, uma pasta montada ou um caminho de GUID de volume.

</dd> </dl>

 

 
