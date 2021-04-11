---
description: Os murals podem exibir uma sequência de imagens e texto em uma caixa de diálogo durante uma instalação. Normalmente, os murals são usados para criar o efeito visual de uma apresentação de slides ou animação que informa ao usuário o progresso de uma instalação.
ms.assetid: 6432ee7d-0da2-48be-b14c-d36a83a3bb1d
title: Exibindo os murals em uma caixa de diálogo sem janela restrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fd0ca40e47a8d52c16db7adde304177d4dc849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091141"
---
# <a name="displaying-billboards-on-a-modeless-dialog"></a>Exibindo os murals em uma caixa de diálogo sem janela restrita

Os murals podem exibir uma sequência de imagens e texto em uma caixa de diálogo durante uma instalação. Normalmente, os murals são usados para criar o efeito visual de uma apresentação de slides ou animação que informa ao usuário o progresso de uma instalação.

**Para exibir os murals em uma caixa de diálogo sem janela restrita**

1.  Inclua um registro na [tabela de diálogo](dialog-table.md) da caixa de diálogo sem janela restrita que contém o mural. Depois que um mural é exibido, uma caixa de diálogo sem janela restrita retorna o controle ao instalador. Isso permite que o instalador processe mensagens e atualize a caixa de diálogo e o mural. Para criar uma caixa de diálogo sem janela restrita, não defina o bit do estilo da caixa de diálogo modal no campo atributos da [tabela de diálogo](dialog-table.md). O registro de [tabela de diálogo](dialog-table.md) a seguir especifica a caixa de diálogo ActionDialog.

    [Tabela de diálogo](dialog-table.md) (parcial)

    | caixa de diálogo\_     | HCentering | VCentering | Largura | Altura | Atributos | Título  | Controlar \_ primeiro | Padrão de controle \_ | \_Cancelar controle |
    |--------------|------------|------------|-------|--------|------------|--------|----------------|------------------|-----------------|
    | ActionDialog | 50         | 50         | 480   | 240    | 5          | Ação | Cancelar         | Cancelar           | Cancelar          |

    

     

2.  Adicione um registro à [tabela de controle](control-table.md) para especificar que a caixa de diálogo exibirá um mural. O registro define o tamanho e a posição da região na caixa de diálogo onde os controles de mural listados na [tabela BBControl](bbcontrol-table.md) devem ser exibidos. O seguinte registro de [tabela de controle](control-table.md) define a posição e o tamanho do mural na caixa de diálogo ActionDialog.

    [Tabela de controle](control-table.md) (parcial)

    | caixa de diálogo\_     | Control   | Type      | X   | S   | Largura | Altura | Atributos |
    |--------------|-----------|-----------|-----|-----|-------|--------|------------|
    | ActionDialog | Mensagem | Mensagem | 0   | 110 | 480   | 130    | 1          |

    

     

3.  A [tabela de mural](billboard-table.md) lista os controles de mensagem e especifica quando um controle de mural específico é exibido. Adicione um registro à [tabela do mural](billboard-table.md) para cada controle do mural. A [tabela do mural](billboard-table.md) inspeciona as mensagens de progresso enviadas durante uma instalação. Um mural é exibido somente quando uma mensagem de progresso é enviada pelas ações listadas na coluna ação da [tabela do mural](billboard-table.md)e somente se o recurso no \_ campo recurso for selecionado para instalação. Depois que um mural é exibido, ele permanece visível até ser coberto por outra mensagem ou até que a caixa de diálogo seja fechada. Se vários murals forem especificados para uma ação, eles serão exibidos um de cada vez na ordem especificada pelo campo ordem. Por exemplo, as seguintes entradas de [tabela de mural](billboard-table.md) exibem primeiro o BB1 e, em seguida, o BB2 de [mural controla](billboard-control.md) quando a ação [InstallFiles](installfiles-action.md) é executada e o recurso QuickTest foi selecionado para ser instalado.

    [Tabela do mural](billboard-table.md) (parcial)

    | Mensagem | Recurso   | Ação       | Ordenando |
    |-----------|-----------|--------------|----------|
    | BB1       | QuickTest | InstallFiles | 1        |
    | BB2       | QuickTest | InstallFiles | 2        |

    

     

4.  A [tabela BBControl](bbcontrol-table.md) especifica os controles que pertencem aos [controles de mural](billboard-control.md) listados na [tabela do mural](billboard-table.md). O controle de [texto](text-control.md), o [controle de bitmap](bitmap-control.md)e o [controle de ícone](icon-control.md) são os únicos tipos de controles que podem ir em um mural. Vários controles podem ser colocados em cada mural. Insira o nome do mural no \_ campo do mural da [tabela BBControl](bbcontrol-table.md) exatamente como ele aparece na [tabela do mural](billboard-table.md).

    Cada posição de controle é especificada como as coordenadas do canto superior esquerdo do controle. A origem do sistema de coordenadas está localizada no canto superior esquerdo do controle do mural, e não em um canto da caixa de diálogo. As coordenadas estão nas unidades do instalador, não nas unidades de caixa de diálogo. Uma unidade de instalador é igual a um décimo da altura do tamanho de fonte MS Sans Serif de 10 pontos. Os registros da [tabela BBControl](bbcontrol-table.md) a seguir vinculam os controles aos murals.

    [Tabela BBControl](bbcontrol-table.md) (parcial)

    | Mensagem | BBControl | Type   | X   | S   | Largura | Altura | Atributos | Texto             |
    |-----------|-----------|--------|-----|-----|-------|--------|------------|------------------|
    | BB1       | Texto      | Texto   | 100 | 30  | 280   | 280    | 3          | Primeira mensagem  |
    | BB1       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Software         |
    | BB1       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Texto      | Texto   | 100 | 30  | 280   | 20     | 3          | Segunda mensagem |
    | BB2       | Bitmap1   | Bitmap | 0   | 0   | 100   | 100    | 3          | Música            |
    | BB2       | Bitmap2   | Bitmap | 380 | 0   | 100   | 100    | 3          | Software         |

    

     

5.  Para exibir um mural na caixa de diálogo ActionDialog, você deve inscrever o controle de mensagem para [ControlEvent, de reprogress](setprogress-controlevent.md) adicionando um registro à [tabela EventMappings](eventmapping-table.md). Quando o instalador publica o ControlEvent, de regressão especificado na coluna evento, o instalador define o atributo de controle que é especificado no campo atributo. O campo de evento contém o identificador de cadeia de caracteres (sem aspas) do ControlEvent, de reprogress. O campo atributo contém o identificador da cadeia de caracteres (sem aspas) do atributo a ser definido. Os campos de caixa de diálogo \_ e controle \_ identificam o controle de mural e devem corresponder aos campos na [tabela de controle](control-table.md). Por exemplo, a [tabela EventMappings](eventmapping-table.md) a seguir assina um controle para um evento.

    [Tabela EventMappings](eventmapping-table.md) (parcial)

    | caixa de diálogo\_     | controle\_ | Evento       | Atributo |
    |--------------|-----------|-------------|-----------|
    | ActionDialog | Mensagem | Em andamento | Progresso  |

    

     

 

 



