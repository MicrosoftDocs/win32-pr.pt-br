---
title: User-Selected Ltda
description: User-Selected Ltda
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- VCM (gerenciador de compactação de vídeo), vcms selecionados pelo usuário
- VCM (gerenciador de compactação de vídeo), grupo selecionado pelo usuário
- Função ICCompressorChoose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c855acb1ecd69876009d0cc3eb6a3b3f4129cc252183e40c5b2d00289be82842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370796"
---
# <a name="user-selected-compressors"></a>User-Selected Ltda

Ao compactar dados, seu aplicativo pode usar a função [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para criar uma caixa de diálogo na qual o usuário pode selecionar o grupo. Você pode especificar sinalizadores para essa função para permitir que o usuário especifique a frequência do quadro-chave e a taxa de dados do filme ou para exibir uma janela de visualização.

O nó selecionado pelo usuário é aberto automaticamente e seu alça é retornado no membro hic da estrutura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) especificada em **ICCompressorChoose**.

Se você usar **ICCompressorChoose**, use a função [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) para fechar o grupo e liberar todos os recursos associados à estrutura **COMPVARS.**

 

 




