---
description: A classe CReftime é uma classe auxiliar para gerenciar tempos de referência.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Classe CReftime (REFTIME. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748807"
---
# <a name="creftime-class"></a>Classe CReftime

![hierarquia de classe CRefTime](images/cutil05.png)

A `CRefTime` classe é uma classe auxiliar para gerenciar tempos de referência.

Um *tempo de referência* é uma unidade de tempo representada em unidades de 100 nanossegundos. Essa classe compartilha o mesmo layout de dados que o tipo de dados de [**\_ tempo de referência**](reference-time.md) , mas adiciona alguns métodos e operadores que fornecem funções de comparação, conversão e aritmética. Para obter mais informações sobre os tempos de referência, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).



| Variáveis de membro público                                                 | Descrição                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**\_tempo m**](creftime-m-time.md)                                      | Especifica o valor de **\_ tempo de referência** .              |
| Métodos públicos                                                          | Descrição                                           |
| [**CReftime**](creftime-creftime.md)                                   | Método de construtor.                                   |
| [**Getunidades**](creftime-getunits.md)                                   | Recupera o tempo de referência em unidades de 100 nanossegundos. |
| [**Milissegundos**](creftime-millisecs.md)                                 | Converte o tempo de referência em milissegundos.          |
| Operadores                                                               | Descrição                                           |
| [**\_tempo de referência do operador ()**](creftime-operator-reference-time-.md) | Converte o objeto em um tipo de dados de **\_ tempo de referência** .  |
| [**operador =**](creftime-operator-assign.md)                           | Atribui um novo tempo de referência.                         |
| [**operador + =**](creftime-operator-plus-assign.md)                     | Adiciona dois tempos de referência.                             |
| [**operador =**](creftime-operator-minus-assign.md)                    | Subtrai um tempo de referência de outro.            |



 

## <a name="remarks"></a>Comentários

Há uma possível armadilha com o uso dessa classe. Se você aplicar o operador + = com um objeto **CRefTime** como o operando esquerdo e uma variável do tipo **Long** como operando à direita, o compilador irá forçar implicitamente o operando direito em um objeto **CRefTime** . Essa coerção usa o construtor **CRefTime** que converte milissegundos em \_ unidades de tempo de referência; como resultado, o operando à direita é multiplicado por 10.000:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



No entanto, a mesma coisa não acontece usando o operador +:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>REFTIME. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




