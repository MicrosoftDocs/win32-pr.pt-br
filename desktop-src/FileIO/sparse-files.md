---
description: A compactação de arquivos que contêm principalmente zeros faz uso eficiente do espaço em disco.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: Arquivos esparsos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb89a8fd3e8c067d5328756e57d511d4c38d615f2bb19c579208462c3f5bdbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951045"
---
# <a name="sparse-files"></a>Arquivos esparsos

Um arquivo no qual grande parte dos dados é zeros é dito que contém um *conjunto de dados esparso*. Arquivos como esses normalmente são muito grandes, por exemplo, um arquivo que contém dados de imagem a serem processados ou uma matriz em um banco de dados de alta velocidade. O problema com arquivos que contêm conjuntos de dados esparsos é que a maioria do arquivo não contém dados úteis e, por isso, eles são um uso ineficiente do espaço em disco.

A compactação de arquivo no sistema de arquivos NTFS é uma solução parcial para o problema. Todos os dados no arquivo que não são gravados explicitamente são definidos explicitamente como zero. A compactação de arquivo compacta esses intervalos de zeros. No entanto, uma desvantagem da compactação de arquivo é que o tempo de acesso pode aumentar devido à compactação e à descompactação de dados.

O suporte para arquivos esparsos é introduzido no sistema de arquivos NTFS como outra maneira de tornar o uso de espaço em disco mais eficiente. Quando a funcionalidade de arquivo esparso está habilitada, o sistema não aloca espaço de unidade de disco rígido para um arquivo, exceto em regiões em que ele contém dados diferentes de zero. Quando uma operação de gravação é tentada em que uma grande quantidade de dados no buffer é zeros, os zeros não são gravados no arquivo. Em vez disso, o sistema de arquivos cria uma lista interna que contém os locais dos zeros no arquivo e essa lista é consultada durante todas as operações de leitura. Quando uma operação de leitura é executada em áreas do arquivo em que zeros estavam localizados, o sistema de arquivos retorna o número apropriado de zeros no buffer alocado para a operação de leitura. Dessa forma, a manutenção do arquivo esparso é transparente para todos os processos que o acessam e é mais eficiente do que a compactação para esse cenário específico.

O valor de dados padrão de um arquivo esparso é zero; no entanto, ele pode ser definido como outros valores.

Para obter mais informações sobre arquivos esparsos, consulte os tópicos a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                     | Descrição                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Operações de arquivo esparsas](sparse-file-operations.md)<br/>                           | Determine se um sistema de arquivos dá suporte a arquivos esparsos chamando a função GetVolumeInformation.<br/>                                                                                |
| [Obtendo o tamanho de um arquivo esparso](obtaining-the-size-of-a-sparse-file.md)<br/> | Obter o tamanho alocado ou o tamanho total de um arquivo usando a [**função GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) ou [**GetFileSize.**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)<br/> |
| [Arquivos esparsos e cotas de disco](sparse-files-and-disk-quota.md)<br/>                | Um arquivo esparso afeta as cotas de usuário pelo tamanho nominal do arquivo, não pela quantidade real alocada de espaço em disco.<br/>                                                                  |



 

 

 




