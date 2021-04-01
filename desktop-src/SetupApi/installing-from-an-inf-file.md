---
description: Depois de recuperar as informações de instalação de um arquivo INF, há várias funções de manipulação de arquivos que você pode usar para instalar os arquivos listados em uma seção INF.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Instalando a partir de um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc3642edfb7abc2864c2c0784c79fbb21612fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829298"
---
# <a name="installing-from-an-inf-file"></a>Instalando a partir de um arquivo INF

Depois de recuperar as informações de instalação de um arquivo INF, há várias funções de manipulação de arquivos que você pode usar para instalar os arquivos listados em uma seção INF. Funções de nível baixo, como [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) e [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) , instalam um único arquivo.

Há também funções para lidar com arquivos compactados. A função [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) retorna informações sobre arquivos compactados. Essas informações podem ser usadas pelo [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) para copiar e, se necessário, expandir o arquivo.

Funções de alto nível, como [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)e [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) , processam as operações de instalação em uma seção de **instalação** ou **serviço** . Desses, o **SetupInstallFromInfSection** é o mais versátil porque ele pode executar qualquer tipo de operação de instalação listada na seção de **instalação** de um arquivo inf. Isso inclui as operações de registro e INI listadas nas linhas **AddReg**, **DelReg**, **UpdateInis** ou **UpdateIniField** de uma seção de **instalação** .

As funções [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) e [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) enfileiram operações de uma seção de **instalação** ou de **serviço** , respectivamente, para uma fila de arquivos existente. Observe que você deve chamar SetupInstallFromInfSection e SetupInstallServicesFromInfSection separadamente para serviços e operações de fila. Para obter mais informações, consulte [filas de arquivos](file-queues.md).

Por outro lado, a função [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) cria e destrói sua própria fila interna. Um uso comum para **SetupInstallFromInfSection** é chamá-lo depois que todos os arquivos tiverem sido copiados com êxito para executar as transações de registro e ini.

No Windows 2000, os arquivos DLL podem ser registrados automaticamente chamando [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) em um arquivo inf que inclui a diretiva **RegisterDlls** em sua seção de **instalação** . **SetupInstallFromInfSection** também pode registrar automaticamente DLLs de 32 bits de um processo de 64 bits.

Em sistemas operacionais de 64 bits, [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pode ser chamado para executar operações na parte de 32 bits do registro. Para adicionar uma chave do registro à parte de 32 bits do registro, inclua o sinalizador FLG \_ ADDREG \_ 32BITKEY na linha **ADDREG** do inf. Para excluir uma chave do registro somente na parte de 32 bits do registro, inclua a chave FLG \_ DELREG \_ 32BITKEY na linha **DELREG** . Para definir ou limpar um valor binário somente na parte de 32 bits do registro, inclua FLG \_ BITREG \_ 32BITKEY na linha **BITREG** .

Além das funções listadas anteriormente, a API de instalação inclui funções que enfileiram operações de instalação de arquivo, seja por arquivo ou pela seção INF. Para obter mais informações, consulte [filas de arquivos](file-queues.md).

 

 



