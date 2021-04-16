---
description: Esse evento notifica o controle Directorylist que uma nova pasta deve ser criada; Ele cria a nova pasta e seleciona o campo nome da pasta para edição.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768470"
---
# <a name="directorylistnew-controlevent"></a>DirectoryListNew ControlEvent,

Esse evento notifica o [controle directorylist](directorylist-control.md) que uma nova pasta deve ser criada; Ele cria a nova pasta e seleciona o campo nome da pasta para edição. O nome padrão da nova pasta pode ser criado na [tabela UIText](uitext-table.md). Insira "NewFolder" na coluna de chave. Insira o valor para o nome padrão da nova pasta na coluna de texto. Esse valor deve estar na forma de um tipo de dados de coluna de [nome de arquivo](filename.md) e usar a \| sintaxe SFN LFN. Se esse valor não estiver presente na tabela UIText ou for um valor inválido, o instalador usará um valor padrão de "Fldr \| nova pasta". Para obter informações relacionadas, consulte [caixa de diálogo Procurar](browse-dialog.md).

Esse evento deve ser publicado por um [controle de pressão](pushbutton-control.md) localizado na mesma caixa de diálogo que o controle assinando esse evento. O evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).

Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário. Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md). Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).

Observe que, se esse ControlEvent, for chamado novamente quando uma nova pasta já existir, uma segunda pasta nova não será criada. Nesse caso, chamar DirectoryListNew seleciona o nome da nova pasta existente para edição.

## <a name="published-by"></a>Publicada por

[Directorylist](directorylist-control.md)

## <a name="argument"></a>Argumento

Este ControlEvent, não usa um argumento.

## <a name="action-on-subscribers"></a>Ação nos assinantes

Este ControlEvent, não executa uma ação nos assinantes.

## <a name="typical-use"></a>Usos comum

Um controle de [supressão](pushbutton-control.md) na mesma caixa de diálogo modal que a directorylist é usado para disparar a criação de uma nova pasta.

 

 



