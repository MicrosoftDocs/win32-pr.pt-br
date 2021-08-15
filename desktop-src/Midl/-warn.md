---
title: /warn switch
description: A opção /warn especifica o nível de aviso do compilador MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /warn switch MIDL
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a51f57be780edeac4a91ea4f127d34d1c004ff700429f405eee4522dcb63ef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067441"
---
# <a name="warn-switch"></a>/warn switch

A **opção /warn** especifica o nível de aviso do compilador MIDL.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Opções de opção

<dl> <dt>

*level* 
</dt> <dd>

Especifica o nível de aviso, um inteiro no intervalo de 0 a 4. Não há espaço entre a opção **/warn** e o dígito que indica o valor de nível de aviso.

</dd> </dl>

## <a name="remarks"></a>Comentários

O nível de aviso indica a severidade do aviso. Os níveis de aviso variam de 1 a 4, com um valor de zero que significa não exibir nenhuma informação de aviso. O aviso de severidade mais alta é o nível 1. A tabela a seguir descreve os avisos para cada nível de aviso.



| Nível de aviso | Descrição                                             | Exemplo                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Sem avisos.                                            |                                                                           |
| 1             | Avisos graves que podem causar erros de aplicativo.      | Nenhum alça de associação especificado, ponteiros não atribuídos, comutadores conflitantes. |
| 2             | Pode causar problemas no ambiente operacional do usuário. | O comprimento do identificador excede 31 caracteres. Nenhum arm de união padrão especificado.  |
| 3             | Reservado.                                               |                                                                           |
| 4             | Nível de aviso mais baixo.                                   | Constructos C não ANSI.                                                    |



 

Os avisos são diferentes dos erros. Os erros causam a interrupção do processamento do arquivo IDL pelo compilador MIDL. Os avisos fazer com que o compilador MIDL emita uma mensagem informacional e continue processando o arquivo IDL.

O nível de aviso definido pela opção **/warn** pode ser usado com a opção [**WX**](-wx.md) para fazer com que o compilador MIDL pare o processamento do arquivo IDL.

A **opção /warn** se comporta da mesma forma que a [**opção /W.**](-w.md)

## <a name="examples"></a>Exemplos

**midl /warn2 filename.idl**

**midl /warn4 bar.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




