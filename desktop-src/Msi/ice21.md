---
description: ICE21 valida que cada componente na tabela de componentes pertence a um recurso. Ele usa a tabela FeatureComponents para verificar esse mapeamento.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753448"
---
# <a name="ice21"></a>ICE21

ICE21 valida que cada componente na tabela de [componentes](component-table.md) pertence a um recurso. Ele usa a [tabela FeatureComponents](featurecomponents-table.md) para verificar esse mapeamento.

## <a name="result"></a>Resultado

ICE21 posta uma mensagem de erro se o pacote de instalação contiver um componente que não pertence a um recurso.

## <a name="example"></a>Exemplo

Para o exemplo a seguir, ICE21 posta uma mensagem de erro informando que o componente comp1 não é mapeado para nenhum recurso.

[Tabela de componentes](component-table.md) (parcial)



| Componente |
|-----------|
| Comp1     |
| Comp2     |



 

[Tabela FeatureComponents](featurecomponents-table.md) (parcial)



| Recurso  | Componente |
|----------|-----------|
| Feature1 | Comp2     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



