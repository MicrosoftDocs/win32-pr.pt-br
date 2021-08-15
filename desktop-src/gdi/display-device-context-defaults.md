---
description: Ao criar primeiro um contexto de dispositivo de exibição, o sistema atribui valores padrão para os atributos (ou seja, objetos de desenho, cores e modos) que compõem o contexto do dispositivo.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Exibir padrões de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366c4ecb861b64d2b69836832259e6820e0f8809e4aa478d074220d133ccec55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887273"
---
# <a name="display-device-context-defaults"></a>Exibir padrões de contexto do dispositivo

Ao criar primeiro um contexto de dispositivo de exibição, o sistema atribui valores padrão para os atributos (ou seja, objetos de desenho, cores e modos) que compõem o contexto do dispositivo. A tabela a seguir mostra os valores padrão para os atributos de um contexto de dispositivo de exibição.



| Atributo                             | Valor padrão                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Cor da tela de fundo                      | Configuração de cor da tela Painel de Controle tela de fundo (normalmente, branco).                                                                               |
| Modo de segundo plano                       | Opaco                                                                                                                                        |
| Bitmap                                | Nenhum                                                                                                                                          |
| Pincel                                 | PINCEL \_ BRANCO                                                                                                                                  |
| Origem do pincel                          | (0,0)                                                                                                                                         |
| Área de recorte                       | Janela inteira ou área de cliente com a região de atualização recortada, conforme apropriado. Janelas filho e pop-up na área do cliente também podem ser recortados. |
| Paleta                               | PALETA \_ PADRÃO                                                                                                                              |
| Posição da caneta atual                  | (0,0)                                                                                                                                         |
| Origem do dispositivo                         | Canto superior esquerdo da janela ou da área do cliente.                                                                                           |
| Modo de desenho                          | R2 \_ COPYPEN                                                                                                                                   |
| Fonte                                  | FONTE DO \_ SISTEMA                                                                                                                                  |
| Espaçamento entre caracteres                | 0                                                                                                                                             |
| Modo de mapeamento                          | MM \_ TEXT                                                                                                                                      |
| Caneta                                   | CANETA \_ PRETA                                                                                                                                    |
| Modo de preenchimento de [**polígono**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) | Alternativo                                                                                                                                     |
| Modo de alongamento                          | BLACKONWHITE                                                                                                                                  |
| Cor do texto                            | Configuração de cor do Painel de Controle (normalmente, preto).                                                                                     |
| Extensão do viewport                       | (1,1)                                                                                                                                         |
| Origem do viewport                       | (0,0)                                                                                                                                         |
| Extensão da janela                         | (1,1)                                                                                                                                         |
| Origem da janela                         | (0,0)                                                                                                                                         |



 

Um aplicativo pode modificar os valores dos atributos de contexto do dispositivo de exibição usando funções de seleção e atributo, como [**SelectObject,**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)e [**SetTextColor.**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) Por exemplo, um aplicativo pode modificar as unidades padrão de medida no sistema de coordenadas usando **SetMapMode** para alterar o modo de mapeamento.

As alterações nos valores de atributo de um contexto de dispositivo comum, pai ou janela não são permanentes. Quando um aplicativo libera esses contextos de dispositivo, as seleções atuais, como o modo de mapeamento e a região de recorte, são perdidas à medida que o contexto é retornado para o cache. As alterações em uma classe ou contexto de dispositivo privado persistem indefinidamente. Para restaurá-los para seus padrões originais, um aplicativo deve definir explicitamente cada atributo.

 

 



