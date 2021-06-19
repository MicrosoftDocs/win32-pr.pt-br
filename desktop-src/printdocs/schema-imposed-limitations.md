---
description: Saiba mais sobre as limitações impostas pelo esquema de PrintCapabilities. O provedor de PrintCapabilities deve detectar inválidas de configurações e resolvê-las.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitações de Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404919"
---
# <a name="schema-imposed-limitations"></a>Limitações de Schema-Imposed

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

O esquema de PrintCapabilities fornece aos autores de PrintCapabilities uma quantidade significativa de flexibilidade e expressividade que pode ser utilizada em descrições de dispositivos. No entanto, as dependências de configuração impõem uma limitação nessa flexibilidade e na expressividade. Instâncias de ParameterDef, a lista de elementos de recurso, a lista de instâncias de opção dentro de cada recurso e as instâncias de ScoredProperty dentro de cada opção não devem conter dependências de configuração. O provedor de documentos PrintCapabilities deve detectar combinações inválidas de configurações e deve resolvê-las.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



