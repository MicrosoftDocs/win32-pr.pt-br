---
title: Opção/w
description: A opção/W especifica o nível de aviso do compilador MIDL. O nível de aviso indica a severidade do aviso.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W opção MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105789785"
---
# <a name="w-switch"></a>Opção/w

A opção **/w** especifica o nível de aviso do compilador MIDL. O nível de aviso indica a severidade do aviso.

``` syntax
midl /W level
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*level* 
</dt> <dd>

Especifica o nível de aviso, um número inteiro no intervalo de 0 a 4. Não há espaço entre a opção **/w** e o dígito que indica o valor de nível de aviso.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os níveis de aviso variam de 1 a 4, com um valor de zero significado para não exibir nenhuma informação de aviso. O aviso de severidade mais alta é o nível 1. A tabela a seguir descreve os avisos para cada nível de aviso.



| Nível de aviso | Descrição                                             | Exemplo                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0            | Sem avisos.                                            |                                                                           |
| W1            | Avisos graves que podem causar erros de aplicativo.      | Nenhum identificador de associação especificado, ponteiros sem atributo, opções conflitantes. |
| W2            | Pode causar problemas no ambiente operacional do usuário. | O comprimento do identificador excede 31 caracteres. Nenhum ARM de União padrão especificado.  |
| W3            | Reservado.                                               |                                                                           |
| S4            | Nível de aviso mais baixo.                                   | Construções não-ANSI C.                                                    |



 

Os avisos são diferentes dos erros. Os erros fazem com que o compilador MIDL pare o processamento do arquivo IDL. Os avisos fazem com que o compilador MIDL emita uma mensagem informativa e continue processando o arquivo IDL.

O nível de aviso definido pela opção **/w** pode ser usado com a opção [**/WX**](-wx.md) para fazer com que o compilador MIDL pare o processamento do arquivo IDL.

A opção **/w** comporta-se da mesma forma que a opção [**/Warn**](-warn.md)

## <a name="examples"></a>Exemplos

**MIDL/W2 filename. idl**

**MIDL/W4 bar. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Warn**](-warn.md)
</dt> </dl>

 

 




