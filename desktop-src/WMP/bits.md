---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Armazenamentos online do Windows Media Player, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- tipo 2 lojas online, Serviço de Transferência Inteligente em Segundo Plano (BITS)
- BITS
- BITS (Serviço de Transferência Inteligente em Segundo Plano)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294172"
---
# <a name="bits"></a>BITS

O [serviço de transferência inteligente em segundo plano](/windows/desktop/Bits/background-intelligent-transfer-service-portal) é um recurso do sistema operacional Windows. O BITS transfere arquivos (downloads ou uploads) entre um cliente e um servidor e fornece informações de progresso relacionadas às transferências. Se você quiser transferir arquivos usando código C++, o BITS é a tecnologia correta a ser usada. Se você quiser transferir arquivos usando código JScript em sua página da Web da loja online, use o Gerenciador de download em vez disso.

Como o Gerenciador de download do Windows Media Player usa BITS, você pode executar etapas para configurar seus trabalhos de cópia do BITS de forma que o Windows Media Player gerencie os trabalhos para você. Para fazer isso, você deve seguir a Convenção descrita na seção [Convenção de trabalho do bits do Windows Media Player](windows-media-player-bits-job-convention.md) ao adicionar seus trabalhos à fila de transferência do bits. Esta seção também descreve um mecanismo para recuperar informações sobre seus trabalhos do BITS em sua página da Web de lojas online.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Gerenciador de download**](using-the-download-manager.md)
</dt> <dt>

[**Sobre as lojas online do tipo 2**](about-type-2-online-stores.md)
</dt> </dl>

 

 