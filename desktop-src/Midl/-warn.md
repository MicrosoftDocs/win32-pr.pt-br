---
title: comutador/Warn
description: A opção/warn especifica o nível de aviso do compilador MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- MIDL do comutador/Warn
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638468"
---
# <a name="warn-switch"></a>comutador/Warn

A opção **/Warn** especifica o nível de aviso do compilador MIDL.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*level* 
</dt> <dd>

Especifica o nível de aviso, um número inteiro no intervalo de 0 a 4. Não há espaço entre a opção **/Warn** e o dígito que indica o valor de nível de aviso.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nível de aviso indica a severidade do aviso. Os níveis de aviso variam de 1 a 4, com um valor de zero significado para não exibir nenhuma informação de aviso. O aviso de severidade mais alta é o nível 1. A tabela a seguir descreve os avisos para cada nível de aviso.



| Nível de aviso | Descrição                                             | Exemplo                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Sem avisos.                                            |                                                                           |
| 1             | Avisos graves que podem causar erros de aplicativo.      | Nenhum identificador de associação especificado, ponteiros sem atributo, opções conflitantes. |
| 2             | Pode causar problemas no ambiente operacional do usuário. | O comprimento do identificador excede 31 caracteres. Nenhum ARM de União padrão especificado.  |
| 3             | Reservado.                                               |                                                                           |
| 4             | Nível de aviso mais baixo.                                   | Construções não-ANSI C.                                                    |



 

Os avisos são diferentes dos erros. Os erros fazem com que o compilador MIDL pare o processamento do arquivo IDL. Os avisos fazem com que o compilador MIDL emita uma mensagem informativa e continue processando o arquivo IDL.

O nível de aviso definido pela opção **/Warn** pode ser usado com a opção [**WX**](-wx.md) para fazer com que o compilador MIDL pare o processamento do arquivo IDL.

A opção **/Warn** se comporta da mesma forma que a opção [**/w**](-w.md) .

## <a name="examples"></a>Exemplos

**MIDL/warn2 filename. idl**

**MIDL/warn4 bar. idl**

## <a name="see-also"></a>Consulte também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




