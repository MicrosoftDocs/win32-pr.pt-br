---
title: atributo talvez
description: A palavra-chave \ talvez \ indica que a chamada de procedimento remoto não precisa ser executada toda vez que é chamada e o cliente não espera uma resposta. Observe que o protocolo \ talvez \ não garante nenhuma entrega nem conclusão da chamada.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- Talvez o atributo MIDL
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006374"
---
# <a name="maybe-attribute"></a>atributo talvez

A palavra-chave **\[ pode \]** indicar que a chamada de procedimento remoto não precisa ser executada toda vez que é chamada e o cliente não espera uma resposta. Observe que o protocolo **\[ talvez \]** não garante nenhuma entrega nem conclusão da chamada.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*interface-atributo-lista* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*nome da interface* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica atributos adicionais a serem aplicados à função. Separe vários atributos com vírgulas.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*nome da função* 
</dt> <dd>

Especifica o nome da função à qual o atributo **\[ talvez \]** será aplicado.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

Uma chamada com o atributo de **\[ talvez \]** não pode conter parâmetros de saída e é implicitamente uma **\[** chamada [**idempotente**](idempotent.md) **\]** .

## <a name="see-also"></a>Confira também

<dl> <dt>

[**difusor**](broadcast.md)
</dt> <dt>

[**idempotente**](idempotent.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 




