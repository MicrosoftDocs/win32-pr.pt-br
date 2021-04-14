---
description: Uma caixa de diálogo de procura permite que o usuário selecione um diretório. O diretório não precisa existir e pode ser criado usando esse controle.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Procurar caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370695"
---
# <a name="browse-dialog"></a>Procurar caixa de diálogo

Uma caixa de diálogo de procura permite que o usuário selecione um diretório. O diretório não precisa existir e pode ser criado usando esse controle.

Esse tipo de caixa de diálogo normalmente contém os três controles a seguir. Esses controles são conectados à mesma propriedade. Essa propriedade é o caminho que está sendo selecionado.

-   Um [controle PathEdit](pathedit-control.md) para selecionar a seção final do caminho. Esse controle não pode perder o foco se a parte final inserida não for válida no volume atual.
-   Um [controle DirectoryCombo](directorycombo-control.md) para mostrar o caminho selecionado no momento que é exibido pelo controle PathEdit. Esse controle não mostra o último segmento do caminho.
-   Um [controle directorylist](directorylist-control.md) para mostrar as pastas abaixo do diretório exibido atualmente pelo DirectoryCombo. Isso também pode mostrar uma pasta que ainda não foi criada.

Uma caixa de diálogo de procura geralmente contém um [controle DirectoryCombo](directorycombo-control.md) que especifica os tipos de volume a serem exibidos. É comum que todos os tipos de volumes sejam exibidos em uma caixa de diálogo de procura.

As caixas de diálogo de procura normalmente contêm três [controles de pressão](pushbutton-control.md). Esses botões estão vinculados a seus respectivos ControlEvents na [tabela ControlEvent,](controlevent-table.md). Esses botões são usados para ativar as opções de controle a seguir.



| Opção de controle | ControlEvent                                            |
|----------------|---------------------------------------------------------|
| Um nível acima   | [DirectoryListUp](directorylistup-controlevent.md)     |
| Nova Pasta     | [DirectoryListNew](directorylistnew-controlevent.md)   |
| Aberto           | [DirectoryListOpen](directorylistopen-controlevent.md) |



 

Para que a nova opção de pasta funcione com um nome de pasta não padrão, o caminho da nova pasta deve ser especificado na [tabela UIText](uitext-table.md). A cadeia de caracteres de caminho deve usar o formulário "nome de arquivo longo do nome de arquivo curto \| " para o nome do arquivo. Por exemplo, use um nome de arquivo como "myprod ~ 1 \| meu produto fabuloso". Confira o tipo de dados coluna de [nome](filename.md) de arquivo para obter mais informações sobre o formato de nome. Se o caminho não estiver presente na tabela UIText ou se estiver definido como um valor inválido, ele será definido como um valor de "Fldr \| nova pasta" por padrão. O botão **nova pasta** pode ser omitido se a caixa de diálogo precisar apenas pesquisar pastas existentes.

 

 



