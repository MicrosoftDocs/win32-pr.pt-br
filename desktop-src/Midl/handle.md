---
title: atributo de identificador
description: O atributo \ Handle \ especifica um definido pelo usuário ou \ 0034; personalizado \ 0034; tipo de identificador.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- manipular o atributo MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d4560de53bf3f24238e9ff96e01c74716729749
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823765"
---
# <a name="handle-attribute"></a>atributo de identificador

O \[  \] atributo Handle especifica um tipo de identificador definido pelo usuário ou "personalizado".

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TypeName* 
</dt> <dd>

Especifica o nome do tipo de identificador de associação definido pelo usuário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os identificadores definidos pelo usuário permitem que os desenvolvedores criem identificadores que são significativos para o aplicativo. Um identificador definido pelo usuário só pode ser definido em uma declaração de tipo, não em um Declarador de função.

Um parâmetro de um tipo definido pelo atributo \[ **Handle** \] é usado para determinar a associação para a chamada e é transmitido para o procedimento chamado.

O usuário deve fornecer associações e desvinculação de rotinas para converter entre tipos de identificador primitivos e definidos pelo usuário. Dado um identificador definido pelo usuário do tipo *TypeName*, o usuário deve fornecer as rotinas *TypeName* \_ **BIND** e *TypeName* \_ **Unbind**. Por exemplo, se o tipo de identificador definido pelo usuário for chamado myhandle, as rotinas serão nomeadas como \_ **associar** e mytratar \_ **desassociar**.

Se for bem-sucedida, a rotina de \_ **Associação** TypeName deverá retornar um identificador de associação primitivo válido. Se não for bem-sucedida, a rotina deverá retornar um **valor nulo**. Se a rotina retornar **NULL**, a  \_ rotina de **desassociar** typeName não será chamada. Se a rotina de associação retornar um identificador de associação inválido diferente de **NULL**, o comportamento do stub será indefinido.

Quando o procedimento remoto tem um identificador definido pelo usuário como um parâmetro ou como um identificador implícito, os stubs do cliente chamam a rotina de associação antes de chamar o procedimento remoto. Os stubs do cliente chamam a rotina de desvinculação após a chamada remota.

No DCE IDL, um parâmetro com o \[ atributo **Handle** \] deve aparecer como o primeiro parâmetro na lista de argumentos de procedimento remoto. Os parâmetros subsequentes, incluindo outros \[  \] atributos de identificador, são tratados como parâmetros comuns. A Microsoft dá suporte a uma extensão para o DCE IDL que permite que o parâmetro de identificador definido pelo usuário \[  \] apareça em posições diferentes do primeiro parâmetro.

## <a name="examples"></a>Exemplos

``` syntax
typedef [handle] struct 
{ 
    char machine[8]; 
    char nmpipe[256]; 
} h_service; 
 
handle_t __RPC_USER h_service_bind(h_service); 
void __RPC_USER h_service_unbind(h_service, handle_t);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Associação e identificadores](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_identificador implícito**](implicit-handle.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 