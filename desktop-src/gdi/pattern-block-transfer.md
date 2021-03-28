---
description: O nome da função PatBlt (uma abreviação para transferência de bloco de padrão) implica que essa função simplesmente Replica o pincel (ou padrão) até que ele preencha um retângulo especificado.
ms.assetid: 601e1e79-a328-4e63-958a-ca26129e03f8
title: Transferência de bloco de padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54424348c28b83d1d0d1075072e80b18049546ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988796"
---
# <a name="pattern-block-transfer"></a>Transferência de bloco de padrão

O nome da função [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) (uma abreviação para transferência de bloco de padrão) implica que essa função simplesmente Replica o pincel (ou padrão) até que ele preencha um retângulo especificado. No entanto, a função é realmente muito mais potente. Antes de replicar o pincel, ele combina os dados de cor para o padrão com os dados de cor dos pixels existentes na exibição do vídeo usando uma operação de rasterização (ROP). Um ROP é uma operação bit que é aplicada aos bits de dados de cor para o pincel replicado e os bits de dados de cor para o retângulo de destino no dispositivo de vídeo. Há 256 ROPs; no entanto, a função **PatBlt** reconhece apenas aqueles que exigem um padrão e um destino (não aqueles que exigem uma origem). A tabela a seguir identifica o ROPs mais comum.



| ROP       | Description                                                                         |
|-----------|-------------------------------------------------------------------------------------|
| PATCOPY   | Copia o padrão para o bitmap de destino.                                       |
| PATINVERT | Combina o bitmap de destino com o padrão usando o operador XOR booliano. |
| DSTINVERT | Inverte o bitmap de destino.                                                     |
| ESCURIDÃO | Transforma toda a saída em zeros binários.                                                   |
| DOCUMENTAÇÃO | Transforma todas as saídas em binários.                                                    |



 

Para obter mais informações, consulte [raster Operation codes](raster-operation-codes.md).

 

 



