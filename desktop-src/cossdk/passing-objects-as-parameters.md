---
description: Passando objetos como parâmetros
ms.assetid: 174847c8-4545-4f61-ae13-42bdec1405e7
title: Passando objetos como parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47669d3e3e5af572b6dfd50dcbbefacf5c008971f276408fa87b37ccbed9a1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070376"
---
# <a name="passing-objects-as-parameters"></a>Passando objetos como parâmetros

O serviço de componentes em fila COM+ não habilita a fila para todos os componentes COM existentes. Há restrições nos tipos de métodos que podem ser en fila. Devido a restrições de mensagens, os métodos devem seguir as seguintes regras:

-   Eles devem conter apenas parâmetros de entrada.
-   Eles não devem retornar nenhum resultado específico do aplicativo.

Além disso, há restrições nos tipos de parâmetros de entrada que podem ser passados para um componente na fila. Em tempo de operação, o serviço componentes na fila em pacotes os argumentos no cliente e os passa para o componente do servidor usando o [En enxadamento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)). Tipos simples, como inteiros e boolianas, podem ser empacotados facilmente– tipos mais complexos não podem ser empacotados sem ajuda.

No caso de passar um objeto por meio da chamada de método de um componente na fila como um parâmetro, o cliente passa o objeto para o gravador. O gravador faz marshaling do objeto em uma mensagem de En fila de mensagens e o passa para o ouvinte. Depois que o ouvinte pegar a mensagem e passá-la para o player, o jogador deverá reinstantir o objeto para expedi-lo para a chamada de método especificada pelo cliente. Com base nos tempo de vida do cliente e do servidor em um ambiente na fila, a implicação é que esses objetos devem ser capazes de marshalar por valor. Como o COM+ não fornece semântica de passagem por valor para objetos COM padrão, o gravador e o player precisam de ajuda do componente para fazer marshal e desmarcar o objeto.

Referências de objeto que suportam [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) podem ser usadas como parâmetros para chamadas de método em componentes na fila. O objeto não pode fazer suposições sobre quando ele será reinstantido. Por exemplo, o servidor pode estar indisponível ou o componente do servidor pode não ser iniciado até mais tarde no dia. Objetos que não são **suportados por IPersistStream** retornarão um erro.

## <a name="visual-basic-persistable-objects"></a>Visual Basic Objetos persistentes

O Microsoft Visual Basic 6 permite que objetos persistentes sejam criados. Esses objetos são [**suportados por IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) e podem ser passados como parâmetros para chamadas de método de componente na fila. Antes que Visual Basic objeto possa ser passado para um componente na fila, o objeto persistente deve ser inicializado. Isso pode ser feito de uma das duas maneiras a seguir:

-   Se o aplicativo que cria o objeto persistente for gravado Visual Basic, o runtime Visual Basic manipulará a inicialização do objeto automaticamente.
-   Se o aplicativo que cria o objeto persistente do Visual Basic for escrito em uma linguagem diferente de Visual Basic, como Microsoft Visual C++, o aplicativo deverá inicializar explicitamente o componente consultando a interface [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) do objeto persistente ou chamando o método [**IPersistStreamInit::InitNew**](/windows/desktop/api/ocidl/nf-ocidl-ipersiststreaminit-initnew)ou [**IPersistStream::Load.**](/windows/desktop/api/objidl/nf-objidl-ipersiststream-load)

## <a name="ado-recordsets-and-ole-db-rowsets"></a>Conjuntos de registros ADO e OLE DB linhas

Passar o ADO **Recordset** ou OLE DB de conjuntos de linhas entre componentes permite que um componente processe os resultados de consultas executadas por outro componente. Isso é útil ao implantar um aplicativo em vários computadores. **Os objetos de conjuntos** de registros e de conjuntos de linhas podem ser passados como parâmetros de método para componentes na fila, com as seguintes restrições:

-   Os objetos **doEt de Registros** do lado do servidor não podem ser marshalados usando [**IPersistStream.**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) Somente objetos do **Recordset do** lado do cliente podem ser passados como parâmetros para uma chamada de método de componente na fila.
-   Se você trabalhar diretamente com OLE DB, o OLE DB de linhas deverá ser definido como um conjuntos de linhas do lado do cliente.

 

 
