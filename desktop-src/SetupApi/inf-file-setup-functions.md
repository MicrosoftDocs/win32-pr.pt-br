---
description: As seguintes funções de API de instalação são usadas com arquivos INF.
ms.assetid: fb4263fc-5f59-460a-a7d9-93f10729c02a
title: Funções de configuração de arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24944f19938217d40ff4a7eaebbfb638c26e4afb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750424"
---
# <a name="inf-file-setup-functions"></a>Funções de configuração de arquivo INF

As seguintes funções de API de instalação são usadas com arquivos INF.



| Função                                                                         | Descrição                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)                                   | Libera recursos e fecha o identificador INF.                                                                                                                                                             |
| [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)                   | Copia um arquivo e, se necessário, o descompacta.                                                                                                                                                      |
| [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                                 | Localiza a primeira linha em uma seção de um arquivo INF ou, se uma chave for especificada, a primeira linha que corresponde a essa chave. Ele atualiza o membro de **linha** de uma estrutura [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) . |
| [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                                   | Retorna a próxima linha de uma seção relativa ao membro de **linha** da estrutura [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) especificada.                                                                    |
| [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                         | Retorna a próxima linha de uma seção em relação ao membro de **linha** do [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) especificado que corresponde a uma chave especificada.                                                 |
| [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                               | Recupera dados de uma linha cujos campos estão em formato binário.                                                                                                                                          |
| [**SetupGetFieldCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)                                 | Retorna o número de campos em uma linha.                                                                                                                                                                |
| [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)               | Recupera informações de compactação de arquivo de um arquivo INF.                                                                                                                                               |
| [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)                               | Obtém uma lista dos tipos de arquivos INF em um diretório especificado.                                                                                                                                        |
| [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                         | Retorna informações sobre um arquivo INF (por membro de **linha** de um [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) ou nome de arquivo).                                                                                     |
| [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                     | Retorna o campo de inteiro especificado de uma linha em um arquivo INF.                                                                                                                                          |
| [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                               | Atualiza o membro de **linha** de um [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) para a linha em um índice especificado na seção especificada.                                                                     |
| [**SetupGetLineCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)                                   | Retorna o número de linhas na seção especificada.                                                                                                                                                  |
| [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                     | Recupera o conteúdo de uma linha especificada de um arquivo INF.                                                                                                                                            |
| [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                             | Retorna uma lista de cadeias de caracteres, começando no campo especificado de uma linha em um arquivo INF.                                                                                                                   |
| [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)                 | Obtém o ordinal e o caminho do disco de origem (em relação à raiz de origem) em que o arquivo de origem está localizado                                                                                                       |
| [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                         | Obtém o tamanho do arquivo de um arquivo de origem individual ou uma seção de **arquivos de cópia** de um arquivo inf.                                                                                                           |
| [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                                 | Recupera o caminho, o arquivo de marca ou a descrição de uma origem.                                                                                                                                             |
| [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                               | Retorna o campo de cadeia de caracteres especificado de uma linha em um arquivo INF.                                                                                                                                           |
| [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                                 | Obtém o caminho de destino para uma seção de **arquivos de cópia** em um arquivo inf.                                                                                                                                      |
| [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)                                     | Instala um arquivo.                                                                                                                                                                                       |
| [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)                                 | Instala um arquivo e retorna uma variável indicando se o arquivo estava em uso ou não.                                                                                                                  |
| [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)       | Enfileira todos os arquivos especificados nas seções **copiar** arquivos, **Excluir arquivos** e **renomear arquivos** listados por uma seção **instalar** .                                                       |
| [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)                 | Executa as diretivas especificadas em uma seção de **instalação** de arquivo inf.                                                                                                                                  |
| [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) | Executa operações de instalação e exclusão de serviço conforme especificado em uma seção de **serviço** de um arquivo inf.                                                                                            |
| [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)                         | Abre um arquivo INF e o anexa a um identificador INF existente.                                                                                                                                             |
| [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)                                     | Abre um arquivo INF e retorna um identificador para ele.                                                                                                                                                          |
| [**SetupOpenMasterInf**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)                                 | Abre o arquivo INF que contém informações de arquivo e de layout para arquivos enviados com o sistema.                                                                                                        |
| [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)             | Consulta uma estrutura de informações INF sobre seus nomes de arquivo INF associados.                                                                                                                               |
| [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)       | Consulta uma estrutura de informações INF para obter informações de versão em um de seus arquivos INF de constituintes.                                                                                                      |
| [**SetupSetDirectoryId**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)                               | Associa um novo identificador de diretório a um diretório específico.                                                                                                                                     |



 

 

 



