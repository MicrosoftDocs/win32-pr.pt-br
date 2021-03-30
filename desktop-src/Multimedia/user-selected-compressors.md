---
title: User-Selected compactadores
description: User-Selected compactadores
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- VCM (Gerenciador de compactação de vídeo), compactadores selecionados pelo usuário
- VCM (Gerenciador de compactação de vídeo), compactadores selecionados pelo usuário
- Função ICCompressorChoose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916435"
---
# <a name="user-selected-compressors"></a>User-Selected compactadores

Ao compactar dados, seu aplicativo pode usar a função [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para criar uma caixa de diálogo na qual o usuário pode selecionar o compressor. Você pode especificar sinalizadores para essa função para permitir que o usuário especifique a frequência de quadro-chave e a taxa de dados de filme ou para exibir uma janela de visualização.

O compressor selecionado pelo usuário é aberto automaticamente e seu identificador é retornado no membro HIC da estrutura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) especificada em **ICCompressorChoose**.

Se você usar **ICCompressorChoose**, use a função [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) para fechar o compressor e liberar todos os recursos associados à estrutura **COMPVARS** .

 

 




