---
description: ICE29 valida se os nomes de fluxo truncados permanecem exclusivos. Qualquer tabela que tenha uma coluna binária ou de objeto é validada. Consulte o tipo de dados coluna binária.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f606bd09314d045b643816c08349eba38bde72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921373"
---
# <a name="ice29"></a>ICE29

ICE29 valida se os nomes de fluxo truncados permanecem exclusivos. Qualquer tabela que tenha uma coluna binária ou de objeto é validada. Consulte o tipo de dados coluna [binária](binary.md) .

A manipulação de fluxos pela implementação de armazenamento estruturado OLE do Win32 limita os nomes de fluxo. Consulte [limitações de OLE em fluxos](ole-limitations-on-streams.md). O instalador pode compactar nomes de fluxo de até 62 caracteres de comprimento. Nomes maiores que isso são truncados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



