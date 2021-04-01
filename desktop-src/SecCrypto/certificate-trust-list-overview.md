---
description: Além de certificados e listas de certificados revogados (CRL), o repositório de certificados do CryptoAPI dá suporte à CTL (lista de certificados confiáveis).
ms.assetid: b0f7e7ce-f981-4f3f-83a0-7792224ce0e3
title: Visão geral da lista de certificados confiáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bdbd8b5fdfe4b2d81f3faddb052c16ecf32428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829428"
---
# <a name="certificate-trust-list-overview"></a>Visão geral da lista de certificados confiáveis

Além de certificados e listas de certificados [*revogados*](../secgloss/c-gly.md) (CRL), o [](../secgloss/c-gly.md) [*repositório de certificados*](../secgloss/c-gly.md) do CryptoAPI dá suporte à CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ). Uma CTL é uma lista predefinida de itens assinados por uma entidade confiável. Uma CTL é uma lista de [*hashes*](../secgloss/h-gly.md) de certificados ou uma lista de nomes de arquivos. Todos os itens da lista são autenticados e aprovados por uma entidade de assinatura confiável. Uma estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) é semelhante às estruturas de contexto de certificado e CRL. Um contexto de CTL pode persistir no repositório de certificados.

Uma CTL de CryptoAPI é uma lista de itens que foram assinados por uma entidade confiável. A lista de itens pode ser qualquer coisa, como uma lista de hashes de certificados ou uma lista de nomes de arquivos. Na maioria dos casos, uma CTL é uma lista de contextos de certificado com hash. Todos os itens da lista são autenticados e aprovados pela entidade de assinatura. O uso principal de CTLs é verificar mensagens assinadas, usando a CTL como uma fonte de [*certificados raiz*](../secgloss/r-gly.md)confiáveis.

A estrutura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) é semelhante às estruturas de contexto de certificado e CRL; no entanto, diferentemente das estruturas de contexto de certificado e CRL, a estrutura de **\_ contexto de CTL** contém um membro **hCryptMsg** . Esse identificador é aberto por uma chamada para qualquer uma das funções que retornam uma estrutura de **\_ contexto de CTL** , possibilitando o uso das funções de mensagem para verificar a assinatura da lista de certificados confiáveis. Essa verificação é necessária para garantir que uma CTL não seja uma plantadas de CTL falsa por uma entidade não autorizada.

Para obter procedimentos para criar uma CTL assinada e salvá-la em um repositório de certificados, consulte [criando, assinando e armazenando uma CTL](creating-signing-and-storing-a-ctl.md). Consulte também [verificando uma CTL](verifying-a-ctl.md) e [verificando mensagens assinadas usando CTLs](verifying-signed-messages-by-using-ctls.md) para procedimentos de verificação passo a passo.

 

 
