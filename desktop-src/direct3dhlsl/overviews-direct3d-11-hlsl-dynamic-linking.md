---
title: Vinculação dinâmica
description: Os desenvolvedores de gráficos às vezes criam sombreadores grandes e de uso geral que podem ser usados por uma ampla variedade de itens de cena.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636022"
---
# <a name="dynamic-linking"></a>Vinculação dinâmica

Os desenvolvedores de gráficos às vezes criam sombreadores grandes e de uso geral que podem ser usados por uma ampla variedade de itens de cena. Em tempo de execução, o sombreador Executa condicionalmente o código apropriado para a situação em questão. Infelizmente, esses sombreadores grandes de uso geral usam GPRs (registros de uso geral) de forma ineficiente e podem ser muito mais lentos do que os sombreadores menores e mais direcionados.

O modelo de sombreador 5 aborda esse problema de desempenho introduzindo a vinculação dinâmica de sombreador. A vinculação dinâmica separa os fragmentos de código do sombreador usando interfaces e funções virtuais e permite que o aplicativo selecione o fragmento a ser usado no momento do desenho. Isso melhora o desempenho ligando apenas o código do sombreador necessário e não todo o sombreador de uso geral grande.

## <a name="in-this-section"></a>Nesta seção



| Item                                                                                                                                                                                                                                                                                                                         | Descrição                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Armazenando variáveis e tipos de sombreadores para compartilhar](storing-variables-and-types-for-shaders-to-share.md)<br/> | Descreve o objeto de vinculação de classe para armazenar variáveis e tipos que vários sombreadores podem compartilhar.<br/> |
| <span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces e classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)<br/>                                                                                                         | Descreve como usar interfaces e classes HLSL para implementar a vinculação dinâmica.<br/>                           |
| <span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Restrições de uso de interface](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)<br/>                                                                            | Descreve as restrições sobre o uso de interfaces no código de sombreador.<br/>                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[HLSL](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





