---
description: Os visores podem exibir uma sequência de imagens e texto em uma caixa de diálogo durante uma instalação. Normalmente, os slides são usados para criar o efeito visual de uma apresentação de slides ou animação que informa o usuário sobre o progresso de uma instalação.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Exibindo cartazes em uma caixa de diálogo sem modo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badf81e2b6d0131d1224f10b19e8de3c06f173ef91e3b08f3a45f31aef52be11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086166"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Exibindo cartazes em uma caixa de diálogo sem modo

Os visores podem exibir uma sequência de imagens e texto em uma caixa de diálogo durante uma instalação. Normalmente, os slides são usados para criar o efeito visual de uma apresentação de slides ou animação que informa o usuário sobre o progresso de uma instalação.

**Para exibir painéis em uma caixa de diálogo sem modo**

1.  Inclua um registro na Tabela [de Diálogo](dialog-table.md) para a caixa de diálogo sem modo que contém o quadro. Depois que um visor é exibido, uma caixa de diálogo sem modo retorna o controle para o Instalador. Isso permite que o Instalador processe mensagens e atualize a caixa de diálogo e a caixa de diálogo. Para criar uma caixa de diálogo sem modo, não defina o Bit de Estilo de Caixa de Diálogo Modal no campo Atributos da [Tabela de Diálogo](dialog-table.md). O registro [tabela de diálogo](dialog-table.md) a seguir especifica a caixa de diálogo ActionDialog.

    [Tabela de diálogo](dialog-table.md) (parcial)

    | caixa de diálogo\_     | HCentering | VCentering | Largura | Altura | Atributos | Título  | Control \_ First | Padrão de \_ controle | Cancelar \_ controle |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | Ação | Cancelar         | Cancelar           | Cancelar          |

    

     

2.  Adicione um registro à Tabela [de Controle](control-table.md) para especificar que a caixa de diálogo exibe um visor. O registro define o tamanho e a posição da região na caixa de diálogo em que os controles de quadro listados na [Tabela BBControl](bbcontrol-table.md) devem ser exibidos. O registro [tabela de controle](control-table.md) a seguir define a posição e o tamanho do quadro na caixa de diálogo ActionDialog.

    [Tabela de controle](control-table.md) (parcial)

    | caixa de diálogo\_     | Control   | Type      | X   | Y   | Largura | Altura | Atributos |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | Outdoor | Outdoor | 0   | 110 | 480   | 130    | 1          |

    

     

3.  A [Tabela Demão](billboard-table.md) lista os controles de ano e especifica quando um controle de ano é exibido. Adicione um registro à [Tabela De mista para](billboard-table.md) cada controle de mamão. A [Tabela De montagem](billboard-table.md) observa as mensagens de progresso enviadas durante uma instalação. Um visor é exibido somente quando uma mensagem de progresso é enviada pelas ações listadas na coluna Ação da Tabela [De montagem](billboard-table.md)e somente se o recurso no campo Recurso estiver selecionado para \_ instalação. Depois que um visor é exibido, ele permanece visível até ser coberto por outro visor ou até que a caixa de diálogo seja fechada. Se vários painéis são especificados para uma ação, eles são exibidos um de cada vez na ordem especificada pelo campo Ordenação. Por exemplo, as seguintes entradas [da Tabela Do Mista](billboard-table.md) exibem primeiro o BB1 e, em seguida, os Controles BB2 [Do BB2 Quando](billboard-control.md) a ação [InstallFiles](installfiles-action.md) é executado e o recurso QuickTest foi selecionado para ser instalado.

    [Tabela Do Table](billboard-table.md) (parcial)

    | Outdoor | Recurso   | Ação       | Ordenando |
    |-----------|-----------|--------------|----------|
    | BB1       | Quicktest | InstallFiles | 1        |
    | BB2       | Quicktest | InstallFiles | 2        |

    

     

4.  A [Tabela BBControl](bbcontrol-table.md) especifica os controles que pertencem aos Controles [De Sempre](billboard-control.md) listados na Tabela do Table [DoMs.](billboard-table.md) O [controle de texto](text-control.md), o controle [bitmap](bitmap-control.md)e o [controle de](icon-control.md) ícone são os únicos tipos de controles que podem ir em um menu. Vários controles podem ser colocados em cada um deles. Insira o nome do quadro no campo Demão da Tabela \_ [BBControl](bbcontrol-table.md) exatamente como ele aparece na [Tabela DoRial.](billboard-table.md)

    Cada posição de controle é especificada como as coordenadas do canto superior esquerdo do controle. A origem do sistema de coordenadas está localizada no canto superior esquerdo do controle de ponto de comando, em vez de em um canto da caixa de diálogo. As coordenadas estão em unidades do Instalador, não em unidades de diálogo. Uma unidade do Instalador é igual a um décimo segundo da altura do tamanho da fonte MS Sans Serif de 10 pontos. A tabela [BBControl a seguir](bbcontrol-table.md) registra controles de vínculo a botões.

    [Tabela BBControl](bbcontrol-table.md) (parcial)

    | Outdoor | BBControl | Type   | X   | Y   | Largura | Altura | Atributos | Texto             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Texto      | Texto   | 100 | 30  | 280   | 280    | 3          | Primeiro mamão  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Texto      | Texto   | 100 | 30  | 280   | 20     | 3          | Segundo mamão |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Para exibir um visor na caixa de diálogo ActionDialog, você deve assinar o controle de [setprogress ControlEvent](setprogress-controlevent.md) adicionando um registro à [Tabela EventMapping](eventmapping-table.md). Quando o Instalador publica o SetProgress ControlEvent especificado na coluna Evento, o Instalador define o atributo de controle especificado no campo Atributo. O campo Evento contém o identificador de cadeia de caracteres (sem aspas) do ControlEvent SetProgress. O campo Atributo contém o identificador de cadeia de caracteres (sem aspas) do atributo a ser definido. Os campos \_ Caixa de Diálogo e Controle \_ identificam o Controle Demão e devem corresponder a esses campos na [Tabela de Controle](control-table.md). Por exemplo, a tabela [EventMapping a seguir](eventmapping-table.md) assina um controle para um evento.

    [Tabela EventMapping](eventmapping-table.md) (parcial)

    | caixa de diálogo\_     | controle\_ | Evento       | Atributo |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Outdoor | SetProgress | Progresso  |

    

     

 

 



