---
title: Compactação de sequência
description: Compactação de sequência
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- VCM (Gerenciador de compactação de vídeo), compactação de sequência
- VCM (Gerenciador de compactação de vídeo), compactação de sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916220"
---
# <a name="sequence-compression"></a>Compactação de sequência

Seu aplicativo pode usar as funções [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)e [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) para compactar uma sequência de quadros. Essas funções usam os dados armazenados na estrutura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) . Os aplicativos usam a função [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para permitir que o usuário selecione um compressor, abra-o e defina os parâmetros de compactação na estrutura **COMPVARS** ; no entanto, os aplicativos podem definir os parâmetros na estrutura manualmente.

Antes que um aplicativo possa começar a compactar uma sequência de quadros, ele deve usar **ICSeqCompressFrameStart** para alocar os recursos necessários. Depois que os recursos são alocados, o aplicativo pode usar **ICSeqCompressFrame** para compactar cada quadro individualmente. A taxa de quadros e a frequência de quadro chave usados na compactação da sequência são especificadas em membros da estrutura **COMPVARS** . O valor de retorno para **ICSeqCompressFrame** aponta para os dados compactados.

Quando um aplicativo conclui a compactação de uma sequência, ele pode usar o **ICSeqCompressFrameEnd** para liberar recursos do sistema alocados para **ICSeqCompressFrameStart**. Para liberar os recursos alocados para a estrutura **COMPVARS** , o aplicativo pode usar a função [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) .

 

 




