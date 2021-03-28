---
title: '\#definir diretiva (macro)'
description: Diretiva de pré-processador que cria uma macro do tipo função.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104988632"
---
# <a name="define-directive-macro"></a>\#definir diretiva (macro)

Diretiva de pré-processador que cria uma macro do tipo função.



| \#definir *identificador*( *argument0*,..., *argumenton-1* ) *token-String* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*ID*<br/>                                                                                                                                                                             | Identificador da macro. <br/> Um segundo [ \# define](dx-graphics-hlsl-appendix-pre-define.md) para uma macro com um identificador que já existe no contexto atual gera um erro, a menos que a segunda sequência de token seja idêntica à primeira. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argumenton-1* ) <br/> | Lista de argumentos para a macro. A lista de argumentos é delimitada por vírgula, pode ter qualquer comprimento e deve ser colocada entre parênteses. Cada nome de argumento na lista deve ser exclusivo. Nenhum espaço em branco pode separar o parâmetro de *identificador* e o parêntese de abertura. <br/> Use a concatenação de linha Coloque uma barra invertida ( \) imediatamente antes do caractere de nova linha para dividir as diretivas longas em várias linhas de origem. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*cadeia de caracteres* \[ de token adicional\] <br/>                                                                                                                     | Valor da macro. Esse parâmetro consiste em uma série de tokens, como palavras-chave, constantes ou instruções completas. Um ou mais caracteres de espaço em branco devem separar esse parâmetro do parâmetro de *identificador* ; Este espaço em branco não é considerado parte do texto substituído, nem qualquer espaço em branco após o último token do texto. Faça uso liberal de parênteses para garantir que argumentos complicados sejam interpretados corretamente. <br/> Se o valor do parâmetro do *identificador* ocorrer dentro do parâmetro de *cadeia de caracteres de token* (mesmo como resultado de outra expansão de macro), ele não será expandido. <br/> Se você excluir esse parâmetro, todas as instâncias do parâmetro do *identificador* serão removidas do arquivo de origem. O identificador permanece definido e pode ser testado usando as diretivas [ \# If definidas](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef. <br/> |



 

## <a name="remarks"></a>Comentários

Todas as instâncias do parâmetro de *identificador* que ocorrem após a diretiva de [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) no arquivo de origem constituem uma chamada de macro e o identificador será substituído por uma versão do parâmetro de *cadeia de caracteres de token* que tem argumentos reais substituídos por parâmetros formais. O número de parâmetros na chamada deve corresponder ao número de parâmetros na definição de macro. O identificador é substituído somente quando ele forma um token; por exemplo, o identificador não será substituído se aparecer em um comentário, dentro de uma cadeia de caracteres ou como parte de um identificador mais longo.

A diretiva [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) instrui o pré-processador a esquecer a definição de um identificador; para obter mais informações, consulte a \# diretiva undef (DirectX HLSL).

A definição de constantes com a opção de compilador/D tem o mesmo efeito que usar a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no início do arquivo. Até 30 macros podem ser definidas com a opção/D.

Os argumentos reais na chamada de macro são correspondidos aos argumentos formais correspondentes na definição de macro. Cada argumento formal na cadeia de caracteres de token é substituído pelo argumento real correspondente, a menos que o argumento seja precedido por um operador stringing ( \# ), Charting ( \# @) ou token-Paste ( \# \# ), ou é seguido por um \# \# operador. As macros no argumento real são expandidas antes da política substituir o parâmetro formal.

A colagem de tokens no compilador HLSL é ligeiramente diferente da colação de token no compilador C, pois os tokens colados devem ser tokens válidos por conta própria. Por exemplo, considere a seguinte definição de macro:


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



No compilador C, isso resulta no seguinte:


```
float4x4 test
```



No compilador HLSL, no entanto, isso resulta no seguinte:


```
float4 x4 test
```



Você pode contornar esse comportamento usando a seguinte definição de macro em vez disso.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Exemplos

O exemplo a seguir usa uma macro para definir linhas de cursor.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



O exemplo a seguir define uma macro que recupera um número inteiro de pseudoaleatória no intervalo especificado.


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definir sobrecargas](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#Diretiva undef (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





