---
title: Comutador/WX
description: A opção/WX instrui o compilador MIDL a lidar com todos os erros no nível de aviso fornecido como erros.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- MIDL do comutador/WX
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823311"
---
# <a name="wx-switch"></a>Comutador/WX

A opção **/WX** instrui o compilador MIDL a lidar com todos os erros no nível de aviso fornecido como erros.

``` syntax
midl /WX
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Se a opção **/WX** for especificada e a opção [**/w**](-w.md)*n* não for especificada, todos os avisos no nível padrão, nível 1, serão tratados como erros.

A opção [**/w**](-w.md)*n* instrui o compilador a exibir todos os avisos no nível *n* e o **/WX** instrui o compilador a lidar com todos os avisos como erros. A combinação dessas duas opções direciona o compilador para lidar com todos os avisos no nível *n* como erros.

Os erros são diferentes dos avisos. Os erros fazem com que o compilador MIDL pare o processamento do arquivo IDL. Os avisos fazem com que o compilador MIDL emita uma mensagem informativa e continue processando o arquivo IDL.

O nível de aviso zero (0) direciona o compilador MIDL para suprimir informações de aviso. Quando as opções **/W0** e **/WX** são combinadas, o compilador MIDL suprime todas as informações de aviso. Nesse caso, a opção **/WX** não tem nenhum efeito.

## <a name="examples"></a>Exemplos

**MIDL/WX filename. idl**

**MIDL/w3/WX filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/W**](-w.md)
</dt> </dl>

 

 




