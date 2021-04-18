---
title: Uso do processo de mapeamento de cores com o WCS
description: O mapeamento de cores WCS é baseado em perfis de dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- WCS (sistema de cores do Windows), mapeamento de cores
- WCS (sistema de cores do Windows), mapeamento de cores
- gerenciamento de cores de imagem, mapeamento de cores
- gerenciamento de cores, mapeamento de cores
- cores, mapeamento de cores
- mapeamento de cores
- WCS (sistema de cores do Windows), perfis de dispositivo
- WCS (sistema de cores do Windows), perfis de dispositivo
- gerenciamento de cores de imagem, perfis de dispositivo
- gerenciamento de cores, perfis de dispositivo
- cores, perfis de dispositivo
- WCS (sistema de cores do Windows), perfis
- WCS (sistema de cores do Windows), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- perfis de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "105793777"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Uso do processo de mapeamento de cores com o WCS

O mapeamento de cores WCS é baseado em [perfis de dispositivo](d.md). Eles são fornecidos por fornecedores de dispositivos de hardware de cores e instalados quando um dispositivo é instalado. Quando o mapeamento de cores é usado por um programa de aplicativo, o WCS acessa o perfil de dispositivo da imagem para obter as informações necessárias para converter a imagem nos PCS. A conversão é feita pelo CMM.

Um perfil de dispositivo pode ser inserido na própria imagem. Portanto, o perfil do dispositivo viaja com a imagem, mesmo pela Internet. Um usuário não precisa do dispositivo de origem para obter um mapeamento de cores preciso. Se uma imagem não tiver um perfil de dispositivo, o espaço sRGB será usado como padrão. Para obter mais detalhes, consulte [usando o gerenciamento de cores na Internet](using-color-management-on-the-internet.md).

Observe que os aplicativos que usam o WCS nunca devem inserir o perfil sRGB em uma imagem. O espaço de cores sRGB fornece um espaço de cores padronizado que é portável em todos os dispositivos. Ele está automaticamente disponível para os usuários do Windows 98 e posterior, bem como Windows 2000 e posterior. Portanto, ele não precisa viajar com a imagem.

Depois que as cores da imagem estiverem nos [PCs](p.md), o WCS acessará o perfil do dispositivo do dispositivo de destino. Ele obtém o CMM para converter as cores da imagem dos PCS para a gama do dispositivo de destino.

O mapeamento de cores mais complexo também pode ser feito com o WCS. Por exemplo, ele pode ser usado para ter uma ideia da aparência de uma imagem criada em uma exibição de vídeo quando impressa em uma impressora laser de alta resolução. O exemplo se torna mais complexo se houver apenas uma impressora jato de radiostandard na qual seja possível visualizá-la. A imagem pode ser convertida da gama da tela, na gama da impressora da jato de radiográfica. A partir daí, ele pode ser convertido na gama da impressora laser. A imagem resultante pode ser impressa na impressora jato de radiográfica. É claro que a imagem estaria em uma resolução mais alta quando impressa na impressora laser colorida. No entanto, as cores da imagem de prova impressa na impressora jato de radiográfica seriam uma correspondência próxima às cores que a impressora laser imprimiria.

A maneira como as conversões no exemplo são realizadas é converter as cores da imagem da gama do vídeo nos PCS. Depois que as cores da imagem forem convertidas nos PCS, o perfil do dispositivo da impressora jato de radiográfica será usado para transformá-las na gama da impressora da jato de radiográfica. Em seguida, a transformação de gama para PCS seria usada para mover as cores de volta para os PCS. A partir daí, o perfil de dispositivo da impressora laser é usado para converter as cores dos PCS na gama da impressora laser.

A capacidade de transformar facilmente as cores de uma gama de dispositivos nos PCS e voltar novamente permite que as cores de imagem pretendidas para um dispositivo de saída de cor sejam provadas em praticamente qualquer outro.

No exemplo anterior, a descrição varia do procedimento real um pouco para maior clareza. Na realidade, todas as transformações mencionadas no parágrafo anterior seriam concatenadas em uma única transformação.

 

 




