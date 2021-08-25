---
title: A estrutura STGMEDIUM
description: A estrutura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da0adc98b5d774754bd2cbbccb415092d6498684a60189d6346afac82bd270a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992266"
---
# <a name="the-stgmedium-structure"></a>A estrutura STGMEDIUM

assim como a estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) é um aprimoramento do identificador de formato de área de transferência Windows, a estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) é uma melhoria do identificador de memória global usado para transferir os dados. A estrutura **STGMEDIUM** inclui um membro, **TYMED**, que indica o meio a ser usado, e uma União que compreende ponteiros e um identificador para obter qualquer meio especificado em **TYMED**.

A estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permite que as fontes de dados e os consumidores escolham o meio de troca mais eficiente em uma base por renderização. Se os dados forem tão grandes que devem ser mantidos no disco, a fonte de dados poderá indicar uma mídia baseada em disco em seu formato preferencial, usando apenas a memória global como um backup se essa for a única mídia que o consumidor compreende. Ser capaz de usar o melhor meio para trocas, pois o padrão melhora o desempenho geral da troca de dados entre aplicativos. Por exemplo, se alguns dos dados a serem transferidos já estiverem no disco, o aplicativo de origem poderá movê-lo ou copiá-lo para um novo destino, no mesmo aplicativo ou em outros, sem precisar primeiro carregar os dados na memória global. Na extremidade de recebimento, o consumidor dos dados não precisa gravá-lo de volta no disco.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de dados e mídia de transferência](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




