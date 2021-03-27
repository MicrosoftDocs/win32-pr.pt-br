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
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006542"
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

 

 





