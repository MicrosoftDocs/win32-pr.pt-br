---
description: A classe COARefTime converte os tempos de referência entre as unidades de segundos e 100-nanossegundos.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Classe COARefTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 569da24d4487a1c7259c71ac0e2cda3ae7f31a88b69a74575186bdeb3b21445b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087266"
---
# <a name="coareftime-class"></a>Classe COARefTime

![hierarquia de classe COARefTime](images/cutil05.png)

A `COARefTime` classe converte os tempos de referência entre as unidades de segundos e 100-nanossegundos.

Essa classe é convertida entre os tempos de referência que são compatíveis com a automação e os tempos de referência que são compatíveis com C/C++. Interfaces compatíveis com automação usam valores **duplos** para representar o tempo em segundos. Outras interfaces usam valores **LONGLONG** de 64 bits para representar o tempo em unidades de 100 nanossegundos. Os seguintes tipos são definidos para esses valores:

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

Os filtros podem usar a `COARefTime` classe para converter entre os dois formatos. Essa classe é derivada da classe [**CRefTime**](creftime.md) .



| Métodos públicos                                          | Descrição                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [**COARefTime**](coareftime-coareftime.md)             | Método de construtor.                                                   |
| Operadores                                               | Descrição                                                           |
| [**double**](coareftime-double.md)                     | Converte o tempo de referência em um valor **duplo** .                    |
| [**hora de referência \_**](coareftime-reference-time.md)    | Converte o objeto em um valor **de \_ tempo de referência** .                      |
| [**operador =**](coareftime-operator-assign.md)        | Atribui um novo tempo de referência.                                         |
| [**operador = =**](coareftime-operator-eq.md)           | Testes de igualdade entre dois tempos de referência.                       |
| [**operador! =**](cmediatype-operator-neq.md)          | Testa desigualdade entre dois tempos de referência.                     |
| [**<do operador**](coareftime-operator-lt.md)         | Testa se um tempo de referência é menor que o outro.                     |
| [**>do operador**](coareftime-operator-gt.md)         | Testa se um tempo de referência é maior que o outro.                  |
| [**<do operador =**](coareftime-operator-lteq.md)      | Testa se um tempo de referência é menor ou igual a outro.         |
| [**>do operador =**](coareftime-operator-gteq.md)      | Testa se um tempo de referência é maior ou igual a outro.      |
| [**operador +**](coareftime-operator-plus.md)          | Adiciona dois tempos de referência.                                             |
| [* * operador * *](coareftime-operator-minus.md)         | Subtrai um tempo de referência de outro.                            |
| [**operador + =**](coareftime-operator-plus-assign.md)  | Adiciona dois tempos de referência e atribui o resultado a esse objeto.      |
| [**operador =**](coareftime-operator-minus-assign.md) | Subtrai dois tempos de referência e atribui o resultado a esse objeto. |
| [**operador \***](coareftime-operator-mult.md)         | Multiplica um tempo de referência por um valor.                               |
| [**operador**](coareftime-operator-div.md)           | Divide um tempo de referência por um valor.                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




