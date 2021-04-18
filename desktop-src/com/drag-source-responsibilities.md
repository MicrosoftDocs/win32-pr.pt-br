---
title: Arrastar responsabilidades de origem
description: Arrastar responsabilidades de origem
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105781317"
---
# <a name="drag-source-responsibilities"></a>Arrastar responsabilidades de origem

A fonte de arrastar é responsável pelas seguintes tarefas:

-   Fornecer um objeto de transferência de dados para o destino de soltura que expõe as interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .
-   Gerando comentários de origem e ponteiro.
-   Determinando quando a operação de arrastar foi cancelada ou uma operação de remoção ocorreu.
-   Executar qualquer ação nos dados originais causados pela operação de remoção, como excluir os dados ou criar um link para ele.

A tarefa principal é criar um objeto de transferência de dados que expõe as interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) . A origem de arrastar pode ou não incluir uma cópia dos dados selecionados. Incluí-lo não é obrigatório, mas isso ajuda a proteger contra alterações inadvertidas e permite que o código de operações da área de transferência seja idêntico ao código de arrastar e soltar.

Enquanto uma operação de arrastar está em andamento, a fonte de arrastar é responsável por definir o ponteiro do mouse e, se apropriado, para fornecer comentários de origem adicionais ao usuário. A fonte de arrastar não pode fornecer comentários que acompanhem a posição do mouse além de definir realmente o ponteiro real (consulte a função [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) ). Essa regra deve ser imposta para evitar conflitos com os comentários fornecidos pelo destino de soltura. (Uma fonte de arrastar também pode ser um destino de soltura. Ao descartar, a origem/destino pode, naturalmente, fornecer comentários de destino para acompanhar a posição do mouse. Nesse caso, no entanto, é a interface "soltar" controlando o mouse, não a origem.) Com base nos comentários oferecidos pelo destino de soltura, a fonte define um ponteiro apropriado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arrastar e soltar](drag-and-drop.md)
</dt> </dl>

 

 