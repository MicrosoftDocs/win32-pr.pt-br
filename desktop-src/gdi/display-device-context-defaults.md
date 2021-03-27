---
description: Na primeira criação de um contexto de dispositivo de vídeo, o sistema atribui valores padrão para os atributos (ou seja, objetos de desenho, cores e modos) que compõem o contexto do dispositivo.
ms.assetid: 1a9244e6-2773-435a-8569-806df3a0cd39
title: Exibir padrões de contexto do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8abcf79339d4f1cc158253d46cc3eb02ec41311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827659"
---
# <a name="display-device-context-defaults"></a>Exibir padrões de contexto do dispositivo

Na primeira criação de um contexto de dispositivo de vídeo, o sistema atribui valores padrão para os atributos (ou seja, objetos de desenho, cores e modos) que compõem o contexto do dispositivo. A tabela a seguir mostra os valores padrão para os atributos de um contexto de dispositivo de exibição.



| Atributo                             | Valor padrão                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Cor da tela de fundo                      | Configuração de cor do plano de fundo do painel de controle (normalmente, branco).                                                                               |
| Modo em segundo plano                       | OPACO                                                                                                                                        |
| Bitmap                                | Nenhum                                                                                                                                          |
| Pincel                                 | \_pincel branco                                                                                                                                  |
| Origem do pincel                          | (0, 0)                                                                                                                                         |
| Área de recorte                       | Janela inteira ou área de cliente com a região de atualização recortada, conforme apropriado. As janelas filho e pop-up na área do cliente também podem ser recortadas. |
| Paleta                               | \_paleta padrão                                                                                                                              |
| Posição da caneta atual                  | (0, 0)                                                                                                                                         |
| Origem do dispositivo                         | Canto superior esquerdo da janela ou da área do cliente.                                                                                           |
| Modo de desenho                          | \_COPYPEN R2                                                                                                                                   |
| Fonte                                  | fonte do sistema \_                                                                                                                                  |
| Espaçamento entre caracteres                | 0                                                                                                                                             |
| Modo de mapeamento                          | \_texto mm                                                                                                                                      |
| Caneta                                   | \_caneta preta                                                                                                                                    |
| [**Polígono**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) – modo de preenchimento | Alterne                                                                                                                                     |
| Modo de ampliação                          | BLACKONWHITE                                                                                                                                  |
| Cor do texto                            | Configuração de cor do texto no painel de controle (normalmente, preto).                                                                                     |
| Extensão do visor                       | (1, 1)                                                                                                                                         |
| Origem do visor                       | (0, 0)                                                                                                                                         |
| Extensão da janela                         | (1, 1)                                                                                                                                         |
| Origem da janela                         | (0, 0)                                                                                                                                         |



 

Um aplicativo pode modificar os valores dos atributos de contexto do dispositivo de exibição usando funções de seleção e atributo, como [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject), [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)e [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor). Por exemplo, um aplicativo pode modificar as unidades de medida padrão no sistema de coordenadas usando **SetMapMode** para alterar o modo de mapeamento.

As alterações nos valores de atributo de um contexto de dispositivo comum, pai ou de janela não são permanentes. Quando um aplicativo libera esses contextos de dispositivo, as seleções atuais, como o modo de mapeamento e a região de recorte, são perdidas, pois o contexto é retornado para o cache. As alterações em uma classe ou contexto de dispositivo privado persistem indefinidamente. Para restaurá-los para seus padrões originais, um aplicativo deve definir explicitamente cada atributo.

 

 



