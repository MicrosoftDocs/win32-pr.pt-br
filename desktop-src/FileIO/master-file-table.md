---
description: Todas as informações sobre um arquivo, incluindo seu tamanho, carimbos de data e hora, permissões e conteúdo de dados, são armazenadas em entradas de MFT (tabela de arquivos mestre) ou em espaço fora do MFT que é descrito pelas entradas de MFT.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Tabela de arquivos mestre (sistemas de arquivos locais)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260740c03e7b7e4ebe9c7e8ec90035431f6be649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769353"
---
# <a name="master-file-table-local-file-systems"></a>Tabela de arquivos mestre (sistemas de arquivos locais)

O sistema de arquivos NTFS contém um arquivo chamado *tabela de arquivos mestre* ou MFT. Há pelo menos uma entrada no MFT para cada arquivo em um volume do sistema de arquivos NTFS, incluindo o próprio MFT. Todas as informações sobre um arquivo, incluindo seu tamanho, carimbos de data e hora, permissões e conteúdo de dados, são armazenadas em entradas de MFT ou em espaço fora do MFT que é descrito pelas entradas de MFT.

À medida que os arquivos são adicionados a um volume do sistema de arquivos NTFS, mais entradas são adicionadas à MFT e o tamanho da MFT aumenta. Quando os arquivos são excluídos de um volume do sistema de arquivos NTFS, suas entradas de MFT são marcadas como livres e podem ser reutilizadas. No entanto, o espaço em disco que foi alocado para essas entradas não é realocado e o tamanho da MFT não diminui.

O sistema de arquivos NTFS reserva espaço para o MFT manter a MFT o mais contíguo possível à medida que ela aumenta. O espaço reservado pelo sistema de arquivos NTFS para o MFT em cada volume é chamado de zona MFT. O espaço para arquivos e diretórios também é alocado a partir desse espaço, mas somente depois que todo o espaço do volume fora da zona MFT tiver sido alocado.

Dependendo do tamanho médio do arquivo e de outras variáveis, a zona MFT reservada ou o espaço não reservado no disco pode ser alocado primeiro, pois o disco preenche a capacidade. Os volumes com um pequeno número de arquivos relativamente grandes alocarão o espaço não reservado primeiro, enquanto os volumes com um grande número de arquivos relativamente pequenos alocam a zona MFT primeiro. Em ambos os casos, a fragmentação do MFT começa a ocorrer quando uma região ou a outra se torna totalmente alocada. Se o espaço não reservado for completamente alocado, o espaço para os arquivos e diretórios do usuário será alocado da zona MFT. Se a zona MFT estiver completamente alocada, o espaço para novas entradas de MFT será alocado do espaço não reservado.

A própria MFT pode ser desfragmentada. Para reduzir a chance de que a zona MFT se torne totalmente alocada antes que o processo de desfragmentação seja concluído, deixe o máximo de espaço no início da zona MFT antes de desfragmentar o volume. Se a zona MFT for totalmente alocada antes da conclusão da desfragmentação, deverá haver espaço não alocado fora da zona MFT.

A zona MFT padrão é calculada e reservada pelo sistema quando ele monta o volume e é baseada no tamanho do volume. Você pode aumentar a zona MFT por meio da entrada de registro detalhada no [artigo 174619 da base de dados de conhecimento Microsoft](https://support.microsoft.com/kb/174619), mas não é possível tornar a zona MFT padrão menor do que a calculada. O aumento da zona MFT não diminui o espaço em disco que os usuários podem usar para arquivos de dados.

Para determinar o tamanho atual do MFT, analise a unidade do sistema de arquivos NTFS com o Desfragmentador de disco e clique no botão **Exibir relatório** . As estatísticas da unidade serão exibidas, incluindo o tamanho atual do MFT e o número de fragmentos. Você também pode obter o tamanho do MFT usando o fsctl obter o código de controle de [**\_ \_ \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data) .

 

 
