---
title: Armazenar variáveis e tipos para sombreadores compartilharem
description: O objeto de vinculação de classe é um namespace para variáveis e tipos que vários sombreadores podem compartilhar.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d40526274ea52d68b0a02dbefd02c116ded77d64e8b343a48abef2735446d971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853166"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Armazenar variáveis e tipos para sombreadores compartilharem

O objeto de vinculação de classe é um namespace para variáveis e tipos que vários sombreadores podem compartilhar. Quando você passa um objeto de vinculação de classe em uma chamada para criar um sombreador, o runtime reúne uma lista de variáveis e tipos que podem implementar cada interface no sombreador e armazena os nomes dessas variáveis e tipos no objeto de vinculação de classe.

Portanto, quando você chama o método [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) para gerar instâncias de classe do objeto de vinculação de classe, o runtime pode recuperar a variável ou o tipo que corresponde ao nome fornecido em cada sombreador (se esse nome for válido para um determinado sombreador) e que é criado com o objeto de vinculação de classe fornecido.

Por exemplo, suponha que você tenha uma **classe Light** que implementa uma interface **Color** e use essa classe em seu sombreador de vértice e sombreador de pixel. Quando você cria um sombreador (por exemplo, chamando [**ID3D11Device::CreatePixelShader),**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)o runtime determina que o tipo de classe **Light** está disponível em sombreadores de vértice e pixel e adiciona o **tipo de** classe Light ao objeto de vinculação de classe. Em seguida,  você pode criar uma instância light em um local desejado, vincular os recursos para ambos os sombreadores e passar essa instância na matriz de instâncias de classe ao definir o sombreador para o dispositivo (por exemplo, chamando [**ID3D11DeviceContext::P SSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)). Em seguida, o runtime executa a seguinte sequência:

1.  Verifica se a instância foi criada com o mesmo objeto de vinculação de classe.
2.  Verifica se o tipo **de classe Light** está em disponibilidade nos sombreadores de vértice e pixel.
3.  Seleciona as tabelas de funções corretas, que podem ser diferentes para os sombreadores de vértice e pixel.
4.  Envia os deslocamentos que a instância fornece.

O objeto de vinculação de classe é, em última análise, um repositório de nomes de tipo e variável. O número máximo de nomes disponíveis para cada item (tipo e variável) é de 64K. Quanto mais longo for o tipo e os nomes de variáveis, maior será o requisito de armazenamento para os metadados de interface armazenados por sombreador. Isso porque o runtime deve armazenar um mapeamento para esses nomes para cada sombreador.

## <a name="related-topics"></a>Tópicos relacionados

[Vinculação dinâmica](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vinculação dinâmica](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 