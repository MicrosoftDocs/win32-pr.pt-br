---
title: Como fazer uma instância de um sombreador de geometria
description: A instanciação do sombreador de geometria permite que várias execuções do mesmo sombreador de geometria sejam executadas por primitivo.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 866b0cedb4de0fe2f8bf9087df6637d3a6340505289b4b773eaccd380fa4b367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067916"
---
# <a name="how-to-instance-a-geometry-shader"></a>Como: instância de um sombreador de geometria

A instanciação do sombreador de geometria permite que várias execuções do mesmo sombreador de geometria sejam executadas por primitivo. Para fazer uma instância de um sombreador de geometria, adicione um atributo de instância à função principal de sombreador e identifique um parâmetro de índice de instância no corpo da função de sombreador.

Para fazer uma instância de um sombreador geometry:

1.  Adicione o [atributo de instância](sm5-attributes-instance.md) à função principal.

    ```
    [instance(24)]
    ```

    

    Isso define o número de instâncias (um máximo de 32) a serem executadas para cada primitiva.

2.  Anexe o valor do sistema [ \_ GSInstanceID VA](sv-gsinstanceid.md) a uma variável na lista de parâmetros de função que pode ser usada para rastrear a ID da instância que está sendo executada.
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  Compile e crie o sombreador da mesma forma que faria com qualquer outro sombreador de geometria.

Outros detalhes incluem:

-   A contagem máxima de instâncias é 32.
-   A contagem máxima de vértices é uma contagem máxima de vértice por instância.
-   Cada invocação de instância (como qualquer invocação de sombreador de geometria) aumenta a contagem de invocação e gera um RestartStrip implícito ().

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do sombreador de geometria](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




