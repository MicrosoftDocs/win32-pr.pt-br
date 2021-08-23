---
title: Uso do processo de mapeamento de cores com o WCS
description: O mapeamento de cores do WCS é baseado em perfis de dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Sistema de Cores (WCS), mapeamento de cores
- WCS (Windows color system),mapeamento de cores
- gerenciamento de cores da imagem, mapeamento de cores
- gerenciamento de cores, mapeamento de cores
- cores, mapeamento de cores
- mapeamento de cores
- Windows Sistema de cores (WCS), perfis de dispositivo
- WCS (Windows color system), perfis de dispositivo
- gerenciamento de cores da imagem, perfis de dispositivo
- gerenciamento de cores, perfis de dispositivo
- cores, perfis de dispositivo
- Windows Sistema de Cores (WCS), perfis
- WCS (Windows color system),perfis
- gerenciamento de cores da imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- perfis de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe785af9fa4160c2aa1e54c6765857edc9c7aacb1a8fa40a0ad04e634b4ab602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934256"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Uso do processo de mapeamento de cores com o WCS

O mapeamento de cores do WCS é baseado em [perfis de dispositivo.](d.md) Eles são fornecidos por fornecedores de dispositivos de hardware de cores e instalados quando um dispositivo é instalado. Quando o mapeamento de cores é usado por um programa de aplicativo, o WCS acessa o perfil de dispositivo da imagem para obter as informações necessárias para converter a imagem no PCS. A conversão é feita pelo CMM.

Um perfil de dispositivo pode ser inserido na própria imagem. Portanto, o perfil do dispositivo percorre a imagem, mesmo pela Internet. Um usuário não precisa do dispositivo de origem para obter um mapeamento de cores preciso. Se uma imagem não tiver um perfil de dispositivo, o espaço sRGB será usado como padrão. Para obter mais detalhes, consulte [Usando o Gerenciamento de Cores na Internet.](using-color-management-on-the-internet.md)

Observe que os aplicativos que usam o WCS nunca devem inserir o perfil sRGB em uma imagem. O espaço de cores sRGB fornece um espaço de cores padronizado que é portátil em todos os dispositivos. Ele está disponível automaticamente para usuários do Windows 98 e posteriores, bem como Windows 2000 e posteriores. Portanto, ele não precisa viajar com a imagem.

Depois que as cores da imagem estão [no PCS,](p.md)o WCS acessa o perfil do dispositivo de destino. Ele obtém o CMM para converter as cores da imagem do PCS para a gama do dispositivo de destino.

O mapeamento de cores mais complexo também pode ser feito com o WCS. Por exemplo, ele pode ser usado para ter uma ideia de como seria a aparência de uma imagem criada em uma exibição de vídeo quando impressa em uma impressora de alta resolução. O exemplo fica mais complexo se houver apenas uma impressora de inkjet padrão na qual a visualização. A imagem pode ser convertida do gamut da exibição, na gama da impressora inkjet. A partir daí, ele pode ser convertido no gamut da impressora de laser. A imagem resultante pode ser impressa na impressora inkjet. É claro que a imagem estaria em uma resolução mais alta quando impressa na impressora de cores do laser. No entanto, as cores da imagem de prova impressa na impressora inkjet seriam uma combinação próxima às cores que a impressora de laser imprimiria.

A maneira como as conversões no exemplo são realizadas é converter as cores da imagem da gama da exibição no PCS. Depois que as cores da imagem são convertidas no PCS, o perfil do dispositivo da impressora inkjet seria usado para transformá-las no gamut da impressora inkjet. Em seguida, a transformação gamut para PCS seria usada para mover as cores de volta para o PCS. A partir daí, o perfil do dispositivo da impressora de raios é usado para converter as cores de PCS na gama da impressora de laser.

A capacidade de transformar facilmente cores de uma gama de dispositivos para o PCS e voltar permite que as cores da imagem destinadas a um dispositivo de saída de cor sejam provadas em praticamente qualquer outro.

No exemplo anterior, a descrição varia um pouco do procedimento real para maior clareza. Na realidade, todas as transformações mencionadas no parágrafo anterior seriam concatenadas em uma única transformação.

 

 




