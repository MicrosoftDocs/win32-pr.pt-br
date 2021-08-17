---
title: texldl – ps
description: Amostra de uma textura com um exemplo específico. O nível de detalhes do mipmap específico que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura. | texldl – ps
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f66bc54f00e5eb560589429f1cb116183e165a36d90f5d560d8895678a2d5bad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723173"
---
# <a name="texldl---ps"></a>texldl – ps

Amostra de uma textura com um exemplo específico. O nível de detalhes do mipmap específico que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura.

## <a name="syntax"></a>Syntax



| texldl dst, src0, src1 |
|------------------------|



 

Em que:

-   dst é um registro de destino.
-   src0 é um registro de origem que fornece as coordenadas de textura para a amostra de textura. Consulte [Registro de coordenadas de textura.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifica o registro de amostra de origem (s), em que especifica qual número de \# amostra de textura deve ser \# amostrado. O amostrador associou a ela uma textura e um estado de controle definidos pela enumeração [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por exemplo, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

O texldl procura o conjunto de texturas no estágio de amostra referenciado por src1. O nível de detalhes é selecionado em src0.w. Esse valor pode ser negativo; nesse caso, o nível de detalhes selecionado é o zero (maior mapa) com o MAGFILTER. Como src0.w é um valor de ponto flutuante, o valor fracionado é usado para interpolar (se MIPFILTER for LINEAR) entre dois níveis mip. Os estados de amostra MIPMAPLODBIAS e MAXMIPLEVEL são considerados. Para obter mais informações sobre estados de amostra, [**consulte D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Se um programa de sombreador amostra de um exemplo que não tem um conjunto de textura, 0001 é obtido no registro de destino.

Veja a seguir um algoritmo aproximado que o dispositivo de referência segue:


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



Restrições:

-   As coordenadas de textura não devem ser dimensionadas pelo tamanho da textura.
-   dst deve ser um [Registro Temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   dst pode aceitar uma máscara de gravação. Consulte [Máscara de Gravação do Registro de Destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).
-   Os padrões para componentes ausentes são 0 ou 1 e dependem do formato de textura.
-   src1 deve ser um [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ). src1 não pode usar um modificador de negação (consulte [Máscara de Gravação do Registro de Destino).](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) o src1 pode usar swizzle (consulte Origem do Registro de [Swizzling),](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)que é aplicado após a amostragem, mas antes que a máscara de gravação (consulte Máscara de Gravação do Registro de Destino) seja acodadas. O sampler deve ter sido declarado (usando [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)) no início do sombreador.
-   O número de coordenadas necessárias para executar a amostra de textura depende de como o sampler foi declarado. Se ele tiver sido declarado como um cubo, uma coordenada de textura de três componentes será necessária (.rgb). A validação impõe que as coordenadas fornecidas ao tex ldl sejam suficientes para \_ a dimensão de textura declarada para o exemplo. No entanto, não há garantia de que o aplicativo realmente define uma textura (por meio da API) com dimensões iguais à dimensão declarada para o exemplo. Nesse caso, o runtime tentará detectar incompatibilidades (possivelmente apenas em depuração). A amostragem de uma textura com menos dimensões do que estão presentes na coordenada de textura será permitida e presumida para ignorar os componentes de coordenadas de textura extras. Por outro lado, a amostragem de uma textura com mais dimensões do que as presentes na coordenada de textura é ilegal.
-   Se o src0 (coordenada de textura) for [Registro](dx9-graphics-reference-asm-ps-registers-temporary.md)Temporário, os componentes necessários para a busca (descritos acima) deverão ter sido gravados anteriormente.
-   A amostragem de texturas RGB não atribuídas resultará em valores float entre 0,0 e 1,0.
-   A amostragem de texturas assinadas resultará em valores float entre -1,0 e 1,0.
-   Ao amostragem de texturas de ponto flutuante, Float16 significa que os dados serão intervalos dentro de MAX \_ FLOAT16. Float32 significa que o intervalo máximo do pipeline será usado. A amostragem fora de qualquer intervalo é indefinida.
-   Não há nenhum limite de leitura dependente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
