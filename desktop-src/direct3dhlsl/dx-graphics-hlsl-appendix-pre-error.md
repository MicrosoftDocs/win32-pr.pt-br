---
title: " Diretiva de erro"
description: Diretiva de pré-processador que produz mensagens de erro de tempo de compilador.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- HLSL de diretiva de erro
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364844"
---
# <a name="error-directive"></a>\#Diretiva de erro

Diretiva de pré-processador que produz mensagens de erro de tempo de compilador.



| \#*cadeia de caracteres de token de* erro |
|------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                    | Descrição                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Cadeia de caracteres de token*<br/> | Mensagem de erro. Esse parâmetro consiste em uma série de tokens, como palavras-chave, constantes ou instruções completas. A cadeia de caracteres do token está sujeita à expansão de macro. <br/> |



 

## <a name="remarks"></a>Comentários

\#as diretivas de erro são mais úteis para detectar inconsistências de programador e violação de restrições durante o pré-processamento. Quando uma \# diretiva de erro é encontrada, a compilação é encerrada.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o processamento de erros durante o pré-processamento.


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





