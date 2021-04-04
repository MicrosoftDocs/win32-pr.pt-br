---
description: Definir essa política de sistema por usuário especifica a ordem em que o instalador pesquisa três tipos de fontes.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837403"
---
# <a name="searchorder"></a>SearchOrder

Definir essa [política de sistema](system-policy.md) por usuário especifica a ordem em que o instalador pesquisa três tipos de fontes. Os tipos de fontes são:

"n" – rede

"m" – mídia (CD-ROM ou DVD)

"u" – localizador de recursos uniforme (URL)

Por exemplo, para pesquisar fontes de rede primeiro, as fontes de mídia segundo e as fontes de URL foram definidas pela última vez essa política como um valor de "NMU". Para omitir a pesquisa de um tipo de origem específico, deixe a letra correspondente do valor.

Se SearchOrder não for definido, a ordem de pesquisa padrão será Network, Media e, em seguida, URL.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ sz**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 



