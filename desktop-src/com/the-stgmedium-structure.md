---
title: A estrutura STGMEDIUM
description: A estrutura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104008582"
---
# <a name="the-stgmedium-structure"></a>A estrutura STGMEDIUM

Assim como a estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) é um aprimoramento do identificador de formato da área de transferência do Windows, a estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) é uma melhoria do identificador de memória global usado para transferir os dados. A estrutura **STGMEDIUM** inclui um membro, **TYMED**, que indica o meio a ser usado, e uma União que compreende ponteiros e um identificador para obter qualquer meio especificado em **TYMED**.

A estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permite que as fontes de dados e os consumidores escolham o meio de troca mais eficiente em uma base por renderização. Se os dados forem tão grandes que devem ser mantidos no disco, a fonte de dados poderá indicar uma mídia baseada em disco em seu formato preferencial, usando apenas a memória global como um backup se essa for a única mídia que o consumidor compreende. Ser capaz de usar o melhor meio para trocas, pois o padrão melhora o desempenho geral da troca de dados entre aplicativos. Por exemplo, se alguns dos dados a serem transferidos já estiverem no disco, o aplicativo de origem poderá movê-lo ou copiá-lo para um novo destino, no mesmo aplicativo ou em outros, sem precisar primeiro carregar os dados na memória global. Na extremidade de recebimento, o consumidor dos dados não precisa gravá-lo de volta no disco.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formatos de dados e mídia de transferência](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




