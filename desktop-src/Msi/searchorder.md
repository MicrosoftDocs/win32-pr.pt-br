---
description: Definir essa política de sistema por usuário especifica a ordem em que o instalador pesquisa três tipos de fontes.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaab6ff8d4b40b966b5ab1785ddd5fd473316732833fc32be7102acaa7c4877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041036"
---
# <a name="searchorder"></a>SearchOrder

Definir essa [política de sistema](system-policy.md) por usuário especifica a ordem em que o instalador pesquisa três tipos de fontes. Os tipos de fontes são:

"n" – rede

"m" – mídia (CD-ROM ou DVD)

"u" – localizador de recursos uniforme (URL)

Por exemplo, para pesquisar fontes de rede primeiro, as fontes de mídia segundo e as fontes de URL foram definidas pela última vez essa política como um valor de "NMU". Para omitir a pesquisa de um tipo de origem específico, deixe a letra correspondente do valor.

Se SearchOrder não for definido, a ordem de pesquisa padrão será Network, Media e, em seguida, URL.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ atuais \_** políticas de Software de usuário \\  \\  \\ **do Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ sz**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 



