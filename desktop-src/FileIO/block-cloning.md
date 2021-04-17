---
description: Uma operação de clonagem de bloco instrui o sistema de arquivos a copiar um intervalo de bytes de arquivo em nome de um aplicativo.
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: Bloquear clonagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33aa1c1eee693b6ed4b502aedc6da6176ece3e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506179"
---
# <a name="block-cloning"></a>Bloquear clonagem

Uma operação de *clonagem de bloco* instrui o sistema de arquivos a copiar um intervalo de bytes de arquivo em nome de um aplicativo. O arquivo de destino pode ser igual ou diferente do arquivo de origem.

Um sistema de arquivos gerencia os mapeamentos de [clusters e extensões](clusters-and-extents.md), e pode ser capaz de realizar a cópia alterando o número do cluster virtual (VCN) para mapeamentos de número de cluster lógico (LCN) como uma operação de metadados de baixo custo, em vez de ler e gravar os dados de arquivo subjacentes. Isso permite que a cópia seja concluída mais rapidamente e gera menos e/s para o armazenamento subjacente. Além disso, vários arquivos podem agora compartilhar clusters lógicos após o clone do bloco, economizando capacidade, não armazenando clusters idênticos várias vezes no disco.

Uma operação de clonagem de bloco não interrompe o isolamento fornecido entre os arquivos. Após a conclusão de um clone de bloco, as gravações no arquivo de origem não aparecem no destino ou vice-versa.

A clonagem de bloco está disponível apenas no tipo de [sistema de arquivos ReFS](/windows/desktop/w8cookbook/resilient-file-system--refs-) a partir do Windows Server 2016.

## <a name="block-cloning-on-refs"></a>Bloquear clonagem em ReFS

O ReFS no Windows Server 2016 implementa a clonagem de bloco ao remapear clusters lógicos (ou seja, locais físicos em um volume) da região de origem para a região de destino. Em seguida, ele usa um mecanismo de alocação na gravação para garantir o isolamento entre essas regiões. As regiões de origem e de destino podem estar nos mesmos arquivos, ou diferentes.

Essa implementação requer que os deslocamentos de arquivo inicial e final sejam alinhados aos limites do cluster. No ReFS no Windows Server 2016, os clusters têm 4 KB de tamanho por padrão, mas, opcionalmente, podem ser definidos como 64 KB. O tamanho do cluster é um conjunto de parâmetros em todo o volume no momento do formato.

## <a name="restrictions-and-remarks"></a>Restrições e comentários

-   As regiões de origem e de destino devem começar e terminar em um limite de cluster.
-   A região clonada deve ter menos de 4 GB.
-   A região de destino não deve ultrapassar o fim do arquivo. Se o aplicativo quiser estender o destino com dados clonados, ele deverá primeiro chamar [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).
-   Se as regiões de origem e de destino estiverem no mesmo arquivo, elas não deverão se sobrepor. (O aplicativo pode continuar dividindo a operação bloquear clonagem em vários clones de bloco que não se sobrepõem mais.)
-   Os arquivos de origem e de destino devem estar no mesmo volume do ReFS.
-   Os arquivos de origem e destino devem ter a mesma configuração de [**fluxos de integridade**](file-attribute-constants.md) (ou seja, os fluxos de integridade devem ser habilitados em ambos os arquivos ou desabilitados em ambos os arquivos).
-   Se o arquivo de origem for esparso, o arquivo de destino também deverá ser esparso.
-   A operação bloquear clonagem interromperá bloqueios oportunistas compartilhados (também conhecidos como [bloqueios oportunistas de nível 2](types-of-opportunistic-locks.md)).
-   O volume ReFS deve ter sido formatado com o Windows Server 2016 e, se o clustering de failover do Windows estiver em uso, o nível funcional de clustering deverá ter sido o Windows Server 2016 ou posterior no formato de hora.

## <a name="example"></a>Exemplo

Suponha que tenhamos dois arquivos, X e Y, onde cada arquivo é composto por 3 regiões distintas. Cada região de arquivo é armazenada em uma região distinta do volume. O sistema de arquivos armazena o conhecimento de que cada uma dessas regiões de volume é referenciada em uma região de arquivo:

![antes do clone](images/before-clone.png)

Agora suponha que um aplicativo emita uma operação de clonagem de bloco do arquivo X, nas regiões de arquivo A e B, para o arquivo Y no deslocamento onde E atualmente é. O seguinte estado do sistema de arquivos resultaria:

![após o clone](images/after-clone.png)

Os dados nas regiões A e B eram efetivamente duplicados do arquivo X para o arquivo Y alterando o VCN para mapeamentos de LCN dentro do volume ReFS. As extensões de disco nas regiões A e B não foram lidas, nem as extensões de disco que faziam o backup das regiões antigas e e F foram substituídas durante a operação.

Os arquivos X e Y agora compartilham clusters lógicos no disco. Isso é refletido nas contagens de referência mostradas na tabela. O compartilhamento resulta em um consumo de capacidade de volume menor do que se as regiões A e B estivessem duplicadas no volume subjacente.

Agora, suponha que o aplicativo substitua a região A no arquivo X. ReFS faz uma cópia duplicada de A, que agora chamamos de G. ReFS e, em seguida, mapeia G no arquivo X e aplica a modificação. Isso garante que o isolamento entre os arquivos seja preservado. As contagens de referência são atualizadas adequadamente:

![Depois de modificar a gravação](images/after-modifying-write.png)

Após a gravação de modificação, a região B ainda é compartilhada no disco. Observe que, se a região A fosse maior que um cluster, somente o cluster modificado teria sido duplicado, e a parte restante continuaria compartilhada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**dados de extensões DUPLICAdas \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**FSCTL \_ \_ extensões duplicadas \_ para o \_ arquivo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
