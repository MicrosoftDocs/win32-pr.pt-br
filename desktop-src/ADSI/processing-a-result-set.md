---
title: Processando um conjunto de resultados
description: Um conjunto de resultados é retornado como uma série de linhas.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294498"
---
# <a name="processing-a-result-set"></a>Processando um conjunto de resultados

Um conjunto de resultados é retornado como uma série de linhas. Cada linha pode ou não conter um determinado atributo. Com o provedor de OLE DB, o conjunto de resultados é semelhante a um conjunto de resultados SQL normal. Se você usar ADO para a consulta, o [ADODB. ](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) O objeto Recordset é usado para percorrer o conjunto de resultados. [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponível somente de linguagens que dão suporte a associações vtable) contém membros para mover o cursor de linha e verificar os valores de propriedade em uma determinada linha. Como alternativa, você pode usar [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para obter e definir propriedades.

 

 