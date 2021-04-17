---
description: O mecanismo de protocolo Schannel executa o handshake e a autenticação em um processo seguro e a criptografia em massa/transmissão de mensagens no processo do aplicativo.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Cruzamento dos limites de processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762019"
---
# <a name="crossing-process-boundaries"></a>Cruzamento dos limites de processo

O mecanismo de protocolo [*Schannel*](../secgloss/s-gly.md) executa o handshake e a autenticação em um [*processo*](../secgloss/p-gly.md) seguro e a criptografia em massa/transmissão de mensagens no processo do aplicativo. Isso significa que as [*chaves de criptografia em massa*](../secgloss/b-gly.md) e as chaves [*Mac*](../secgloss/m-gly.md) devem ser copiadas de um processo para outro. Para copiar as chaves de um processo para outro, use as funções [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) da seguinte maneira:

1.  O processo seguro exporta cada chave para um [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) usando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)e, em seguida, destrói a chave usando [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Observe que, se a chave for armazenada em hardware, o CSP deverá reconhecê-la e não deverá tentar destruir a chave.
2.  O processo seguro passa o OPAQUEKEYBLOBs para o processo do aplicativo de uma maneira além do escopo deste documento.
3.  O processo do aplicativo importa cada OPAQUEKEYBLOB de volta para o CSP usando [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). Neste ponto, a chave deve estar exatamente no mesmo [*estado*](../secgloss/s-gly.md) em que foi exportada.

 

 
