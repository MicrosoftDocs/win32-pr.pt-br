---
title: " Diretiva de linha"
description: Diretiva de pré-processador que define o número de linha armazenado internamente do compilador e o nome do arquivo para os valores especificados.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- Diretiva de linha HLSL
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d452ebf68487dcf9b3177b5f89c81748b45760030dbddb6c3ae60070ca66bf0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118091196"
---
# <a name="line-directive"></a>\#Diretiva de linha

Diretiva de pré-processador que define o número de linha armazenado internamente do compilador e o nome do arquivo para os valores especificados.



| \#linha *LineNumber* "*filename*" |
|----------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                              | Descrição                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*<br/>                    | Número de linha a ser definido. Pode ser qualquer constante inteira. A substituição de macro pode ser executada nos tokens de pré-processamento, desde que o resultado seja avaliado como a sintaxe correta. <br/>                     |
| <span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*nome do arquivo* \[ adicional\] <br/> | Nome de arquivo a ser definido. O nome do arquivo pode ser qualquer combinação de caracteres e deve ser colocado entre aspas duplas (""). Se esse parâmetro for omitido, o nome de arquivo anterior permanecerá inalterado. <br/> |



 

## <a name="remarks"></a>Comentários

O compilador usa o número de linha e o nome de arquivo para se referir a erros encontrados durante a compilação. O número de linha geralmente se refere à linha de entrada atual, e o nome de arquivo se refere ao arquivo de entrada atual. O número de linha é incrementado depois que cada linha é processada. Se você alterar o número de linha e o nome de arquivo, o compilador irá ignorar os valores anteriores e continuar o processamento com os novos valores. A \# diretiva de linha normalmente é usada por geradores de programa para fazer com que as mensagens de erro se refiram ao arquivo de origem original, e não ao programa gerado.

O tradutor usa o número de linha e o nome de arquivo para determinar os valores do \_ \_ arquivo \_ \_ e \_ \_ linha \_ \_ de macros predefinidos. Você pode usar essas macros para inserir mensagens de erro autodescritivas no texto do programa. A \_ \_ macro File se \_ \_ expande para uma cadeia de caracteres cujo conteúdo é o nome do arquivo, entre aspas duplas ("").

## <a name="examples"></a>Exemplos

O exemplo a seguir define o número de linha como 151 e o nome de arquivo como "Copy. c".


```
#line 151 "copy.c"
```



No exemplo a seguir, a macro ASSERT usa a linha e o arquivo de macros predefinidos \_ \_ \_ \_ \_ \_ \_ \_ para imprimir uma mensagem de erro sobre o arquivo de origem se a declaração especificada não for verdadeira.


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





