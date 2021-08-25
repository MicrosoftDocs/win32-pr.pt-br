---
description: Depois de recuperar informações de instalação de um arquivo INF, há várias funções de manipulação de arquivos que você pode usar para instalar os arquivos listados em uma seção INF.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Instalando de um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e32780855e126eaaa38ae937a265951711662434e90ab0ffb425e2e4f4f6c42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867566"
---
# <a name="installing-from-an-inf-file"></a>Instalando de um arquivo INF

Depois de recuperar informações de instalação de um arquivo INF, há várias funções de manipulação de arquivos que você pode usar para instalar os arquivos listados em uma seção INF. Funções de baixo nível, como [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) e [**SetupInstallFileEx,**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) instalam um único arquivo.

Também há funções para lidar com arquivos compactados. A [**função SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) retorna informações sobre arquivos compactados. Essas informações podem ser usadas por [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) para copiar e, se necessário, expandir o arquivo.

Funções de  alto nível, como [**SetupInstallFromInfSection,**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)e [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) processam as operações de instalação em uma seção Instalar ou Serviço.  Desses, **SetupInstallFromInfSection** é o mais versátil porque pode executar qualquer  tipo de operação de instalação listada na seção Instalar de um arquivo INF. Isso inclui as operações de Registro e INI listadas nas linhas **AddReg**, **DelReg**, **UpdateInis** ou **UpdateIniField** de uma **seção Install.**

As [**funções SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) e [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona)  são  operações de fila de uma seção Instalar ou Serviço, respectivamente, para uma fila de arquivos existente. Observe que você deve chamar SetupInstallFromInfSection e SetupInstallServicesFromInfSection separadamente para operações e serviços de fila. Para obter mais informações, consulte [Filas de arquivos](file-queues.md).

Por outro lado, a [**função SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) cria e destrói sua própria fila interna. Um uso comum para **SetupInstallFromInfSection** é chamá-lo depois que todos os arquivos foram copiados com êxito para executar as transações de Registro e INI.

No Windows 2000, os arquivos DLL podem ser auto-registrados chamando [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) em um arquivo INF que inclui a **diretiva RegisterDlls** em sua seção **Instalar.** **SetupInstallFromInfSection** também pode registrar DLLs de 32 bits de um processo de 64 bits.

Em sistemas operacionais de 64 bits, [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pode ser chamado para executar operações na parte de 32 bits do Registro. Para adicionar uma chave do Registro à parte de 32 bits do Registro, inclua o sinalizador FLG \_ ADDREG \_ 32BITKEY na linha **AddReg** do INF. Para excluir uma chave do Registro somente na parte de 32 bits do Registro, inclua a chave FLG \_ DELREG \_ 32BITKEY na **linha DelReg.** Para definir ou limpar um valor binário somente na parte de 32 bits do Registro, inclua o FLG \_ BITREG \_ 32BITKEY na linha **BitReg.**

Além das funções listadas anteriormente, a API de Instalação inclui funções que enfileiam operações de instalação de arquivo, por arquivo ou por seção INF. Para obter mais informações, consulte [Filas de arquivos](file-queues.md).

 

 



