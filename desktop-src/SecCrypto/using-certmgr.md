---
description: Use o CertMgr para exibir certificados, CRLs e CTLs de um arquivo ou de um repositório de certificados, para copiar certificados em um repositório de certificados, para excluir certificados de um repositório de certificados e para salvar certificados em arquivos.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Usando CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753389"
---
# <a name="using-certmgr"></a>Usando CertMgr

O [certmgr](certmgr.md) pode ser usado para exibir [*certificados*](../secgloss/c-gly.md), [*listas de certificados revogados*](../secgloss/c-gly.md) (CRLs) e listas de [*certificados confiáveis*](../secgloss/c-gly.md) (CTLs) de um arquivo ou de um repositório de certificados, para copiar certificados em um [*repositório de certificados*](../secgloss/c-gly.md), para excluir certificados de um repositório de certificados e para salvar certificados em arquivos.

Quando [certmgr](certmgr.md) é usado sem opções, um assistente de certmgr é exibido para orientar o usuário durante a operação.

O arquivo deve ser um dos seguintes tipos:

-   Um arquivo de certificado, CRL ou CTL codificado (pode ser codificado em base-64)
-   Um \# arquivo PKCS 7
-   Um arquivo SPC
-   Um documento assinado
-   Um StoreFile serializado

Os exemplos a seguir usam comandos [certmgr](certmgr.md) para executar tarefas comuns de certificado.

-   Exiba os certificados, as CRLs e as CTLs de *MyFile. ext*.

    **certmgr** *MyFile. ext*

-   Exiba os certificados, as CRLs e as CTLs do meu repositório do sistema.

    **Certmgr-s My**

-   Copie todos os certificados, CRLs e CTLs em um arquivo chamado *MyFile. ext* para um novo arquivo, chamado *newfile. ext*.

    **certmgr-Add-All-c** *MyFile. ext* *newfile. ext*

-   Copie todos os certificados, CRLs e CTLs do meu repositório do sistema para um arquivo chamado *NewMyFile. ext*.

    **certmgr-adicionar-tudo-c-s My** *NewMyFile. ext*

-   Copie um certificado com o nome comum *MyCert* no meu armazenamento do sistema para um arquivo chamado *NewCert. cer*.

    **certmgr-Add-c-n** *MyCert* **-s minha** *NewCert. cer*

-   Exclua todos os certificados do meu repositório do sistema.

    **Certmgr-del-All-c-s meu**

-   Exclua todas as CTLs do meu repositório do sistema e salve o repositório resultante em um arquivo chamado *NewStore. Str*.

    **certmgr-del-All-CTL-s My** *NewStore. Str*

-   Salve, em um arquivo chamado *NewCert. cer*, um certificado que é um certificado codificado [*X. 509*](../secgloss/x-gly.md) , que tem o nome comum *MyCert* e que está localizado no repositório de certificados raiz.

    **certmgr-Put-c-n** *MyCert* **-s raiz** *NewCert. cer*

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[CertMgr](certmgr.md)
</dt> </dl>

 

 
