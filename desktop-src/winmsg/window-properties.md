---
description: Esta seção discute as propriedades da janela. Uma propriedade de janela é qualquer dado atribuído a uma janela.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowproperties.htm
title: Propriedades da janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82aba0544e1763d36c0378e5d06dc25d48f3297ba8bc8b3bd8687dbba4b0afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200587"
---
# <a name="window-properties"></a>Propriedades da janela

Uma propriedade de janela é qualquer dado atribuído a uma janela. Uma propriedade de janela geralmente é um identificador dos dados específicos da janela, mas pode ser qualquer valor. Cada propriedade de janela é identificada por um nome de cadeia de caracteres.

### <a name="in-this-section"></a>Nesta seção



| Nome                                                       | Descrição                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Sobre as propriedades da janela](about-window-properties.md)     | Discute as propriedades da janela.<br/>                                                   |
| [Usando propriedades de janela](using-window-properties.md)     | Explica como executar as seguintes tarefas associadas às propriedades da janela.<br/> |
| [Referência de propriedade de janela](window-property-reference.md) | Contém a referência de API.<br/>                                                    |



 

### <a name="window-property-functions"></a>Funções de propriedade de janela



| Nome                                   | Descrição                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa)         | Enumera todas as entradas na lista de propriedades de uma janela passando-as, uma a uma, para a função de retorno de chamada especificada. [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) continua até que a última entrada seja enumerada ou a função de retorno de chamada retorna **false**.<br/>                                                                                                        |
| [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa)     | Enumera todas as entradas na lista de propriedades de uma janela passando-as, uma a uma, para a função de retorno de chamada especificada. [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) continua até que a última entrada seja enumerada ou a função de retorno de chamada retorna **false**. <br/>                                                                                                  |
| [**GetProp**](/windows/win32/api/winuser/nf-winuser-getpropa)             | Recupera um identificador de dados da lista de propriedades da janela especificada. A cadeia de caracteres identifica o identificador a ser recuperado. A cadeia de caracteres e o identificador devem ter sido adicionados à lista de propriedades por uma chamada anterior à função [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa) . <br/>                                                                                    |
| [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca)     | Uma função de retorno de chamada definida pelo aplicativo usada com a função [**EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) . A função recebe entradas de propriedade da lista de propriedades de uma janela. O tipo **PROPENUMPROC** define um ponteiro para essa função de retorno de chamada. [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca) é um espaço reservado para o nome da função definida pelo aplicativo. <br/>           |
| [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) | Uma função de retorno de chamada definida pelo aplicativo usada com a função [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) . A função recebe entradas de propriedade da lista de propriedades de uma janela. O tipo **PROPENUMPROCEX** define um ponteiro para essa função de retorno de chamada. [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa) é um espaço reservado para o nome da função definida pelo aplicativo. <br/> |
| [**RemoveProp**](/windows/win32/api/winuser/nf-winuser-removepropa)       | Remove uma entrada da lista de propriedades da janela especificada. A cadeia de caracteres especificada identifica a entrada a ser removida.<br/>                                                                                                                                                                                                                    |
| [**SetProp**](/windows/win32/api/winuser/nf-winuser-setpropa)             | Adiciona uma nova entrada ou altera uma entrada existente na lista de propriedades da janela especificada. A função adicionará uma nova entrada à lista se a cadeia de caracteres especificada já não existir na lista. A nova entrada contém a cadeia de caracteres e o identificador. Caso contrário, a função substituirá o identificador atual da cadeia de caracteres pelo identificador especificado. <br/> |



 

 

 
