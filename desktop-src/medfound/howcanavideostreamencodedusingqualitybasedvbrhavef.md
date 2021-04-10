---
description: Como um fluxo de vídeo codificado usando a taxa de bits baseada em qualidade tem menos quadros do que o fluxo original?
ms.assetid: acce9c88-2ee1-4628-9fd5-ccb441f8b43e
title: Como um fluxo de vídeo codificado usando a taxa de bits baseada em qualidade tem menos quadros do que o fluxo original?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2af2775882155ed7ef2b0cfffdddeb30b2066e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165450"
---
# <a name="how-can-a-video-stream-encoded-using-quality-based-vbr-have-fewer-frames-than-the-original-stream"></a>Como um fluxo de vídeo codificado usando a taxa de bits baseada em qualidade tem menos quadros do que o fluxo original?

A contagem de quadros de um fluxo codificado pode ser menor do que a contagem de quadros do original por um destes dois motivos: quadros duplicados e quadros ignorados.

Normalmente, o codificador não produz quadros que são duplicatas exatas do quadro anterior. Se você precisar ter um exemplo para cada quadro (isso é exigido por alguns contêineres, por exemplo), poderá configurar o codificador para produzir quadros "fictícios" definindo a propriedade [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) como Variant \_ true.

O codificador descarta os quadros quando não é possível codificar todos os quadros sem estourar o buffer. Os quadros descartados afetam a qualidade do fluxo, não há quadros duplicados.

Você pode obter estatísticas de quadro do codificador para determinar se os quadros foram descartados. Para obter mais informações, consulte [obtendo estatísticas de codificação](gettingencodingstatistics.md).

Normalmente, os fluxos de VBR com base em qualidade terão menos quadros do que o original se houver quadros duplicados (porque a taxa de bits não é restrita).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Perguntas frequentes](frequentlyaskedquestions.md)
</dt> </dl>

 

 



