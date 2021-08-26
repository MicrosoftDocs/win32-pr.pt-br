---
title: " Diretiva pragma"
description: Diretiva de pré-processador que fornece recursos específicos do computador ou do sistema operacional, mantendo a compatibilidade geral com as linguagens C e C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- HLSL de diretiva de pragma
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a16101eac6f303dbba03819c8d9f460c06c2613c748ef8ce4c74ae3fe30bb0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024606"
---
# <a name="pragma-directive"></a>\#Diretiva pragma

Diretiva de pré-processador que fornece recursos específicos do computador ou do sistema operacional, mantendo a compatibilidade geral com as linguagens C e C++.



| \#pragma *token-cadeia de caracteres* |
|-------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                    | Descrição                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Cadeia de caracteres de token*<br/> | Série de caracteres que fornece instruções e argumentos específicos do compilador. Este parâmetro está sujeito à expansão de macro. <br/> |



 

## <a name="remarks"></a>Comentários

Se o compilador encontrar um pragma não reconhecido, ele emitirá um aviso, mas a compilação continuará.

O compilador HLSL reconhece os seguintes pragmas:

-   [particular](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [message](message-pragma-directive--directx-hlsl-.md)
-   [matriz de pacote \_](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





