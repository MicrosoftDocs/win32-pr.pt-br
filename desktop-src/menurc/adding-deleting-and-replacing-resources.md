---
title: Adicionando, excluindo e substituindo recursos
description: Este tópico discute como adicionar, excluir ou substituir recursos.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c23375dbfff770a22b96ef7cb517af1c0b8d40579d6919a31a8136e1691474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118735289"
---
# <a name="adding-deleting-and-replacing-resources"></a>Adicionando, excluindo e substituindo recursos

Com frequência, os aplicativos devem adicionar, excluir ou substituir recursos em arquivos executáveis. Dois métodos podem ser usados para realizar essas tarefas. A primeira é editar o arquivo de definição de recurso, recompilar os recursos e adicionar os recursos recompilados ao arquivo executável do aplicativo. O segundo método é copiar os dados do recurso diretamente para o arquivo executável do aplicativo.

Por exemplo, para localizar um aplicativo em inglês para uso na Noruega, pode ser necessário substituir a caixa de diálogo inglês por uma usando o norueguês. Um desenvolvedor cria uma caixa de diálogo apropriada usando um editor de caixa de diálogo ou escrevendo um modelo no arquivo de definição de recurso. Em seguida, o desenvolvedor recompila os recursos e adiciona os novos recursos ao arquivo executável do aplicativo.

Se uma caixa de diálogo apropriada existir em formato binário, no entanto, o desenvolvedor poderá copiar os dados diretamente para o arquivo executável que está sendo localizado usando as funções a seguir. A [**função BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) cria um alçamento de atualização para o arquivo executável cujos recursos devem ser alterados. A [**função UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) usa esse alça para adicionar, excluir ou substituir um recurso no arquivo executável. A [**função EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) fecha o alçamento.

Depois que um alça de atualização para um arquivo executável é criado por [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea), um aplicativo pode usar [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) repetidamente para fazer alterações nos dados do recurso. Cada chamada para **UpdateResource** contribui para uma lista interna de adições, exclusões e substituições, mas na verdade não escreve os dados no arquivo executável. Imediatamente antes de fechar o alça de atualização, [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) grava as alterações acumuladas no arquivo executável.

Às vezes, um aplicativo deve copiar recursos de outro arquivo. [Atualizar recursos mostra](using-resources.md) um exemplo de como obter os dados do recurso e seu tamanho de um arquivo.

 

 




