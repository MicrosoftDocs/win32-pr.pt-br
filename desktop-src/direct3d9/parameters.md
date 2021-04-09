---
description: Os parâmetros são variáveis de efeito.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Parâmetros (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088799"
---
# <a name="parameters-direct3d-9"></a>Parâmetros (Direct3D 9)

Os parâmetros são variáveis de efeito.

## <a name="syntax"></a>Syntax

*ID do tipo de uso* \[ :  \] \[ < *expressão de anotação semântica (s)* > \] \[ =   \] ;

Os parâmetros podem ser lidos e gravados pelo aplicativo com [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).

Os parâmetros podem ser referenciados em funções e em técnicas (especificamente, no lado direito das atribuições de estado).



| Item                                                                                 | Descrição                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*usos*<br/>                   | Escopo do parâmetro. Consulte [usos e literais (Direct3D 9)](usages-and-literals.md).<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*Escreva*<br/>                      | Qualquer [referência válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) o tipo HLSL.<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*SESSÃO*<br/>                            | Um nome exclusivo.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*semântico*<br/>          | Uma marca que segue as regras de identificador que normalmente indicam o uso do parâmetro. Deve ser um tipo específico.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*anotações*<br/> | Zero ou mais partes de informações específicas do usuário. Pode ser qualquer tipo. Consulte [adicionar informações para parâmetros de efeito com anotações](using-an-effect.md).<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*expressão*<br/>    | Inicializa o valor do parâmetro. Consulte [Expressions (Direct3D 9)](expressions.md).<br/>                                                                  |



 

Os parâmetros podem ser inicializados para qualquer [referência válida para](../direct3dhlsl/dx-graphics-hlsl-reference.md) a expressão HLSL que reduz para um valor literal.

Os valores de parâmetro não são alterados pela execução da atribuição de estado ou chamadas de função.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
