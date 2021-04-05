---
description: ICE09 valida que o bit permanente está definido para cada componente marcado para instalação no SystemFolder.
ms.assetid: b4e11d75-4214-49de-ac12-6f360771ad73
title: ICE09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01cd20a1b354888877be0f5d456b6d6af2bdec82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662532"
---
# <a name="ice09"></a>ICE09

ICE09 valida que o bit permanente está definido para cada componente marcado para instalação no SystemFolder. O ICE09 posta um aviso porque você deve evitar a instalação de componentes do sistema não permanentes no SystemFolder. Para evitar esse aviso, defina o bit permanente na coluna atributos da tabela de [componentes](component-table.md) para cada componente que está marcado para instalação no SystemFolder. Nenhuma validação será feita se o banco de dados não tiver uma tabela de componentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



