---
description: A extensão de endereço físico (PAE) é um recurso de processador que permite que os processadores x86 acessem mais de 4 GB de memória física em versões compatíveis do Windows.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Extensão de endereço físico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2fd9193a19d228f26a09865086c59b65c0019b3cee42142dfd27188eff30169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979716"
---
# <a name="physical-address-extension"></a>Extensão de endereço físico

A extensão de endereço físico (PAE) é um recurso de processador que permite que os processadores x86 acessem mais de 4 GB de memória física em versões compatíveis do Windows. determinadas versões de 32 bits do Windows Server em execução em sistemas baseados em x86 podem usar o PAE para acessar até 64 gb ou 128 gb de memória física, dependendo do tamanho do endereço físico do processador. para obter detalhes, consulte [limites de memória para versões de Windows](memory-limits-for-windows-releases.md).

As arquiteturas de processador Intel Itanium e x64 podem acessar mais de 4 GB de memória física nativamente e, portanto, não fornecem o equivalente de PAE. o PAE é usado somente pelas versões de 32 bits do Windows em execução em sistemas baseados em x86.

Com o PAE, o sistema operacional passa da conversão de endereços linear de dois níveis para a conversão de endereços de três níveis. Em vez de um endereço linear que está sendo dividido em três campos separados para indexação em tabelas de memória, ele é dividido em quatro campos separados: um Telebit de 2 bits, um bitfields-bit de 2 9 bits e um campo de linhas de 12 bits que corresponde ao tamanho da página implementado pela arquitetura Intel (4 KB). O tamanho das PTEs (entradas de tabela de página) e PDEs (entradas de diretório de página) no modo PAE aumentou de 32 para 64 bits. Os bits adicionais permitem que um sistema operacional PTE ou PDE referencie a memória física acima de 4 GB.

no Windows de 32 bits em execução em sistemas baseados em x64, o PAE também permite vários recursos avançados de sistema e processador, incluindo a DEP ( [prevenção de execução de dados](data-execution-prevention.md) ) habilitada para hardware, o [NUMA (acesso não uniforme à memória](../procthread/numa-support.md)) e a capacidade de adicionar memória a um sistema enquanto ele está em execução (adição de memória a quente).

O PAE não altera a quantidade de espaço de endereço virtual disponível para um processo. cada processo em execução no Windows de 32 bits ainda está limitado a um espaço de endereço virtual de 4 GB.

## <a name="system-support-for-pae"></a>Suporte do sistema para PAE

o PAE tem suporte apenas nas seguintes versões de 32 bits do Windows em execução em sistemas baseados em x86:

-   Windows 7 (somente 32 bits)
-   Windows Servidor 2008 (somente 32 bits)
-   Windows Vista (somente 32 bits)
-   Windows Servidor 2003 (somente 32 bits)
-   Windows XP (somente 32 bits)

## <a name="enabling-pae"></a>Habilitando PAE

Windows automaticamente habilita o PAE se a dep estiver habilitada em um computador com suporte para DEP habilitada para hardware ou se o computador estiver configurado para adicionar dispositivos de memória a quente em intervalos de memória além de 4 GB. Se o computador não oferecer suporte a DEP habilitada para hardware ou não estiver configurado para adicionar dispositivos de memória a quente em intervalos de memória além de 4 GB, a PAE deverá ser habilitada explicitamente.

Para habilitar explicitamente o PAE, use o seguinte comando [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) para definir a opção de entrada de inicialização de **PAE** :

 **bcdedit/set \[ {ID} \] PAE ForceEnable**  


SE a DEP estiver habilitada, o PAE não poderá ser desabilitado. Use os seguintes comandos [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) para desabilitar o DEP e o PAE:

 **bcdedit/set \[ {ID} \] NX AlwaysOff**  
**bcdedit/set \[ {ID} \] PAE ForceDisable**  


**Windows Server 2003 e Windows XP:** Para habilitar o PAE, use a opção **/PAE** no arquivo de [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) . Para desabilitar o PAE, use a opção **/NOPAE** Para desabilitar o DEP, use a opção **/Execute** .

## <a name="comparing-pae-and-other-large-memory-support"></a>Comparando o PAE e outros suporte de memória grande

PAE, [ajuste de 4 gigabytes](4-gigabyte-tuning.md) (4GT) e [extensões de janelas de endereço](address-windowing-extensions.md) (AWE) servem para diferentes finalidades e podem ser usados independentemente um do outro:

-   O PAE permite que o sistema operacional acesse e use mais de 4 GB de memória física.
-   4GT aumenta a parte do espaço de endereço virtual disponível para um processo de 2 GB para até 3 GB.
-   O AWE é um conjunto de APIs que permite a um processo alocar memória física não paginável e, em seguida, mapear dinamicamente partes dessa memória para o espaço de endereço virtual do processo.

Quando não há nenhum 4GT nem AWE sendo usado, a quantidade de memória física que um único processo de 32 bits pode usar é limitada pelo tamanho de seu espaço de endereço (2 GB). Nesse caso, um sistema habilitado para PAE ainda pode usar mais de 4 GB de RAM para executar vários processos ao mesmo tempo ou para armazenar em cache os dados de arquivo na memória.

4GT pode ser usado com ou sem PAE. no entanto, algumas versões do Windows limitam a quantidade máxima de memória física que pode ter suporte quando 4gt é usado. Em tais sistemas, a inicialização com 4GT habilitado faz com que o sistema operacional ignore qualquer memória que ultrapasse o limite.

O AWE não requer PAE ou 4GT, mas geralmente é usado junto com o PAE para alocar mais de 4 GB de memória física a partir de um único processo de 32 bits.

## <a name="related-topics"></a>Tópicos relacionados



[**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[Referência técnica do PAE x86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
