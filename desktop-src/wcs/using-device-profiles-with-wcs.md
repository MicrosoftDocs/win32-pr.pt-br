---
title: Uso de perfis de dispositivo com o WCS
description: Os perfis de dispositivo são uma ferramenta básica para o gerenciamento de cores.
ms.assetid: 9ea420ad-dcf1-4ba9-b739-308be7a56a6c
keywords:
- Windows Sistema de cores (WCS), perfis de dispositivo
- WCS (Windows sistema de cores), perfis de dispositivo
- gerenciamento de cores de imagem, perfis de dispositivo
- gerenciamento de cores, perfis de dispositivo
- cores, perfis de dispositivo
- Windows Sistema de cores (WCS), perfis
- WCS (Windows sistema de cores), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- perfis de dispositivo
- conversão de cores
- perfis de link de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8211ff883f8e30e7b67b0168e6da980744b252cbb1b89412fc834ac6370cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090066"
---
# <a name="using-device-profiles-with-wcs"></a>Uso de perfis de dispositivo com o WCS

Os perfis de dispositivo são uma ferramenta básica para o gerenciamento de cores. Um [perfil de dispositivo](d.md) é um arquivo que contém informações sobre como converter cores no espaço de cores e a [gama](./g.md) de cores de um dispositivo específico em um espaço de cores independente de dispositivo. O espaço de cores independente de dispositivo usado pelo ICM2 é chamado de espaço de conexão de perfil (PCS). Um perfil de dispositivo também contém informações sobre como converter cores dos PCS no espaço de cores e na gama de cores de um dispositivo específico.

Esses dois conjuntos de informações de conversão são usados para [conversão de cores](c.md) e gerenciamento de cores. Por exemplo, uma imagem pode ser criada no espaço de cores e na gama de cores de uma exibição de vídeo. As informações nos arquivos de perfil do dispositivo podem ser usadas para exibir uma representação de uma imagem impressa. Geralmente, os usuários desejam ver na tela como as cores serão alteradas quando uma imagem for impressa. Isso é chamado de prova. Uma imagem pode ser verificada convertendo as cores da gama de cores de origem (a tela) em [PCs](p.md) cores e, em seguida, convertendo-as dos PCs na gama de cores de destino (a impressora). A imagem resultante pode ser exibida na tela, permitindo que o usuário veja qual será a aparência da imagem final quando ela for impressa.

Os perfis de dispositivo também permitem usos mais complexos. Por exemplo, eles podem ser usados para ter uma ideia da aparência de uma imagem criada em uma exibição de vídeo quando impressa em uma impressora laser de alta resolução. O exemplo se tornará mais complexo se houver apenas uma impressora de jato de radiostandard na qual você deve comprovar a ti. O ICM2 converterá a imagem da [gama](./g.md) da tela, na gama da impressora da jato de radiográfica. A partir daí, ele é convertido na gama da impressora laser. A imagem resultante pode ser impressa na impressora jato de radiográfica. É claro que a imagem estaria em uma resolução mais alta quando impressa na impressora laser colorida. No entanto, as cores da imagem de prova impressa na impressora jato de radiográfica seriam uma correspondência próxima às cores que a impressora laser imprimiria.

As conversões de um perfil de dispositivo podem ser concatenadas em um único arquivo, chamado de *perfil de link de dispositivo*. Se uma série de conversões for usada repetidamente, criar um perfil de link de dispositivo para elas reduzirá o tempo de conversão.

Os próprios perfis de dispositivo podem ser gerenciados. O gerenciamento de perfil é o processo de associar perfis de cor a instâncias de dispositivo. Qualquer dispositivo de saída de cor pode ter um conjunto de um ou mais perfis de cor associados a ele. Fabricantes de hardware e terceiros que fornecem perfis de cores precisam executar o gerenciamento de perfil.

Os conjuntos de perfis podem ser compartilhados entre dispositivos ou podem ser dedicados a dispositivos específicos. Por exemplo, suponha que você tenha duas impressoras coloridas do mesmo modelo. Cada impressora exigiria que um conjunto de perfis de cor fosse associado a ele. O conjunto de perfis de cor para uma impressora corresponde às várias configurações possíveis nesse modelo. Sendo do mesmo modelo, ambas as impressoras podem compartilhar um conjunto de perfis. A alternativa é fornecer a cada impressora seu próprio conjunto de perfis distinto. No último caso, os perfis de cor no conjunto podem ser calibrados precisamente para a saída individual da impressora, não apenas as características de saída geral do modelo.

Há três classes diferentes de perfis ICC: perfis de entrada, perfis de exibição e perfis de saída. Os perfis de entrada geralmente são associados a um dispositivo, como um scanner. Os perfis de exibição são normalmente associados a um monitor de computador. Os perfis de saída normalmente são associados a impressoras.

A especificação também permite perfis de dispositivo, perfis abstratos, perfis de link de dispositivo, perfis de cores nomeados e perfis de espaço de cores.

Um perfil de dispositivo descreve o espaço de cores de um dispositivo específico.

Um perfil abstrato fornece um método genérico para que os usuários façam alterações de cores subjetivas em imagens ou objetos gráficos transformando os dados de cor nos PCS.

Como mencionado anteriormente, um perfil de link de dispositivo concatena uma série de perfis em uma transformação.

Os perfis de cor nomeados podem ser considerados como perfis irmãos para perfis de dispositivo. Para um determinado dispositivo, haveria um ou mais perfis de dispositivo para lidar com conversões de cores de processo e um ou mais perfis de cor nomeados para lidar com cores nomeadas. Pode haver vários perfis de cores nomeados para considerar diferentes itens consumíveis ou vários fornecedores de cores nomeados.

Um perfil de espaço de cores descreve um espaço de cores independente de dispositivo.

A tabela a seguir resume os vários tipos de perfis.



| Tipo de Perfil        | Descrição                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Perfil abstrato    | Um perfil que foi ajustado para atender às preferências específicas de um usuário.                                                     |
| Perfil de espaço de cores | Um perfil que descreve um espaço de cores independente de dispositivo.                                                                    |
| Perfil de link do dispositivo | Uma série de perfis que são concatenados em um único perfil.                                                    |
| Perfil do dispositivo      | Um perfil que descreve o espaço de cores de um dispositivo específico.                                                              |
| Exibir Perfil     | Uma classe ou categoria de perfis que inclui qualquer tipo de perfil associado a uma exibição.                                  |
| Perfil de entrada       | Uma classe ou categoria de perfis que inclui qualquer tipo de perfil associado a um dispositivo de entrada, como um scanner.          |
| Perfil de cor nomeada | Um perfil para um espaço de cores que consiste em cores nomeadas.                                                                    |
| Perfis de saída     | Uma classe ou categoria de perfis que inclui qualquer tipo de perfil associado a um dispositivo de saída impresso, como uma impressora. |



 

Transformações de cores podem ser criadas com um ou mais perfis. Se uma transformação for criada com apenas um perfil, o perfil deverá ser um perfil de link de dispositivo. Uma transformação também pode ter dois ou mais perfis em uma cadeia. Se tiver, ele não poderá conter nenhum perfil de link de dispositivo. Os perfis abstratos só podem estar no meio da cadeia. O primeiro e o último perfis devem ser perfis de dispositivo ou perfis de espaço de cores.

 

 