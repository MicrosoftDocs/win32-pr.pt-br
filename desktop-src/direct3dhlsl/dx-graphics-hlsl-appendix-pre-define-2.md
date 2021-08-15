---
title: '\#diretiva define (macro)'
description: Diretiva de pré-processador que cria uma macro semelhante a uma função.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49f89847a47a173f8f7d3bcbb22464fecad658068031f62559bde6ec0735f7f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514807"
---
# <a name="define-directive-macro"></a>\#diretiva define (macro)

Diretiva de pré-processador que cria uma macro semelhante a uma função.



| \#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*<br/>                                                                                                                                                                             | Identificador da macro. <br/> Uma segunda [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) para uma macro com um identificador que já existe no contexto atual gera um erro, a menos que a segunda sequência de token seja idêntica à primeira. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* ) <br/> | Lista de argumentos para a macro. A lista de argumentos é delimitada por vírgulas, pode ter qualquer comprimento e deve ser entre parênteses. Cada nome de argumento na lista deve ser exclusivo. Nenhum espaço em branco pode separar *o parâmetro de identificador* e o parêntese de abertura. <br/> Use a concatenação de linha coloque uma faixa invertida ( ) imediatamente antes do caractere de nova linha para dividir \\ diretivas longas em várias linhas de origem. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*cadeia de caracteres de token* \[ Opcional\] <br/>                                                                                                                     | Valor da macro. Esse parâmetro consiste em uma série de tokens, como palavras-chave, constantes ou instruções completas. Um ou mais caracteres de espaço em branco devem separar esse parâmetro do *parâmetro do identificador;* esse espaço em branco não é considerado parte do texto substituído, nem qualquer espaço em branco após o último token do texto. Use parênteses para garantir que argumentos complicados sejam interpretados corretamente. <br/> Se o valor do parâmetro *identificador* ocorrer dentro do parâmetro de cadeia de caracteres de *token* (mesmo como resultado de outra expansão de macro), ele não será expandido. <br/> Se você excluir esse parâmetro, todas as instâncias do parâmetro *identificador* serão removidas do arquivo de origem. O identificador permanece definido e pode ser testado usando as diretivas [ \# ,](dx-graphics-hlsl-appendix-pre-ifdef.md) \# ifdef e \# ifndef definidas. <br/> |



 

## <a name="remarks"></a>Comentários

Todas as instâncias do parâmetro de *identificador* que ocorrem após a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no arquivo de origem constituem uma chamada de macro e o identificador será substituído por uma versão do parâmetro de cadeia de caracteres de *token* que tem argumentos reais substituídos por parâmetros formais. O número de parâmetros na chamada deve corresponder ao número de parâmetros na definição de macro. O identificador é substituído somente quando ele forma um token; por exemplo, o identificador não será substituído se ele aparecer em um comentário, em uma cadeia de caracteres ou como parte de um identificador mais longo.

A [ \# diretiva undef](dx-graphics-hlsl-appendix-pre-undef.md) instrui o pré-processador a esquecer a definição de um identificador; para obter mais informações, consulte \# Diretiva undef (DirectX HLSL).

Definir constantes com a opção do compilador /D tem o mesmo efeito que usar a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no início do arquivo. Até 30 macros podem ser definidas com a opção /D.

Os argumentos reais na chamada de macro são correspondentes aos argumentos formais correspondentes na definição de macro. Cada argumento formal na cadeia de caracteres de token é substituído pelo argumento real correspondente, a menos que o argumento seja precedido por um operador stringizing ( \# ), charizing ( @) ou \# token-pasting ( \# \# ) \# ou é seguido por um \# operador . As macros no argumento real são expandidas antes da política substituir o parâmetro formal.

A colar token no compilador HLSL é ligeiramente diferente da colar token no compilador C, já que os tokens colares devem ser tokens válidos por conta própria. Por exemplo, considere a seguinte definição de macro:


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



No compilador C, isso resulta no seguinte:


```
float4x4 test
```



No entanto, no compilador HLSL, isso resulta no seguinte:


```
float4 x4 test
```



Você pode resolver esse comportamento usando a definição de macro a seguir.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Exemplos

O exemplo a seguir usa uma macro para definir linhas de cursor.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



O exemplo a seguir define uma macro que recupera um inteiro pseudorandom no intervalo especificado.


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

 

 





