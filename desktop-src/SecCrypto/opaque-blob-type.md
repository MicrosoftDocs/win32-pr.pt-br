---
description: BLOBs opacos, também conhecidos como OPAQUEKEYBLOBs, são usados para armazenar chaves de sessão em um formato específico de fornecedor, como Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Tipo de BLOB opaco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370775"
---
# <a name="opaque-blob-type"></a>Tipo de BLOB opaco

[*BLOBs opacos*](../secgloss/o-gly.md), também conhecidos como OPAQUEKEYBLOBs, são usados para armazenar [*chaves de sessão*](../secgloss/s-gly.md) em um formato específico de fornecedor, como [*Schannel*](../secgloss/s-gly.md). Eles contêm o material de chave base e todas as informações de [*estado*](../secgloss/s-gly.md) atuais. Isso inclui informações como o [*valor salt*](../secgloss/s-gly.md), o [*vetor de inicialização*](../secgloss/i-gly.md)e a tabela de chave. O formato dos BLOBs opacos não é publicado. Cada fornecedor do CSP determina seu próprio formato de BLOB.

Como uma chave é exportada para um BLOB opaco no formato específico do CSP, ela só pode ser importada para o CSP do qual foi exportada originalmente.

Quando dois processos estão envolvidos, cada [*processo*](../secgloss/p-gly.md) chama o [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) de forma independente. Cada processo Obtém um identificador para um contêiner de chave. É possível que ambos os processos tenham identificadores para o mesmo contêiner de chave. Um processo cria as chaves e as exporta em BLOBs opacos e, em seguida, passa os BLOBs para o segundo processo. O segundo processo importa as chaves do BLOB para seu [*contêiner de chave*](../secgloss/k-gly.md).

Se um CSP de hardware não oferecer suporte à exportação de chaves, o BLOB poderá conter apenas o índice de um registro de chave ou algo semelhante. Nesse caso, o restante do procedimento é ignorado.

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
