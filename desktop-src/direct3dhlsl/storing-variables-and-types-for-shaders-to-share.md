---
title: Armazenando variáveis e tipos de sombreadores para compartilhar
description: O objeto de vinculação de classe é um namespace para variáveis e tipos que vários sombreadores podem compartilhar.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967218"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Armazenando variáveis e tipos de sombreadores para compartilhar

O objeto de vinculação de classe é um namespace para variáveis e tipos que vários sombreadores podem compartilhar. Quando você passa um objeto de vinculação de classe em uma chamada para criar um sombreador, o tempo de execução reúne uma lista de variáveis e tipos que podem implementar cada interface no sombreador e armazena os nomes dessas variáveis e tipos no objeto de vinculação de classe.

Portanto, quando você chama o método [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) para gerar instâncias de classe do objeto de vinculação de classe, o tempo de execução pode recuperar a variável ou o tipo que corresponde ao nome que é fornecido em cada sombreador (se esse nome for válido para um determinado sombreador) e criado com o objeto de vinculação de classe fornecido.

Por exemplo, suponha que você tenha uma classe **leve** que implementa uma interface de **cor** e use essa classe no sombreador de vértice e no sombreador de pixel. Quando você cria um sombreador (por exemplo, chamando [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), o tempo de execução determina que o tipo de classe **Light** está disponível em sombreadores de vértices e de pixel e adiciona o tipo de classe **Light** ao objeto de vinculação de classe. Em seguida, você pode criar uma instância **clara** em um local desejado, associar os recursos para os dois sombreadores e passar essa instância na matriz de instâncias de classe ao definir o sombreador para o dispositivo (por exemplo, chamando [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)). Em seguida, o tempo de execução executa a seguinte sequência:

1.  Verifica se a instância foi criada com o mesmo objeto de vinculação de classe.
2.  Verifica se o tipo de classe **leve** é disponível em sombreadores de vértice e de pixel.
3.  Seleciona as tabelas de funções corretas, que podem ser diferentes para os sombreadores de vértice e pixel.
4.  Envia os deslocamentos que a instância fornece.

O objeto de vinculação de classe é, em última instância, um repositório de tipos e nomes de variáveis. O número máximo de nomes disponíveis para cada item (tipo e variável) é 64K. Quanto mais longos forem os nomes de tipo e variável, maior será o requisito de armazenamento para os metadados da interface armazenados por sombreador. Isso ocorre porque o tempo de execução deve armazenar um mapeamento para esses nomes para cada sombreador.

## <a name="related-topics"></a>Tópicos relacionados

[Vinculação dinâmica](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vinculação dinâmica](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 