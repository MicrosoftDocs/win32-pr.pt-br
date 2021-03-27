---
title: '\#definir diretiva (constante)'
description: Diretiva de pré-processador que atribui um nome significativo a uma constante em seu aplicativo.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104006936"
---
# <a name="define-directive-constant"></a>\#definir diretiva (constante)

Diretiva de pré-processador que atribui um nome significativo a uma constante em seu aplicativo.



| \#definir *identifiertoken-cadeia de caracteres* |
|-----------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*ID*<br/>                                          | Identificador da constante. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*cadeia de caracteres* \[ de token adicional\]<br/> | Valor da constante. Esse parâmetro consiste em uma série de tokens, como palavras-chave, constantes ou instruções completas. Um ou mais caracteres de espaço em branco devem separar esse parâmetro do parâmetro de *identificador* ; Este espaço em branco não é considerado parte do texto substituído, nem qualquer espaço em branco após o último token do texto. <br/> Se você excluir esse parâmetro, todas as instâncias do parâmetro do *identificador* serão removidas do arquivo de origem. O identificador permanece definido e pode ser testado usando as diretivas [ \# If definidas](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef. <br/> |



 

## <a name="remarks"></a>Comentários

Todas as instâncias do parâmetro de *identificador* que ocorrem após a diretiva de [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) no arquivo de origem serão substituídas pelo valor do parâmetro *token-String* . O identificador é substituído somente quando ele forma um token; por exemplo, o identificador não será substituído se aparecer em um comentário, dentro de uma cadeia de caracteres ou como parte de um identificador mais longo.

A diretiva [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) instrui o pré-processador a esquecer a definição de um identificador; para obter mais informações, consulte a \# diretiva undef (DirectX HLSL).

A definição de constantes com a opção de compilador/D tem o mesmo efeito que usar a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no início do arquivo. Até 30 constantes podem ser definidas com a opção/D. Para obter um exemplo de como isso pode ser usado, consulte a seção de exemplos de [ \# ifdef e)](dx-graphics-hlsl-appendix-pre-ifdef.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir define a largura do identificador como a constante de inteiro 80 e define o comprimento em termos de largura e a constante de inteiro 10.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Cada instância subsequente de LENGTH é substituída por (WIDTH + 10) e todas as instâncias subsequentes de WIDTH + 10 são substituídas pela expressão (80 + 10). Os parênteses em volta da largura + 10 são importantes porque controlam a interpretação em instruções como as seguintes.


```
var = LENGTH * 20;
```



Após o estágio de pré-processamento, a instrução se torna o seguinte, que é avaliado como 1.800.


```
var = ( 80 + 10 ) * 20;
```



Sem parênteses, o resultado seria o seguinte, que é avaliado como 280.


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definir sobrecargas](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#Diretiva undef (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





