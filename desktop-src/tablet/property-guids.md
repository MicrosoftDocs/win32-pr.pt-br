---
description: Os reconhecedores da Microsoft usam os GUIDs a seguir.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUIDs de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4883ee713122ae36c4ad7e29b86013beb670545ffac31da28bad4da8c2f59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031654"
---
# <a name="property-guids"></a>GUIDs de propriedade

Os reconhecedores da Microsoft usam os GUIDs a seguir. Sempre que possível, os aplicativos devem usar esses GUIDs. No entanto, é esperado e incentivado que outros reconhecedores usarão GUIDs adicionais para propriedades que não têm suporte dos reconhecedores da Microsoft.

Todas as funções de propriedade foram desenvolvidas com a compreensão de que a lista de GUIDs pode ser estendida por outros reconhecedores. Essas funções de propriedade incluem:

-   [**Função GetContextPropertyList**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**Função GetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**Função GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**Função SetContextPropertyValue**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

A tabela a seguir lista os GUIDs de Propriedade do Tablet PC definidos em msinkaut. h (instalado em c: \\ arquivos de programas \\ Microsoft Tablet PC Platform SDK \\ incluem por padrão).



| GUID                                                  | Definição                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| INKRECOGNITIONPROPERTY \_ BOXNUMBER<br/>          | O índice da caixa alternativa do reconhecedor no modo de caixa<br/>                                    |
| INKRECOGNITIONPROPERTY \_ LINENUMBER<br/>         | O número da linha<br/>                                                                   |
| \_segmentação INKRECOGNITIONPROPERTY<br/>       | Como o reconhecedor segmenta palavras e caracteres<br/>                                  |
| INKRECOGNITIONPROPERTY \_ HOTPOINT<br/>           | O ponto de acesso do gesto<br/>                                                             |
| INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT<br/> | Número máximo de traços para um segmento<br/>                                           |
| INKRECOGNITIONPROPERTY \_ POINTSPERINCH<br/>      | A métrica de pontos por polegada<br/>                                                        |
| INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL<br/>    | [**Confiança \_**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) Enumeração de nível<br/>                         |
| INKRECOGNITIONPROPERTY \_ LINEMETRICS<br/>        | Informações para computação de linha de base, Tabs no meio ou Both, que são usadas no malha<br/> |



 

 

 




