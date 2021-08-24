---
title: Interfaces BITS
description: Use as interfaces Serviço de Transferência Inteligente em Segundo Plano bits (BITS) a seguir para transferir arquivos e monitorar trabalhos dentro da fila de transferência.
ms.assetid: 72668c9b-e6f3-4f3f-9d4b-50d930d1889d
ms.topic: article
ms.date: 01/08/2019
ms.openlocfilehash: 0edd4229e76a85767689427cfccd6cb38aa11c0e54345053ce10d1a99fc1fde8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529066"
---
# <a name="bits-interfaces"></a>Interfaces BITS

Use as seguintes interfaces Serviço de Transferência Inteligente em Segundo Plano bits (BITS) para [transferir arquivos e monitorar trabalhos](using-bits.md) dentro da fila de transferência.

| Interface | Descrição |
|-|-|
| [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) | Os clientes implementam a interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) para receber uma notificação de que um trabalho foi concluído, foi modificado ou está com erro. |
| [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) | Os clientes implementam a interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) para receber uma notificação de que um arquivo concluiu o download. |
| [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) | Os clientes implementam a interface [**IBackgroundCopyCallback3**](/windows/desktop/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3) para receber uma notificação de que os intervalos de um arquivo concluíram o download. |
| [**IBackgroundCopyError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) | Recupera detalhes de um erro de trabalho. |
| [**IBackgroundCopyFile**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyfile) | Recupera os nomes de arquivo local e remoto de uma solicitação de transferência de arquivo no trabalho e seu progresso. |
| [**IBackgroundCopyFile2**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2) | Especifica um novo nome remoto para o arquivo e recupera a lista de intervalos a baixar. |
| [**IBackgroundCopyFile3**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3) | Valida o arquivo para que os pares possam solicitar seu conteúdo e recupere o nome do arquivo temporário. |
| [**IBackgroundCopyFile4**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4) | Recupera estatísticas de download para servidores de pares e de origem. |
| [**IBackgroundCopyFile5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5) | Fornece métodos get e set de propriedade genérica para propriedades BackgroundCopyFile. |
| [**IBackgroundCopyFile6**](/windows/desktop/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6) | Obtém ou define propriedades genéricas de transferências de arquivo BITS. |
| [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) | Adiciona arquivos ao trabalho, define o nível de prioridade do trabalho, determina o estado do trabalho e inicia e interrompe o trabalho. |
| [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) | Recupera dados de resposta de um trabalho de upload, determina o progresso da transferência de dados de resposta para o cliente, solicita a execução da linha de comando e fornece credenciais para um proxy e servidor remoto. |
| [**IBackgroundCopyJob3**](/windows/desktop/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3) | Baixa intervalos de um arquivo, altera o prefixo de um nome de arquivo remoto e mantém as informações de proprietário e ACL com o arquivo. |
| [**IBackgroundCopyJob4**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4) | Habilita o cache par, restringe o tempo de download e inspeciona as características do token do usuário. |
| [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) | Consulta ou define vários comportamentos opcionais de um trabalho. |
| [**IBackgroundCopyJobHttpOptions**](/windows/desktop/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions) | Especifica certificados de cliente para autenticação de cliente baseada em certificado e cabeçalhos personalizados para solicitações HTTP. |
| [**IBackgroundCopyJobHttpOptions2**](/windows/desktop/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2) | Use essa interface para recuperar e/ou para substituir o método HTTP usado para uma transferência bits. |
| [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) | Cria trabalhos de transferência, recupera um objeto enumerador de trabalhos na fila e recupera trabalhos individuais da fila. |
| [**IBitsPeer**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeer) | Obtém informações sobre um par na região. |
| [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) | Gerencie o pool de pares do qual você pode baixar conteúdo. |
| [**IBitsPeerCacheRecord**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacherecord) | Obtém informações sobre um arquivo no cache. |
| [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions) | Associa e gerencia um par de tokens de segurança para um trabalho de transferência Serviço de Transferência Inteligente em Segundo Plano (BITS). |
| [**IEnumBackgroundCopyFiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) | Enumera arquivos no trabalho. |
| [**IEnumBackgroundCopyJobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) | Enumera trabalhos na fila de transferência. |
| [**IEnumBitsPeerCacheRecords**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords) | Enumera os registros do cache. |
| [**IEnumBitsPeers**](/windows/desktop/api/Bits3_0/nn-bits3_0-ienumbitspeers) | Enumera a lista de pares que o BITS descobriu. |



 

 

 




