---
title: texldl-vs
description: Exemplo de uma textura com uma amostra específica. O nível mipmap específico de detalhes que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b06d9529d4f7e6bf8e44339290855d50e6668d67f56305fbc3bbeb77ad4b217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787846"
---
# <a name="texldl---vs"></a>texldl-vs

Exemplo de uma textura com uma amostra específica. O nível mipmap específico de detalhes que está sendo amostrado deve ser especificado como o quarto componente da coordenada de textura.

## <a name="syntax"></a>Syntax



| texldl DST, src0, src1 |
|------------------------|



 

Em que:

-   o DST é um registro de destino.
-   src0 é um registro de origem que fornece as coordenadas de textura para o exemplo de textura.
-   src1 identifica os registros de amostra de origem \# , em que \# especifica qual número de amostra de textura deve ser amostrado. A amostra está associada a ela uma textura e um estado de controle definido pela enumeração [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por exemplo, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| texldl                 |      |      |      |       | x    | x     |



 

texldl pesquisa o conjunto de texturas no estágio de amostra referenciado por src1. O nível de detalhe é selecionado em src0. w. Esse valor pode ser negativo; nesse caso, o nível de detalhe selecionado é o "inicial One" (maior mapa) com o MAGFILTER. Como src0. w é um valor de ponto flutuante, o valor fracionário é usado para interpolar (se MIPFILTER for LINEAR) entre dois níveis de MIP. Os Estados de amostra MIPMAPLODBIAS e MAXMIPLEVEL são respeitados. Para obter mais informações sobre os Estados de amostra, consulte [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Se um programa de sombreador apresentar amostras de uma amostra que não tenha uma textura definida, 0001 será obtido no registro de destino.

Essa é uma aproximação para o algoritmo do dispositivo de referência.


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
   LOD = MAX( MAXMIPLEVEL, LOD);
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
-   o DST deve ser um [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).
-   o DST pode aceitar uma máscara de gravação. Consulte [máscara de registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).
-   Os padrões para os componentes ausentes são 0 ou 1 e dependem do formato de textura.
-   src1 deve ser uma [amostra (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# ). src1 não pode usar um modificador de negação. src1 pode usar swizzle, que é aplicado após a amostragem antes que a máscara de gravação seja respeitada. A amostra deve ter sido declarada (usando o [ \_ SampleType de DCL (SM3-vs ASM)](dcl-samplertype---vs.md)) no início do sombreador.
-   O número de coordenadas necessárias para executar o exemplo de textura depende de como a amostra foi declarada. Se ele foi declarado como um cubo, uma coordenada de textura de três componentes é necessária (. RGB). A validação impõe que as coordenadas fornecidas para texldl sejam suficientes para a dimensão de textura declarada para a amostra. No entanto, não é garantido que o aplicativo realmente defina uma textura (por meio da API) com dimensões iguais à dimensão declarada para a amostra. Nesse caso, o tempo de execução tentará detectar incompatibilidades (possivelmente em depuração somente). A amostragem de uma textura com menos dimensões do que as presentes na coordenada de textura será permitida e será considerada para ignorar os componentes de coordenadas de textura extras. Por outro lado, a amostragem de uma textura com mais dimensões do que as presentes na coordenada de textura não é permitida.
-   Se o src0 (coordenada de textura) for um [registro temporário](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), os componentes necessários para a pesquisa (descritos acima) deverão ter sido gravados anteriormente.
-   A amostragem de texturas RGB não assinadas resultará em valores flutuantes entre 0,0 e 1,0.
-   As texturas assinadas de amostragem resultarão em valores flutuantes entre-1,0 e 1,0.
-   Quando texturas de ponto flutuante de amostragem, Float16 significa que os dados serão rangedos no máximo \_ Float16. Float32 significa que o intervalo máximo do pipeline será usado. A amostragem fora de um dos intervalos é indefinida.
-   Não há nenhum limite de leitura dependente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
