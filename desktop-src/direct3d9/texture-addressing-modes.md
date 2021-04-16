---
description: Seu aplicativo Direct3D pode atribuir coordenadas de textura a qualquer vértice de qualquer primitiva.
ms.assetid: 2e23bcb3-9eba-49d9-93ce-0a4fbb15f746
title: Modos de endereçamento de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ebad5fdb141c41c43c651a2188640d7a6b764e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105765206"
---
# <a name="texture-addressing-modes-direct3d-9"></a>Modos de endereçamento de textura (Direct3D 9)

Seu aplicativo Direct3D pode atribuir coordenadas de textura a qualquer vértice de qualquer primitiva. Para obter detalhes, consulte [coordenadas de textura (Direct3D 9)](texture-coordinates.md). Normalmente, as coordenadas de textura u e v que você atribui a um vértice estão no intervalo de 0.0 a 1.0. No entanto, atribuindo coordenadas de textura fora desse intervalo, você pode criar certos efeitos especiais de texturização.

Você controla o que o Direct3D faz com coordenadas de textura que estão fora do \[ intervalo 0,0, 1,0, \] definindo o modo de endereçamento de textura. Por exemplo, você pode fazer com que seu aplicativo defina o modo de endereçamento de textura de forma que uma textura seja colocada lado a lado em uma primitiva.

O Direct3D permite que os aplicativos executem o encapsulamento de textura. É importante observar que definir o modo de endereçamento de textura como D3DTADDRESS \_ Wrap não é o mesmo que executar o encapsulamento de textura. Definir o modo de endereçamento de textura como D3DTADDRESS \_ Wrap resulta em várias cópias da textura de origem que está sendo aplicada ao primitivo atual e habilitar o encapsulamento de textura altera o modo como o sistema rasteriza polígonos texturizados. Para obter detalhes, consulte [disposição de textura (Direct3D 9)](texture-wrapping.md).

Habilitar o encapsulamento de textura efetivamente faz as coordenadas de textura fora do \[ 0,0, 1,0 \] intervalo inválido, e o comportamento para rasterizar coordenadas de textura de inadimplente é indefinido nesse caso. Quando o encapsulamento de textura está habilitado, os modos de endereçamento de textura não são usados. Tome cuidado para seu aplicativo não especificar coordenadas de textura menores que 0.0 ou maiores que 1.0 quando o encapsulamento de textura estiver habilitado.

## <a name="setting-the-addressing-mode"></a>Configurando o modo de endereçamento

Você pode definir modos de endereçamento de textura para estágios de textura individuais chamando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/desktop/api) . Especifique o identificador de estágio de textura desejado no parâmetro de *amostra* . Defina o parâmetro de *tipo* como D3DSAMP \_ AddressU, D3DSAMP \_ ADDRESSV ou D3DSAMP \_ ADDRESSW Values para atualizar os modos de endereçamento u, v-ou w individualmente. O parâmetro *Value* determina qual modo está sendo definido. Isso pode ser qualquer membro do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) . Para recuperar o modo de endereço de textura atual para um estágio de textura, chame [**IDirect3DDevice9:: Getsamplestate**](/windows/desktop/api), usando os \_ Membros D3DSAMP AddressU, D3DSAMP \_ ADDRESSV ou D3DSAMP \_ ADDRESSW da enumeração [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) para identificar o modo de endereço sobre o qual você deseja obter informações.

## <a name="device-limitations"></a>Limitações do dispositivo

Embora o sistema geralmente permita coordenadas de textura fora do intervalo de 0.0 e 1.0, as limitações do hardware geralmente ditam até que ponto as coordenadas de textura podem se afastar desse intervalo. Um dispositivo de renderização comunica esse limite no membro **MaxTextureRepeat** da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando você recupera os recursos do dispositivo. O valor neste membro descreve o intervalo completo de coordenadas de textura permitidas pelo dispositivo. Por exemplo, se esse valor for 128, as coordenadas de textura de entrada deverão ser mantidas no intervalo de -128.0 a +128.0. Passar vértices com coordenadas de textura fora desse intervalo será inválido. A mesma restrição se aplica às coordenadas de textura geradas como resultado da geração automática de coordenadas de textura e das transformações de coordenadas de textura.

A interpretação de **MaxTextureRepeat** também é afetada pelo \_ bit de recurso D3DPTEXTURECAPS TEXREPEATNOTSCALEDBYSIZE. Quando esse bit é definido, o valor no membro **MaxTextureRepeat** é usado precisamente conforme descrito. No entanto, quando D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE não é definido, as limitações de repetição de textura dependem do tamanho da textura indexada pelas coordenadas de textura. Nesse caso, **MaxTextureRepeat** deve ser dimensionado pelo tamanho atual da textura no maior nível de detalhes para calcular o intervalo de coordenadas de textura válido. Por exemplo, considerando uma dimensão de textura de 32 e **MaxTextureRepeat** de 512, o intervalo de coordenadas de textura válido real é 512/32 = 16, portanto, as coordenadas de textura para esse dispositivo devem estar dentro do intervalo de-16,0 a + 16,0.

Informações adicionais sobre os modos de endereçamento de textura estão contidas nos tópicos a seguir.

-   [Modo de endereço de textura de encapsulamento (Direct3D 9)](wrap-texture-address-mode.md)
-   [Modo de endereço de textura de espelho (Direct3D 9)](mirror-texture-address-mode.md)
-   [Modo de endereço de textura fixe (Direct3D 9)](clamp-texture-address-mode.md)
-   [Modo de endereço de textura de cor da borda (Direct3D 9)](border-color-texture-address-mode.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
