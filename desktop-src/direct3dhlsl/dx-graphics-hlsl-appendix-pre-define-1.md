---
title: '\#diretiva define (constante)'
description: Diretiva de pré-processador que atribui um nome significativo a uma constante em seu aplicativo.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06e3992dd81d2ffcc32a672e2d524fa51c1372c02ab90d8b6b8a905100ac9afb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855046"
---
# <a name="define-directive-constant"></a>\#diretiva define (constante)

Diretiva de pré-processador que atribui um nome significativo a uma constante em seu aplicativo.



| \#definir *identifiertoken-string* |
|-----------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                                                       | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*<br/>                                          | Identificador da constante. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*cadeia de caracteres de token* \[ Opcional\]<br/> | Valor da constante. Esse parâmetro consiste em uma série de tokens, como palavras-chave, constantes ou instruções completas. Um ou mais caracteres de espaço em branco devem separar esse parâmetro do *parâmetro do identificador;* esse espaço em branco não é considerado parte do texto substituído, nem qualquer espaço em branco após o último token do texto. <br/> Se você excluir esse parâmetro, todas as instâncias do parâmetro *identificador* serão removidas do arquivo de origem. O identificador permanece definido e pode ser testado usando as diretivas [ \# ,](dx-graphics-hlsl-appendix-pre-ifdef.md) \# ifdef e \# ifndef definidas. <br/> |



 

## <a name="remarks"></a>Comentários

Todas as instâncias do parâmetro *de identificador* que ocorrem após a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no arquivo de origem serão substituídas pelo valor do parâmetro *token-string.* O identificador é substituído somente quando ele forma um token; por exemplo, o identificador não será substituído se ele aparecer em um comentário, em uma cadeia de caracteres ou como parte de um identificador mais longo.

A [ \# diretiva undef](dx-graphics-hlsl-appendix-pre-undef.md) instrui o pré-processador a esquecer a definição de um identificador; para obter mais informações, consulte \# Diretiva undef (DirectX HLSL).

Definir constantes com a opção do compilador /D tem o mesmo efeito que usar a diretiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) no início do arquivo. Até 30 constantes podem ser definidas com a opção /D. Para ver um exemplo de como isso pode ser usado, consulte a seção Exemplos de [ \# ifdef e )](dx-graphics-hlsl-appendix-pre-ifdef.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir define o identificador WIDTH como a constante de inteiro 80 e, em seguida, define LENGTH em termos de WIDTH e a constante de inteiro 10.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Cada instância subsequente de LENGTH é substituída por (WIDTH + 10) e cada instância subsequente de WIDTH + 10 é substituída pela expressão (80 + 10). Os parênteses em torno de WIDTH + 10 são importantes porque controlam a interpretação em instruções como as a seguir.


```
var = LENGTH * 20;
```



Após o estágio de pré-processamento, a instrução se torna a seguinte, que é avaliada como 1.800.


```
var = ( 80 + 10 ) * 20;
```



Sem parênteses, o resultado seria o seguinte, que é avaliada como 280.


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

 

 





