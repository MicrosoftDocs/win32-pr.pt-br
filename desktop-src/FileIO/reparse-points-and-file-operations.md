---
description: Descreve como os pontos de nova análise permitem o comportamento do sistema de arquivos que faz parte do comportamento que a maioria dos desenvolvedores do Windows espera.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Pontos de nova análise e operações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170962"
---
# <a name="reparse-points-and-file-operations"></a>Pontos de nova análise e operações de arquivo

Os *pontos de nova análise* habilitam o comportamento do sistema de arquivos que faz parte do comportamento em que a maioria dos desenvolvedores do Windows pode estar acostumado, portanto, estar ciente desses comportamentos ao escrever aplicativos que manipulam arquivos é vital para aplicativos robustos e confiáveis destinados a acessar sistemas de arquivos que dão suporte a pontos de nova análise. A extensão dessas considerações dependerá da implementação específica e do comportamento do filtro do sistema de arquivos associado de um determinado ponto de nova análise, que pode ser definido pelo usuário. Para obter mais informações, consulte [pontos de nova análise](reparse-points.md).

Considere os exemplos a seguir sobre as implementações de ponto de nova análise de NTFS, que incluem pastas montadas, arquivos vinculados e o servidor de armazenamento remoto da Microsoft:

-   Os aplicativos de backup que usam [fluxos de arquivos](file-streams.md) devem especificar **\_ \_ dados de nova análise de backup** na estrutura de [**\_ \_ ID de fluxo do Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) ao fazer backup de arquivos com pontos de nova análise.
-   Os aplicativos que usam a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) devem especificar o sinalizador do **sinalizador de arquivo \_ \_ abrir \_ \_ ponto de nova análise** ao abrir o arquivo se ele for um ponto de nova análise. Para obter mais informações, consulte [criando e abrindo arquivos](creating-and-opening-files.md).
-   O processo de [desfragmentação de arquivos](defragmenting-files.md) requer tratamento especial para pontos de nova análise.
-   Os aplicativos de detecção de vírus devem procurar pontos de nova análise que indiquem arquivos vinculados.
-   A maioria dos aplicativos deve executar ações especiais para arquivos que foram movidos para o armazenamento de longo prazo, se apenas notificar o usuário de que pode levar algum tempo para recuperar o arquivo.
-   A função [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) abrirá o arquivo ou o ponto de nova análise, dependendo do uso do sinalizador de **\_ \_ \_ \_ ponto de nova análise aberto do sinalizador de arquivo** .
-   Links simbólicos, como pontos de nova análise, têm determinadas [considerações de programação](symbolic-link-programming-considerations.md) específicas para eles.
-   As atividades de gerenciamento de volume para ler os registros do diário de alterações do USN (número de sequência de atualização) exigem tratamento especial para pontos de nova análise ao usar o [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e ler estruturas de [**\_ dados do \_ diário \_ de USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Determinando se um diretório é uma pasta montada](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[Criando pastas montadas](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[Efeitos de link simbólico em funções de sistemas de arquivos](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
