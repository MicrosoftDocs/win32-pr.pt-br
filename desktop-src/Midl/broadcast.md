---
title: atributo de difusão
description: A palavra-chave \ Broadcast \ especifica que as chamadas de procedimento remoto sejam enviadas a todos os servidores em uma rede local.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- MIDL do atributo de difusão
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293297"
---
# <a name="broadcast-attribute"></a>atributo de difusão

A **\[ difusão \]** de palavra-chave especifica que as chamadas de procedimento remoto sejam enviadas a todos os servidores em uma rede local.

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
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

Especifica o nome da função à qual o atributo de **\[ difusão \]** será aplicado.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

A palavra-chave **\[ Broadcast \]** especifica que a rotina sempre é transmitida para todos os servidores na rede, em vez de ser entregue a um servidor específico. O cliente recebe a saída da primeira resposta a ser retornada com êxito, enquanto as respostas subsequentes são descartadas.

Uma operação com o atributo **\[ Broadcast \]** é implicitamente uma operação [**\[ idempotente \]**](idempotent.md) . No entanto, o atributo **\[ Broadcast \]** Especifica propriedades adicionais que funções com o atributo **\[ idempotente \]** não têm. Especificamente, as funções que usam o atributo **\[ Broadcast \]** especificam que a rotina pode ser chamada várias vezes como o resultado de uma chamada de procedimento remoto. Ao mesmo tempo, eles podem ser enviados para vários servidores. Isso é diferente do atributo **\[ idempotente \]** , que especifica apenas que uma chamada pode ser repetida se não for concluída.

Se um procedimento remoto transmite sua chamada para todos os hosts em uma rede local, ele deve usar a sequência de protocolo [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md) ou [**ncadg \_ IPX**](ncadg-ipx.md) . Observe que o tamanho de um pacote de **\[ difusão \]** é determinado pelo serviço de datagrama em uso.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**idempotente**](idempotent.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Eu**](maybe.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> </dl>

 

 




