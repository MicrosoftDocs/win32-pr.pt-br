---
description: ICE29 valida que os nomes de fluxo truncado permanecem exclusivos. Qualquer tabela que tenha uma coluna Binary ou Object é validada. Consulte o tipo de dados Coluna binária.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdef203e314a087e9eb11bcf1b958425d7608028d979db925edce1b42e4bebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528706"
---
# <a name="ice29"></a>ICE29

ICE29 valida que os nomes de fluxo truncado permanecem exclusivos. Qualquer tabela que tenha uma coluna Binary ou Object é validada. Consulte o [tipo de dados Coluna](binary.md) binária.

A manipulação de fluxos pela implementação de armazenamento estruturado OLE win32 limita os nomes de fluxo. Consulte [Limitações do OLE Fluxos](ole-limitations-on-streams.md). O instalador pode compactar nomes de fluxo de até 62 caracteres. Nomes maiores do que esse são truncados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



