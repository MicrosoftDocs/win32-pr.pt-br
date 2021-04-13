---
description: Passando objetos como parâmetros
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Passando objetos como parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a58e012138bc65cec481f714ac216bb8227fb924
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501048"
---
# <a name="passing-objects-as-parameters"></a>Passando objetos como parâmetros

O serviço de componentes em fila COM+ não habilita o enfileiramento para todos os componentes COM existentes. Há restrições sobre os tipos de métodos que podem ser enfileirados. Devido a restrições de mensagens, os métodos devem aderir às seguintes regras:

-   Eles devem conter apenas parâmetros de entrada.
-   Eles não devem retornar nenhum resultado específico do aplicativo.

Além disso, há restrições sobre os tipos de parâmetros de entrada que podem ser passados para um componente enfileirado. Em tempo de execução, o serviço de componentes na fila empacota os argumentos no cliente e os passa para o componente de servidor usando o [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)). Tipos simples, como números inteiros e boolianos, podem ser empacotados facilmente — tipos mais complexos não podem ser empacotados sem ajuda.

No caso de passar um objeto por meio de uma chamada de método de componente enfileirada como um parâmetro, o cliente passa o objeto para o gravador. O gravador realiza marshaling do objeto em uma mensagem do serviço de enfileiramento de mensagens e passa-o para o ouvinte. Depois que o ouvinte selecionar a mensagem e passá-la para o Player, o Player deverá recriar a instância do objeto para expedir para a chamada de método especificada pelo cliente. Com base nos tempos de vida do cliente e do servidor em um ambiente em fila, a implicação é que esses objetos devem ser capazes de realizar marshaling por valor. Como o COM+ não fornece semântica de passagem por valor para objetos COM padrão, o gravador e o Player precisam de ajuda do componente para realizar marshaling e Desempacotamento do objeto.

Referências de objeto que dão suporte a [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) podem ser usadas como parâmetros para chamadas de método em componentes em fila. O objeto não pode fazer suposições sobre quando ele será reinstanciado. Por exemplo, o servidor pode estar indisponível ou o componente do servidor pode não ser iniciado até mais tarde no dia. Os objetos que não dão suporte a **IPersistStream** retornarão um erro.

## <a name="visual-basic-persistable-objects"></a>Visual Basic objetos persistentes

O Microsoft Visual Basic 6 permite que objetos persistentes sejam criados. Esses objetos dão suporte a [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) e podem ser passados como parâmetros para chamadas de método de componente em fila. Antes que um objeto de Visual Basic possa ser passado para um componente enfileirado, o objeto persistente deve ser inicializado. Isso pode ser feito de uma das duas maneiras a seguir:

-   Se o aplicativo que cria o objeto persistente for gravado em Visual Basic, o tempo de execução do Visual Basic tratará a inicialização do objeto automaticamente.
-   Se o aplicativo que cria o Visual Basic objeto persistente é escrito em uma linguagem diferente de Visual Basic, como Microsoft Visual C++, o aplicativo deve inicializar explicitamente o componente consultando a interface [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) do objeto persistente ou chamando o método [**IPersistStreamInit:: InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)ou [**IPersistStream:: Load**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load) .

## <a name="ado-recordsets-and-ole-db-rowsets"></a>Conjuntos de linhas de OLE DB e Recordsets ADO

Passar objetos **RECORDSET** ADO ou OLE DB conjunto de linhas entre componentes permite que um componente processe os resultados das consultas executadas por outro componente. Isso é útil ao implantar um aplicativo em vários computadores. Os objetos **Recordset** e Rowset podem ser passados como parâmetros de método para componentes em fila, com as seguintes restrições:

-   Os objetos **Recordset** do lado do servidor não podem ser empacotados usando [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Somente objetos **Recordset** do lado do cliente podem ser passados como parâmetros para uma chamada de método de componente enfileirada.
-   Se você trabalha diretamente com OLE DB, o conjunto de linhas de OLE DB deve ser definido como um conjunto de linhas do lado do cliente.

 

 
