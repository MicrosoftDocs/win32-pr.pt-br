---
description: Conjunto de propriedades de revisão do quadro
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Conjunto de propriedades de revisão do quadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645934"
---
# <a name="frame-stepping-property-set"></a>Conjunto de propriedades de revisão do quadro

Os decodificadores que implementam a busca precisa do quadro no Microsoft DirectShow devem implementar o \_ conjunto de propriedades am KSPROPSETID \_ FrameStep, que é usado em conjunto com a interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .



|                   |                            |
|-------------------|----------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ FrameStep |



 



| ID da propriedade                              | Descrição                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ etapa FRAMESTEP da propriedade am \_            | Instrui o decodificador a iniciar uma operação de etapa e passa uma estrutura [**\_ \_ FRAMESTEP de propriedade am**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) que especifica o número de etapas.            |
| \_Propriedade am \_ FRAMESTEP \_ cancelar          | Instrui o decodificador para cancelar a operação de etapa atual. Nenhum dado de instância está associado a esta propriedade.                                                                  |
| \_FRAMESTEP da propriedade am \_ \_         | O decodificador retorna S \_ OK nessa instrução para indicar que ele pode executar a revisão do quadro, \_ caso contrário, S false. Nenhum dado de instância é passado quando essa propriedade é definida.         |
| \_Propriedade am \_ FRAMESTEP \_ CANSTEPMULTIPLE | O decodificador retorna S \_ OK nessa instrução para indicar que ele pode passar vários quadros por vez; \_ caso contrário, S false. Nenhum dado de instância é passado quando essa propriedade é definida. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 



