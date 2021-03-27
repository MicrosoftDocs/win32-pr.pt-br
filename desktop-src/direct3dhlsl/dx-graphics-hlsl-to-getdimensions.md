---
title: GetDimensions (objeto de textura DirectX HLSL)
description: Obtém informações de tamanho da textura. O bloco de sintaxe mostra todos os parâmetros que são possíveis na declaração do método. A tabela na seção de comentários mostra quais parâmetros são implementados para cada tipo de objeto de textura.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823442"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>GetDimensions (objeto de textura DirectX HLSL)

Obtém informações de tamanho da textura. O bloco de sintaxe mostra todos os parâmetros que são possíveis na declaração do método. A tabela na seção de comentários mostra quais parâmetros são implementados para cada tipo de objeto de textura.



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| void Object. GetDimensions (UINT MipLevel, largura de typeX, altura de typeX, elementos typeX, profundidade de typeX, typeX NumberOfLevels, typeX NumberOfSamples); |



 

typeX denota que há dois tipos possíveis: **uint** ou **float**.

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                               | Descrição                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*<br/>                                     | Qualquer tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) , exceto um objeto de **buffer** .<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*<br/>                             | \[em \] um índice de base zero que identifica o nível de mipmap. Se esse argumento não for usado, o primeiro nível de MIP será assumido.<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Largura*<br/>                                         | \[fora \] da largura da textura, em texels.<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Tamanho*<br/>                                     | \[fora \] da altura da textura, em texels.<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elementos*<br/>                             | \[\]o número de elementos em uma matriz.<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Detalhado*<br/>                                         | \[\]a profundidade da textura, em texels.<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*<br/>     | \[\]o número de níveis de mipmap.<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*<br/> | \[\]o número de amostras.<br/>                                                                                            |



 

## <a name="return-value"></a>Valor Retornado

Nenhum

## <a name="overloaded-methods"></a>Métodos sobrecarregados

Esta tabela lista todas as versões diferentes do método; as versões são diferentes pelo número de parâmetros de entrada. Observe que, para cada método que usa parâmetros inteiros, há um método sobrecarregado que usa parâmetros de ponto flutuante.



| Tipo de Texture-Object | Parâmetros de Entrada                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | UINT MipLevel, largura UINT, NumberOfLevels UINT                                 |
| Texture1D           | Largura de UINT                                                                     |
| Texture1D           | UINT MipLevel, largura flutuante, NumberOfLevels flutuante                               |
| Texture1D           | Largura flutuante                                                                    |
| Texture1DArray      | UINT MipLevel, largura UINT, elementos UINT, NumberOfLevels UINT                  |
| Texture1DArray      | Elementos de largura UINT, UINT                                                      |
| Texture1DArray      | UINT MipLevel, largura flutuante, elementos float, NumberOfLevels flutuante               |
| Texture1DArray      | Largura flutuante, elementos float                                                    |
| Texture2D           | UINT MipLevel, largura UINT, altura UINT, NumberOfLevels UINT                    |
| Texture2D           | Largura UINT, altura UINT                                                        |
| Texture2D           | UINT MipLevel, largura de flutuação, altura flutuante, NumberOfLevels flutuante                 |
| Texture2D           | Largura flutuante, altura flutuante                                                      |
| Texture2DArray      | UINT MipLevel, largura UINT, altura UINT, elementos UINT, NumberOfLevels UINT     |
| Texture2DArray      | Largura de UINT, altura UINT, elementos UINT                                         |
| Texture2DArray      | UINT MipLevel, largura flutuante, altura flutuante, elementos float, NumberOfLevels flutuante |
| Texture2DArray      | Largura float, altura flutuante, elementos float                                      |
| Texture3D           | UINT MipLevel, largura UINT, altura UINT, profundidade UINT, NumberOfLevels UINT        |
| Texture3D           | Largura UINT, altura UINT, profundidade de UINT                                            |
| Texture3D           | UINT MipLevel, largura flutuante, altura flutuante, profundidade flutuante, NumberOfLevels flutuante    |
| Texture3D           | Largura de flutuação, altura flutuante, profundidade de flutuação                                         |
| TextureCube         | UINT MipLevel, largura UINT, altura UINT, NumberOfLevels UINT                    |
| TextureCube         | Largura UINT, altura UINT                                                        |
| TextureCube         | UINT MipLevel, largura flutuante, altura flutuante, NumberOfLevels UINT                  |
| TextureCube         | Largura flutuante, altura flutuante                                                      |
| TextureCubeArray    | UINT MipLevel, largura UINT, altura UINT, elementos UINT, NumberOfLevels UINT     |
| TextureCubeArray    | Largura de UINT, altura UINT, elementos UINT                                         |
| TextureCubeArray    | UINT MipLevel, largura flutuante, altura flutuante, elementos float, NumberOfLevels flutuante |
| TextureCubeArray    | Largura float, altura flutuante, elementos float                                      |
| Texture2DMS         | Largura UINT, altura UINT, amostras UINT                                          |
| Texture2DMS         | Largura float, altura float, amostras float                                       |
| Texture2DMSArray    | Largura UINT, altura UINT, elementos UINT, amostras UINT                           |
| Texture2DMSArray    | Largura float, altura float, elementos float, amostras float                       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Retorna dimensões para o maior nível de mipmap (inicial).
2.  O TextureCubeArray está disponível no modelo de sombreador 4,1 ou superior.
3.  O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Textura-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





