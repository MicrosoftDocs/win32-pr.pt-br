---
title: atributo handle
description: O atributo \ handle\ especifica um definido pelo usuário ou \ 0034;personalizado \ 0034; tipo de identificador.
ms.assetid: db5c6ea6-6081-4cea-9265-5e2f67fd8c14
keywords:
- atributo handle MIDL
topic_type:
- apiref
api_name:
- handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacdb3611a12873a6e828c33606bb9c970747555c285f8612be2b43bc3f51adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895286"
---
# <a name="handle-attribute"></a>atributo handle

O \[ **atributo** \] handle especifica um tipo de identificador definido pelo usuário ou "personalizado".

``` syntax
typedef [handle] typename;  
handle_t __RPC_USER typename_bind (typename);
void __RPC_USER typename_unbind (typename, handle_t);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Typename* 
</dt> <dd>

Especifica o nome do tipo de identificador de associação definido pelo usuário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os alças definidos pelo usuário permitem que os desenvolvedores projete alças significativas para o aplicativo. Um identificador definido pelo usuário só pode ser definido em uma declaração de tipo, não em um declarador de função.

Um parâmetro de um tipo definido pelo atributo handle é usado para determinar a associação para a chamada e \[  \] é transmitido para o procedimento chamado.

O usuário deve fornecer rotinas de associação e desa associação para converter entre tipos de alça primitivos e definidos pelo usuário. Dado um identificador definido pelo usuário do *tipo typename*, o usuário deve fornecer as rotinas *typename* \_ **bind** e *typename* \_ **unbind**. Por exemplo, se o tipo de identificador definido pelo usuário for chamado MYHANDLE, as rotinas serão nomeadas myhandle bind e \_  MYHANDLE \_ **unbind**.

Se for bem-sucedida, a rotina de associação *typename* \_  deverá retornar um identificador de associação primitivo válido. Se não for bem-sucedida, a rotina deverá retornar um **NULL.** Se a rotina retornar **NULL,** a rotina *de* \_ **desabinar** typename não será chamada. Se a rotina de associação retornar um handle de associação inválido diferente de **NULL,** o comportamento do stub será indefinido.

Quando o procedimento remoto tem um alça definido pelo usuário como um parâmetro ou como um alça implícito, os stubs do cliente chamam a rotina de associação antes de chamar o procedimento remoto. Os stubs de cliente chamam a rotina de desavinculação após a chamada remota.

Na IDL do DCE, um parâmetro com o atributo handle deve aparecer como o primeiro \[  \] parâmetro na lista de argumentos de procedimento remoto. Parâmetros subsequentes, incluindo outros \[ **atributos de** \] alça, são tratados como parâmetros comuns. A Microsoft dá suporte a uma extensão para ADL de DCE que permite que o parâmetro de alça definido pelo usuário apareça em posições que não \[  \] o primeiro parâmetro.

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

[Associação e alças](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**alça \_ implícita**](implicit-handle.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 