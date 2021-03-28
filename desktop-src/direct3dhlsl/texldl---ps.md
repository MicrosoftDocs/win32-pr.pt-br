---
title: texldl-PS
description: Exemplo de uma textura com uma amostra específica. O nível mipmap específico de detalhes que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura. | texldl-PS
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968297"
---
# <a name="texldl---ps"></a>texldl-PS

Exemplo de uma textura com uma amostra específica. O nível mipmap específico de detalhes que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura.

## <a name="syntax"></a>Syntax



| texldl DST, src0, src1 |
|------------------------|



 

Em que:

-   o DST é um registro de destino.
-   src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura. Consulte [registro de coordenadas de textura](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).
-   src1 identifica os registros de amostra de origem \# , em que \# especifica qual número de amostra de textura deve ser amostrado. A amostra está associada a ela uma textura e um estado de controle definido pela enumeração [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por exemplo, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

texldl pesquisa o conjunto de texturas no estágio de amostra referenciado por src1. O nível de detalhe é selecionado em src0. w. Esse valor pode ser negativo, caso o nível de detalhe selecionado seja o inicial um (maior mapa) com o MAGFILTER. Como src0. w é um valor de ponto flutuante, o valor fracionário é usado para interpolar (se MIPFILTER for LINEAR) entre dois níveis de MIP. Os Estados de amostra MIPMAPLODBIAS e MAXMIPLEVEL são respeitados. Para obter mais informações sobre os Estados de amostra, consulte [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Se um programa de sombreador apresentar amostras de uma amostra que não tenha uma textura definida, 0001 será obtido no registro de destino.

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
-   o DST deve ser um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   o DST pode aceitar um writemask. Consulte [máscara de gravação do registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).
-   Os padrões para os componentes ausentes são 0 ou 1 e dependem do formato de textura.
-   src1 deve ser uma [amostra (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ). src1 não pode usar um modificador de negação (consulte [máscara de gravação de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)). src1 pode usar swizzle (consulte [o Swizzling de registro de origem](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)), que é aplicado após a amostragem, mas antes de a máscara de gravação (consulte máscara de gravação do registro de destino) ser respeitada. A amostra deve ter sido declarada (usando o [ \_ SampleType de DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)) no início do sombreador.
-   O número de coordenadas necessárias para executar o exemplo de textura depende de como a amostra foi declarada. Se ele foi declarado como um cubo, uma coordenada de textura de três componentes é necessária (. RGB). A validação impõe que as coordenadas fornecidas para TeX \_ LDL sejam suficientes para a dimensão de textura declarada para a amostra. No entanto, não há garantia de que o aplicativo realmente define uma textura (por meio da API) com dimensões iguais à dimensão declarada para a amostra. Nesse caso, o tempo de execução tentará detectar incompatibilidades (possivelmente em depuração somente). A amostragem de uma textura com menos dimensões do que as presentes na coordenada de textura será permitida e presumida para ignorar os componentes de coordenada de textura extra. Por outro lado, a amostragem de uma textura com mais dimensões do que as presentes na coordenada de textura é inválida.
-   Se o src0 (coordenada de textura) for um [registro temporário](dx9-graphics-reference-asm-ps-registers-temporary.md), os componentes necessários para a pesquisa (descritos acima) deverão ter sido gravados anteriormente.
-   A amostragem de texturas RGB não assinadas resultará em valores flutuantes entre 0,0 e 1,0.
-   As texturas assinadas de amostragem resultarão em valores flutuantes entre-1,0 e 1,0.
-   Durante a amostragem de texturas de ponto flutuante, Float16 significa que os dados serão rangedos no máximo \_ Float16. Float32 significa que o intervalo máximo do pipeline será usado. A amostragem fora de um dos intervalos é indefinida.
-   Não há nenhum limite de leitura dependente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
