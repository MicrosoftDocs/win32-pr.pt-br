---
title: Adicionando, excluindo e substituindo recursos
description: Este tópico discute como adicionar, excluir ou substituir recursos.
ms.assetid: 15b1086e-e3a2-460a-828b-17db5105309f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c12a1531e422efe44cbd0b3deca9f89838698
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748363"
---
# <a name="adding-deleting-and-replacing-resources"></a>Adicionando, excluindo e substituindo recursos

Os aplicativos sempre devem adicionar, excluir ou substituir recursos em arquivos executáveis. Dois métodos podem ser usados para realizar essas tarefas. A primeira é editar o arquivo de definição de recurso, recompilar os recursos e adicionar os recursos recompilados ao arquivo executável do aplicativo. O segundo método é copiar os dados do recurso diretamente no arquivo executável do aplicativo.

Por exemplo, para localizar um aplicativo em inglês para uso na Noruega, pode ser necessário substituir a caixa de diálogo em inglês por uma usando norueguês. Um desenvolvedor cria uma caixa de diálogo apropriada usando um editor de caixa de diálogo ou escrevendo um modelo no arquivo de definição de recurso. Em seguida, o desenvolvedor recompila os recursos e adiciona os novos recursos ao arquivo executável do aplicativo.

No entanto, se houver uma caixa de diálogo apropriada em formato binário, o desenvolvedor poderá copiar os dados diretamente para o arquivo executável que está sendo localizado usando as funções a seguir. A função [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea) cria um identificador de atualização para o arquivo executável cujos recursos devem ser alterados. A função [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) usa esse identificador para adicionar, excluir ou substituir um recurso no arquivo executável. A função [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) fecha o identificador.

Depois que um identificador de atualização para um arquivo executável é criado pelo [**BeginUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-beginupdateresourcea), um aplicativo pode usar o [**UpdateResource**](/windows/desktop/api/Winbase/nf-winbase-updateresourcea) repetidamente para fazer alterações nos dados do recurso. Cada chamada para **UpdateResource** contribui para uma lista interna de adições, exclusões e substituições, mas na verdade não grava os dados no arquivo executável. Imediatamente antes de fechar o identificador de atualização, o [**EndUpdateResource**](/windows/desktop/api/Winbase/nf-winbase-endupdateresourcea) grava as alterações acumuladas no arquivo executável.

Às vezes, um aplicativo deve copiar recursos de outro arquivo. A [atualização de recursos](using-resources.md) mostra um exemplo de como obter os dados do recurso e seu tamanho de um arquivo.

 

 




