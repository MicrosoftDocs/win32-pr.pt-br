---
description: A tabela de arquivos mestre (MFT) armazena as informações necessárias para recuperar arquivos de uma partição NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Tabela de arquivos mestre (notas do desenvolvedor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920148"
---
# <a name="master-file-table"></a>Tabela de arquivos mestre

\[Este documento se aplica somente à versão 3 de volumes NTFS.\]

A tabela de arquivos mestre (MFT) armazena as informações necessárias para recuperar arquivos de uma partição NTFS.

Um arquivo pode ter um ou mais registros de MFT e pode conter um ou mais atributos. No NTFS, uma referência de arquivo é a referência de segmento de MFT do registro de arquivo base. Para obter mais informações, [**consulte \_ \_ referência de segmento de MFT**](mft-segment-reference.md).

A MFT contém segmentos de registro de arquivo; os primeiros 16 deles são reservados para arquivos especiais, como o seguinte:

-   0: MFT ($Mft)
-   5: diretório raiz ( \\ )
-   6: arquivo de alocação de cluster de volume ($Bitmap)
-   8: arquivo de cluster inválido ($BadClus)

Cada segmento de registro de arquivo começa com um cabeçalho de segmento de registro de arquivo. Para obter mais informações, [**consulte \_ \_ \_ cabeçalho de segmento de registro de arquivo**](file-record-segment-header.md). Cada segmento de registro de arquivo é seguido por um ou mais atributos. Cada atributo começa com um cabeçalho de registro de atributo. Para obter mais informações, [**consulte \_ \_ cabeçalho de registro de atributo**](attribute-record-header.md). O registro de atributo inclui o tipo de atributo (como $DATA ou $BITMAP), um nome opcional e o valor do atributo. O fluxo de dados do usuário é um atributo, assim como todos os fluxos. A lista de atributos é encerrada com 0xFFFFFFFF ($END).

Veja a seguir alguns exemplos de atributos.

-   O arquivo de $Mft contém um atributo de $DATA sem nome que é a sequência de segmentos de registro de MFT, em ordem.
-   O arquivo de $Mft contém um atributo de $BITMAP sem nome que indica quais registros de MFT estão em uso.
-   O arquivo de $Bitmap contém um atributo de $DATA sem nome que indica quais clusters estão em uso.
-   O arquivo de $BadClus contém um atributo de $DATA chamado $BAD que contém uma entrada que corresponde a cada cluster defeituoso.

Quando não há mais espaço para armazenar atributos no segmento de registro de arquivo, segmentos de registro de arquivo adicionais são alocados e inseridos no primeiro segmento (ou base) de registro de arquivo em um atributo chamado lista de atributos. A lista de atributos indica onde cada atributo associado ao arquivo pode ser encontrado. Isso inclui todos os atributos no registro de arquivo base, exceto para a própria lista de atributos. Para obter mais informações, consulte a [**\_ \_ entrada da lista de atributos**](attribute-list-entry.md).

As estruturas relacionadas ao MFT incluem o seguinte:

-   [**\_entrada da lista de atributos \_**](attribute-list-entry.md)
-   [**\_cabeçalho de registro de atributo \_**](attribute-record-header.md)
-   [**nome do arquivo \_**](file-name.md)
-   [**\_cabeçalho de \_ segmento de registro de arquivo \_**](file-record-segment-header.md)
-   [**\_referência de segmento de MFT \_**](mft-segment-reference.md)
-   [**cabeçalho de vários \_ setores \_**](multi-sector-header.md)
-   [**\_informações padrão**](standard-information.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência técnica do NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
