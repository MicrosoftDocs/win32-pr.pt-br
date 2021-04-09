---
description: O mecanismo direcionado de destino permite que os gravadores remapeiem arquivos no momento da restauração.
ms.assetid: c0b4ab26-2bb6-4b0f-b837-01057983b49b
title: Trabalhando com destinos direcionados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd2e15ec873b87030a2d01be69d2c3e5f95a193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010504"
---
# <a name="working-with-directed-targets"></a>Trabalhando com destinos direcionados

O mecanismo [*direcionado de destino*](vssgloss-d.md) permite que os gravadores remapeiem arquivos no momento da restauração. Isso permite que os gravadores façam o seguinte:

-   Especifique novos locais de destino (análogo ao [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)) de um solicitante.
-   Recupere espaço em disco restaurando apenas as partes necessárias de um arquivo para o disco, especialmente quando foi feito o backup de um arquivo usando o mecanismo de [*arquivo parcial*](vssgloss-p.md) .
-   Altere o formato de arquivo para atender às necessidades atuais.

Qualquer arquivo a ser usado com uma operação direcionada de destino deve ter um [*destino de restauração*](vssgloss-r.md) do VSS \_ RT \_ direcionado.

Depois de estabelecer que um solicitante pode dar suporte a uma operação direcionada de destino, um gravador (ao manipular o evento de [**Prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ) usa [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) para a instância do [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente ao componente que gerencia o arquivo (ou o componente que define o conjunto de componentes que contém o arquivo) para definir como o arquivo deve ser remapeado na restauração.

Ao usar [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget), os gravadores especificam o nome do arquivo e o caminho usados para fazer backup do arquivo, o nome do arquivo e o caminho de seu destino de restauração (esses valores podem ser iguais aos do caminho e do nome do arquivo original) e os intervalos de arquivos de origem e de destino.

Assim como acontece com as operações de arquivo parcial, as listas de intervalos são pares de deslocamentos para o backup do arquivo (em bytes) e o comprimento da seção a ser restaurada (em bytes), o deslocamento e o comprimento que estão sendo separados por dois-pontos e cada par separado por uma vírgula: *Offset1 ***:**_Length1_*_,_* * Offset2 ***:**_Length2_. Cada valor é um inteiro de 64 bits no formato hexadecimal ou Decimal.

Se um gravador precisar usar o mecanismo direcionado de destino para fazer com que o solicitante restaure um arquivo para um novo local, ele teria chamado [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) com o nome e o caminho do arquivo original e o novo nome e caminho do arquivo e especifique os intervalos de destino de origem com um deslocamento zero e um comprimento igual ao de todo o tamanho do arquivo.

Por exemplo, se um gravador precisar ter um arquivo de 200 k, C: \\ WriterData \\ index. dat, restaurado como C: \\ WriterData \\ OldIndex. dat, a cadeia de caracteres de intervalo de origem e de destino seria "**0:204880**".

Para remapear um arquivo de backup grande e parcialmente feito, o solicitante usará o intervalo de origem usado para fazer backup do arquivo e um intervalo de destino que reduzirá o tamanho do arquivo. As informações do intervalo de origem podem ser obtidas usando [**IVssComponent:: Getparcialfile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) para a instância de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente ao componente que gerencia o arquivo (ou o componente que define o conjunto de componentes que contém o arquivo).

Se o arquivo com backup parcial era inicialmente um arquivo grande cujo cabeçalho, bytes 64-512, contém uma contagem de registros e outras informações atualizadas com frequência e cujos dados mais recentes são encontrados nos últimos 65536 bytes do arquivo — bytes 0x1239E8577A a 0x1239E7577A, um gravador poderia especificar uma lista de intervalos de origem como a cadeia de caracteres "**64:448, 0x1239E8577A: 65536**."

Se o gravador quisesse remapear o arquivo restaurado para conter apenas o cabeçalho e os dados mais recentes, a lista de intervalos pode ser a cadeia de caracteres "**0:488488:65536**".

Antes de realmente executar uma operação de restauração, um solicitante deve verificar se algum arquivo requer suporte direcionado a destino.

Para fazer isso, o solicitante primeiro itera sobre os gravadores com componentes armazenados em seu documento de componentes de backup usando [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

Em seguida, a interface [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) é usada para retornar instâncias da interface [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) , que fornece os métodos [**IVssWriterComponentsExt:: GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) que permitem que o solicitante obtenha as instâncias de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Isso permite que um solicitante obtenha candidatos direcionados ao destino usando [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget) para a instância de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondente ao componente que gerencia o arquivo (ou o componente que define o conjunto de componentes que contém o arquivo).

 

 
