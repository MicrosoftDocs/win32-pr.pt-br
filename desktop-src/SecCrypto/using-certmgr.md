---
description: Use o CertMgr para exibir certificados, CRLs e CTLs de um arquivo ou um armazenamento de certificados, para copiar certificados em um armazenamento de certificados, para excluir certificados de um armazenamento de certificados e salvar certificados em arquivos.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Usando CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c0e62135937e0e14bcdb97ee9d51d37d174de80078939ef1e0c762461923f53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971537"
---
# <a name="using-certmgr"></a>Usando CertMgr

[O CertMgr](certmgr.md) pode ser usado para exibir [*certificados,*](../secgloss/c-gly.md)CRLs [*(listas*](../secgloss/c-gly.md) de certificados revogados) e CTLs [*(listas*](../secgloss/c-gly.md) de confiança de certificado) de um arquivo ou um armazenamento de certificados, para copiar certificados em um armazenamento de certificados, [](../secgloss/c-gly.md)para excluir certificados de um armazenamento de certificados e salvar certificados em arquivos.

Quando [o CertMgr](certmgr.md) é usado sem opções, um assistente certMgr é exibido para orientar o usuário durante a operação.

O arquivo deve ser um dos seguintes tipos:

-   Um arquivo de certificado, CRL ou CTL codificado (pode ser codificado em base 64)
-   Um arquivo PKCS \# 7
-   Um arquivo SPC
-   Um documento assinado
-   Um storeFile serializado

Os exemplos a seguir usam [comandos CertMgr](certmgr.md) para executar tarefas comuns de certificado.

-   Ex veja os certificados, as CRLs e as CTLs *de MyFile.ext.*

    **certmgr** *MyFile.ext*

-   Exibir os certificados, as CRLs e as CTLs do meu armazenamento do sistema.

    **certmgr -s my**

-   Copie todos os certificados, CRLs e CTLs em um arquivo chamado *MyFile.ext* para um novo arquivo, *chamado NewFile.ext.*

    **certmgr -add -all -c** *MyFile.ext* *NewFile.ext*

-   Copie todos os certificados, CRLs e CTLs do armazenamento do sistema MY para um arquivo *chamado NewMyFile.ext.*

    **certmgr -add -all -c -s my** *NewMyFile.ext*

-   Copie um certificado com o nome comum *MyCert* no armazenamento do sistema MY para um arquivo *chamado NewCert.cer.*

    **certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*

-   Exclua todos os certificados do meu armazenamento do sistema.

    **certmgr -del -all -c -s my**

-   Exclua todas as CTLs do repositório do sistema MY e salve o repositório resultante em um arquivo *chamado NewStore.str*.

    **certmgr -del -all -ctl -s my** *NewStore.str*

-   Salve, em um arquivo chamado *NewCert.cer*, um certificado que é um certificado codificado em [*X.509,*](../secgloss/x-gly.md) que tem o nome comum *MyCert* e que está localizado no armazenamento de certificados raiz.

    **certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[CertMgr](certmgr.md)
</dt> </dl>

 

 
