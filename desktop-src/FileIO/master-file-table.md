---
description: Todas as informações sobre um arquivo, incluindo seu tamanho, carimbos de data e hora, permissões e conteúdo de dados, são armazenadas em entradas MFT (tabela de arquivos mestre) ou no espaço fora do MFT descrito por entradas MFT.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Tabela de arquivos mestre (sistemas de arquivos locais)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fefec19906e6e2e2c67bbcabf8bd891ccc032b7e8d0882a3622011c324d11c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525636"
---
# <a name="master-file-table-local-file-systems"></a>Tabela de arquivos mestre (sistemas de arquivos locais)

O sistema de arquivos NTFS contém um arquivo chamado tabela *de arquivos mestre* ou MFT. Há pelo menos uma entrada no MFT para cada arquivo em um volume do sistema de arquivos NTFS, incluindo o próprio MFT. Todas as informações sobre um arquivo, incluindo seu tamanho, carimbos de data e hora, permissões e conteúdo de dados, são armazenadas em entradas MFT ou no espaço fora do MFT descrito pelas entradas MFT.

À medida que os arquivos são adicionados a um volume do sistema de arquivos NTFS, mais entradas são adicionadas ao MFT e o MFT aumenta de tamanho. Quando os arquivos são excluídos de um volume do sistema de arquivos NTFS, suas entradas MFT são marcadas como livres e podem ser reutilizados. No entanto, o espaço em disco que foi alocado para essas entradas não é realocado e o tamanho do MFT não diminui.

O sistema de arquivos NTFS reserva espaço para o MFT manter o MFT o mais contíguo possível à medida que cresce. O espaço reservado pelo sistema de arquivos NTFS para o MFT em cada volume é chamado de zona MFT. O espaço para arquivos e diretórios também é alocado desse espaço, mas somente depois que todo o espaço de volume fora da zona MFT foi alocado.

Dependendo do tamanho médio do arquivo e de outras variáveis, a zona MFT reservada ou o espaço não reservado no disco podem ser alocados primeiro à medida que o disco preenche a capacidade. Volumes com um pequeno número de arquivos relativamente grandes alocam o espaço não reservado primeiro, enquanto os volumes com um grande número de arquivos relativamente pequenos alocam a zona MFT primeiro. Em ambos os casos, a fragmentação do MFT começa a ocorrer quando uma região ou outra se torna totalmente alocada. Se o espaço não reservado for completamente alocado, o espaço para arquivos de usuário e diretórios será alocado da zona MFT. Se a zona MFT for completamente alocada, o espaço para novas entradas MFT será alocado do espaço não reservado.

O próprio MFT pode ser desfragmentado. Para reduzir a chance da zona MFT se tornar totalmente alocada antes que o processo de desfragmentação seja concluído, deixe o máximo de espaço no início da zona MFT possível antes de desfragmentar o volume. Se a zona MFT se tornar totalmente alocada antes da conclusão da desfragmentação, deverá haver espaço não alocado fora da zona MFT.

A zona MFT padrão é calculada e reservada pelo sistema quando ele monta o volume e é baseada no tamanho do volume. Você pode aumentar a zona MFT por meio da entrada do Registro detalhada no artigo Base de Dados de Conhecimento Microsoft 174619 , mas não pode tornar [a](https://support.microsoft.com/kb/174619)zona MFT padrão menor do que a calculada. Aumentar a zona MFT não diminui o espaço em disco que os usuários podem usar para arquivos de dados.

Para determinar o tamanho atual do MFT, analise a unidade do sistema de arquivos NTFS com o Desfragmentador de Disco e clique no botão **Exibir** Relatório. As estatísticas de unidade serão exibidas, incluindo o tamanho atual da MFT e o número de fragmentos. Você também pode obter o tamanho do MFT usando o código de [**controle FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data)

 

 
