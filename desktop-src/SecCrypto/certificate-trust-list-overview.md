---
description: Além de certificados e CRL (listas de certificados revogados), o armazenamento de certificados CryptoAPI dá suporte à CTL (lista de certificados de confiança).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Visão geral da lista de confiança de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7906f02e9af3534445c5b1d6a48c94653feb78b57c71a23acfd9af51477cd050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771102"
---
# <a name="certificate-trust-list-overview"></a>Visão geral da lista de confiança de certificado

Além de certificados e CRL [*(listas*](../secgloss/c-gly.md) de certificados revogados), o armazenamento de certificados [*CryptoAPI*](../secgloss/c-gly.md) [](../secgloss/c-gly.md) dá suporte à CTL [*(lista*](../secgloss/c-gly.md) de certificados de confiança). Uma CTL é uma lista predefinida de itens assinados por uma entidade confiável. Uma CTL é uma lista de [*hashes*](../secgloss/h-gly.md) de certificados ou uma lista de nomes de arquivo. Todos os itens na lista são autenticados e aprovados por uma entidade de assinatura confiável. Uma [**estrutura CONTEXT \_ CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) é semelhante às estruturas de contexto de certificado e CRL. Um contexto CTL pode ser persistido no armazenamento de certificados.

Uma CTL de CryptoAPI é uma lista de itens assinados por uma entidade confiável. A lista de itens pode ser qualquer coisa, como uma lista de hashes de certificados ou uma lista de nomes de arquivo. Na maioria dos casos, uma CTL é uma lista de contextos de certificado com hashed. Todos os itens na lista são autenticados e aprovados pela entidade de assinatura. O principal uso de CTLs é verificar mensagens assinadas, usando a CTL como uma fonte de [*certificados raiz confiáveis.*](../secgloss/r-gly.md)

A [**estrutura CTL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) é semelhante às estruturas de contexto de certificado e CRL; no entanto, ao contrário das estruturas de contexto de certificado e CRL, a estrutura **CTL \_ CONTEXT** contém um membro **hCryptMsg.** Esse handle é aberto por uma chamada para qualquer uma das funções que retornam uma estrutura **CONTEXT CTL, \_** possibilitando o uso das funções de mensagem para verificar a assinatura da CTL. Essa verificação é necessária para garantir que uma CTL não seja uma CTL falsa plantada por uma entidade não autorizada.

Para procedimentos para criar uma CTL assinada e salvá-la em um armazenamento de certificados, consulte [Criando, assinando e armazenando uma CTL](creating-signing-and-storing-a-ctl.md). Consulte também [Verificando uma CTL](verifying-a-ctl.md) e [Verificando mensagens assinadas usando CTLs](verifying-signed-messages-by-using-ctls.md) para procedimentos de verificação passo a passo.

 

 
