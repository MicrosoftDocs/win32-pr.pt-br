---
title: atributo broadcast
description: A palavra-chave \ broadcast\ especifica que as chamadas de procedimento remoto são enviadas a todos os servidores em uma rede local.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- atributo de difusão MIDL
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f176b03f9d33ee1bbe1d0e805dfc109de477b7499f8fd624ba7732709dc61a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385232"
---
# <a name="broadcast-attribute"></a>atributo broadcast

A **\[ difusão de \]** palavra-chave especifica que as chamadas de procedimento remoto são enviadas a todos os servidores em uma rede local.

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

*interface-attribute-list* 
</dt> <dd>

Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo. Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.

</dd> <dt>

*interface-name* 
</dt> <dd>

Especifica o nome da interface.

</dd> <dt>

*lista de atributos* 
</dt> <dd>

Especifica atributos adicionais a serem aplicados à função. Separe vários atributos com vírgulas.

</dd> <dt>

*Returntype* 
</dt> <dd>

Especifica o tipo de retorno da função.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função à qual o atributo **\[ de difusão \]** será aplicado.

</dd> <dt>

*params* 
</dt> <dd>

Lista de parâmetros de função.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\[ \] palavra-chave** broadcast especifica que a rotina é sempre transmitida para todos os servidores na rede, em vez de ser entregue a um servidor específico. O cliente recebe a saída da primeira resposta para retornar com êxito, enquanto as respostas subsequentes são descartadas.

Uma operação com o **\[ atributo broadcast \]** é implicitamente [**\[ \] uma operação idempotente.**](idempotent.md) No entanto, **\[ o atributo broadcast \]** especifica propriedades adicionais que funcionam com o atributo **\[ idempotente \]** não têm. Especificamente, as funções que usam o **\[ atributo broadcast \]** especificam que a rotina pode ser chamada várias vezes como resultado de uma chamada de procedimento remoto. Ao mesmo tempo, eles podem ser enviados para vários servidores. Isso é diferente do atributo **\[ \] idempotente,** que especifica apenas que uma chamada pode ser recuperada se ela não for concluída.

Se um procedimento remoto transmitir sua chamada para todos os hosts em uma rede local, ele deverá usar a sequência de protocolo [**ncadg \_ ip \_ udp**](ncadg-ip-udp.md) ou [**ncadg \_ ipx.**](ncadg-ipx.md) Observe que o tamanho de um **\[ pacote de difusão \]** é determinado pelo serviço de datagrama em uso.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**idempotente**](idempotent.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Talvez**](maybe.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> </dl>

 

 




