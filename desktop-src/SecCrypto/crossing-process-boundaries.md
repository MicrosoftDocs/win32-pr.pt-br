---
description: O mecanismo de protocolo Schannel executa a autenticação e a prática em um processo seguro e a criptografia/mensagem em massa passando o processo do aplicativo.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Cruzar limites do processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f8ba4c2d7a0a80ad97e62487421b5b4a0a6f8deda9d8edb550c2d8fcddab15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768862"
---
# <a name="crossing-process-boundaries"></a>Cruzar limites do processo

O [*mecanismo de protocolo Schannel*](../secgloss/s-gly.md) executa a autenticação e a prática em um processo seguro e a criptografia/mensagem em massa passando o processo do aplicativo. [](../secgloss/p-gly.md) Isso significa que as [*chaves de criptografia em*](../secgloss/b-gly.md) massa e as chaves [*MAC*](../secgloss/m-gly.md) devem ser copiadas de um processo para outro. Para copiar as chaves de um processo para outro, use as funções [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) da seguinte maneira:

1.  O processo seguro exporta cada chave para um [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) usando [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)e, em seguida, destrói a chave usando [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Observe que, se a chave for armazenada em hardware, o CSP deverá reconhecer isso e não deve tentar destruir a chave.
2.  O processo seguro passa os OPAQUEKEYBLOBs para o processo do aplicativo de uma maneira além do escopo deste documento.
3.  O processo do aplicativo importa cada OPAQUEKEYBLOB de volta para o CSP usando [**CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) Neste ponto, a chave deve estar exatamente no [*mesmo*](../secgloss/s-gly.md) estado de quando foi exportada.

 

 
