---
description: Descreve as tarefas que devem ser realizadas para criar uma mensagem assinada.
ms.assetid: 61896022-28c2-4f70-977a-c990b4b23c55
title: Criando uma mensagem assinada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f68511c41a10fc0f690574e71c1dfe8a354efbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170203"
---
# <a name="creating-a-signed-message"></a>Criando uma mensagem assinada

A ilustração a seguir descreve as tarefas que devem ser realizadas para criar uma mensagem assinada. As etapas são listadas após a ilustração.

![assinando uma mensagem](images/signdmsg.png)

**Para criar uma mensagem assinada**

1.  Crie os dados (se necessário) e obtenha um ponteiro para ele.
2.  Abra um [*repositório de certificados*](../secgloss/c-gly.md) que contenha o certificado do signatário.
3.  Obtenha a [*chave privada*](../secgloss/p-gly.md) para o certificado. Uma propriedade deve ser definida no certificado antes de ser usada, para vincular um certificado a um [*CSP*](../secgloss/c-gly.md)específico e, dentro desse CSP, a uma chave privada específica. Isso precisa ser definido uma vez.
4.  Escolha um algoritmo de hash para a operação de resumo. É recomendável que o algoritmo de hash seja selecionado de um local configurável que possa ser atualizado posteriormente sem a necessidade de alterações no código.
5.  Envie os dados por meio da função de hash usando o algoritmo de hash, criando assim um [*hash*](../secgloss/h-gly.md) (Digest) dos dados.
6.  Usando a [*chave privada*](../secgloss/p-gly.md) obtida por meio da propriedade no certificado, criptografe o resumo, criando a assinatura.
7.  Inclua o seguinte na mensagem assinada:

    -   Os dados assinados
    -   O algoritmo de hash
    -   A assinatura
    -   O identificador de signatário (emissor do certificado e número de série)
    -   O certificado do signatário (opcional)

Para obter um procedimento detalhado e um exemplo, consulte o [procedimento para assinar dados](procedure-for-signing-data.md) e [programa de exemplo C: assinando uma mensagem e verificando uma assinatura de mensagem](example-c-program-signing-a-message-and-verifying-a-message-signature.md).

 

 
