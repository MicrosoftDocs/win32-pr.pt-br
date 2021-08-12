---
description: Esta seção fornece um glossário dos termos técnicos usados na documentação do VDS (Serviço de Disco Virtual).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossário do Serviço de Disco Virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7e73e9de8f6c30b69f2e39e78fae36e5c3ea547cccfed2f25f9a15327e3f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602989"
---
# <a name="virtual-disk-service-glossary"></a>Glossário do Serviço de Disco Virtual

\[Começando com Windows 8 e Windows Server 2012, a interface COM do Serviço de Disco [Virtual](virtual-disk-service-portal.md) é superada pelo [Windows Armazenamento API de Gerenciamento](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Esta seção fornece um glossário dos termos técnicos usados na documentação do VDS (Serviço de Disco Virtual).

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configuração automagica**
</dt> <dd>

Provedor RAID de hardware que fornece um conjunto de regras para escolher o remapeamento de bloco lógico lun com base em atributos simples. Os provedores de automação também podem alterar dinamicamente o mapeamento para gerenciamento de falhas ou desempenho.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**dicas automagéticas**
</dt> <dd>

Informações fornecidas a um provedor de automação para orientar a configuração de bloco lógico lun. As dicas incluem informações sobre a tolerância a falhas desejada, atomicidade física e padrão de acesso de E/S pretendido.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco básico**
</dt> <dd>

Um disco gerenciado pelo provedor de software mais simples possível. O provedor de disco básico dá suporte apenas a volumes que mapeiam diretamente para estruturas de dados de configuração de partição.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**Ligação**
</dt> <dd>

Selecionando para um conjunto de mapeamentos para recursos físicos.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**Converter**
</dt> <dd>

O processo de conversão de um disco básico em um disco dinâmico.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**Configuração**
</dt> <dd>

Uma coleção dos parâmetros operacionais que fornecem o mapeamento de um volume ou LUN para recursos físicos.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**Controlador**
</dt> <dd>

Um programa de software que contém a inteligência de runtime para um provedor de hardware.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**Disco**
</dt> <dd>

Um LUN de RAID de hardware ou disco físico. Os discos são destinos para carga de E/S de armazenamento em runtime; Plug and Play (PNP) não distingue entre JBOD e LUNs.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**placa de disco**
</dt> <dd>

Um subconjunto de um pacote usado para exportar ou importar volumes de um pacote.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**disk pack**
</dt> <dd>

Consulte *pack*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**Dirigir**
</dt> <dd>

Um eixo de disco físico dentro de um subsistema RAID de hardware. As unidades são vinculadas a LUNs pelo subsistema .

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinâmico**
</dt> <dd>

Um disco gerenciado por um provedor RAID de software com suporte para reconfiguração de volume flexível. Um disco dinâmico usa uma partição como um contêiner para volumes; não há nenhum mapeamento garantido.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configuração explícita**
</dt> <dd>

Uma configuração com os parâmetros, incluindo o tipo de volume e o layout exato, para uma coleção de volumes de destino.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**Exportação**
</dt> <dd>

O ato de mover uma placa de disco e todos os volumes contidos nesse disco para fora de um pacote.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**Extensão**
</dt> <dd>

Um intervalo contíguo de setores lógicos que contribuem para um único volume ou disco. Uma extensão também pode ser um intervalo de setores não alocados. Normalmente, um sistema de arquivos exibe os detalhes da extensão para um usuário final.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabela de partição GUID (GPT)**
</dt> <dd>

Estruturas usadas pelo firmware EFI. GPT é um dos dois formatos de dados de configuração de software de nível mais baixo usados pelo firmware da plataforma para localizar um sistema operacional inicializável ou outra imagem executável.

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**provedor de hardware**
</dt> <dd>

Uma coleção de software que é executada no host, um adaptador de barramento e, possivelmente, um subsistema de armazenamento externo que trabalha em conjunto para superfície e gerenciamento de LUNs RAID. Os provedores de hardware para a maioria dos subsistemas de armazenamento externos contêm apenas o modo de usuário, software baseado em host.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**Saúde**
</dt> <dd>

O status atual de gerenciamento de falhas de um volume ou lun.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**
</dt> <dd>

Adicionar temporariamente um volume plex a um volume.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**Importação**
</dt> <dd>

O ato de mover uma placa de disco e todos os seus volumes para um pacote existente.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**apenas um monte de discos (JBOD)**
</dt> <dd>

Uma coleção de eixos físicos sem o controle coordenado fornecido por um dispositivo RAID de hardware.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**número de bloco lógico (LBN)**
</dt> <dd>

A menor unidade de dados de armazenamento que pode ser abordada. O LBN é usado com protocolos de comando de E/S.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**mapeamento de bloco lógico**
</dt> <dd>

A transformação dos blocos lógicos apresentados a um provedor para aqueles expostos pelo provedor.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**LUN (número de unidade lógica)**
</dt> <dd>

Uma unidade de armazenamento fisicamente acessível conforme a superfície por um subsistema RAID de hardware. Esse termo também pode se referir ao identificador SCSI para a unidade de armazenamento.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Número do LUN**
</dt> <dd>

Um número que um provedor de hardware VDS atribui a um LUN em uma matriz. Isso não é o mesmo que o "número de unidade lógica" no endereço SCSI do disco.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**serviço de gerenciamento**
</dt> <dd>

Um programa de software que é executado conforme necessário para executar a configuração de volume, o monitoramento ou o tratamento de falhas.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**Mapeamento**
</dt> <dd>

Um volume que é exposto ao sistema operacional e tem um nome de volume associado (uma letra da unidade). Um volume é acessível por um sistema de arquivos.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**Máscara**
</dt> <dd>

Um disco não reconhecido pelo sistema operacional. Um disco pode ser mascarado pelo subsistema RAID de hardware, switch, SCSI RESERVE por outro host de computador ou software na pilha de disco.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**MBR (master boot record partitioning)**
</dt> <dd>

O MBR é um dos dois formatos de dados de configuração de software de nível mais baixo e é usado pelo firmware BIOS para localizar uma imagem inicializável do sistema operacional.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**Membro**
</dt> <dd>

Uma coleção de extensão de disco concatenada contida em mais um disco. Um disco pode contribuir com apenas um membro de um volume.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**Espelho**
</dt> <dd>

Um mapeamento de volume ou disco que mantém duas ou mais cópias de dados idênticas. O tipo de mapeamento também é chamado de RAID Nível 1.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**Pack**
</dt> <dd>

Uma coleção de volumes lógicos e discos subjacentes. Um pacote é a unidade de fechamento transitivo para um volume. Pacotes de disco dinâmicos e grupos de discos são termos para o mesmo item.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**faixa de paridade**
</dt> <dd>

Um mapeamento de volume ou disco que mantém informações de verificação de paridade, bem como dados. Cada fornecedor fornece o mapeamento exato e o esquema de proteção. Inclui RAID 3, 4, 5 e 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configuração parcialmente direcionada**
</dt> <dd>

Uma configuração de volume ou disco que não é totalmente explícita. O tipo de associação e uma coleção de recursos de destino são especificados; o layout real não é. A configuração parcialmente direcionada é a configuração de volume mais comum.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**Partição**
</dt> <dd>

Um intervalo contíguo de setores lógicos descrito por uma única entrada na estrutura MBR ou GPT. Em discos básicos, as partições correspondem diretamente a volumes simples. As estruturas de partição são compartilhadas entre o firmware da plataforma BIOS ou EFI e um sistema operacional ou outra imagem inicializável.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**Caminho**
</dt> <dd>

O caminho de acesso de um computador para um DISCO ou LUN de hardware externo.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**Plex**
</dt> <dd>

Um membro de um volume espelhado ou LUN.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**Porta**
</dt> <dd>

O ponto de extremidade de um caminho em um disco.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**matriz redundante de discos independentes (RAID)**
</dt> <dd>

Uma coleção de técnicas para gerenciar vários discos.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**serviço de runtime**
</dt> <dd>

Um programa de software que é executado em uma base de solicitação de E/S.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco simples**
</dt> <dd>

Um eixo que não está conectado a um controlador RAID de hardware. Consulte também JBOD (Apenas um monte de discos).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**provedor de software**
</dt> <dd>

Software baseado em host que expõe volumes lógicos e opera em discos. Um provedor de software inclui serviços de runtime de modo kernel, dados de configuração e serviços de gerenciamento de modo de usuário.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**Span**
</dt> <dd>

Um mapeamento linear de volume ou disco de várias extensão de disco ou unidade descontinuadas. As extensão podem estar em um ou mais eixos ou LUNs.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**Eixo**
</dt> <dd>

Uma unidade física de armazenamento em disco.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**Empilhamento**
</dt> <dd>

O ato de construir um volume ou LUN executando mais de uma operação de mapeamento de bloco lógico. Um exemplo é um volume espelhado em faixa. O empilhamento mais comum ocorre quando o RAID de software é usado entre LUNs construídos pelo RAID de hardware.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Listra**
</dt> <dd>

Um mapeamento de volume ou disco que intercala as extensão contíguas em vários volumes, discos ou unidades. Esse mapeamento também é chamado de RAID 0.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**Status**
</dt> <dd>

A disponibilidade atual de um volume, disco ou unidade.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**Subsistema**
</dt> <dd>

A insta instação do software do provedor de hardware. Um subsistema contém pelo menos um controlador e uma unidade. Se o subsistema for externo ao computador, um ou mais caminhos de rede conectarão o subsistema ao computador.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**estado de transição**
</dt> <dd>

Status do mapeamento lógico para físico que está passando por alterações.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco não reinicializado**
</dt> <dd>

Um disco que não é membro de um pacote.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco não máscarado**
</dt> <dd>

Um disco visível para o sistema operacional. O conteúdo de um disco sem máscara é visível para gerenciadores de volume de software, sistemas de arquivos e assim por diante.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**Volume**
</dt> <dd>

Várias extensão de disco vinculadas a um intervalo virtualmente contíguo de blocos lógicos. Um volume pode ser acessado por meio de uma letra da unidade, uma pasta montada ou um caminho GUID do volume.

</dd> </dl>

 

 
