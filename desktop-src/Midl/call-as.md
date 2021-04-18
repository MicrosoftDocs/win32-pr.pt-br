---
title: Atributo call_as
description: O atributo \ Call \_ as \ permite mapear uma função que não pode ser chamada remotamente a uma função remota.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- call_as do atributo MIDL
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105749809"
---
# <a name="call_as-attribute"></a>chamar \_ como atributo

O atributo **\[ Call \_ \]** as permite mapear uma função que não pode ser chamada remotamente a uma função remota.

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*proc local* 
</dt> <dd>

Especifica uma rotina definida pela operação.

</dd> <dt>

*Operation-atributo-List* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam à operação. Separe vários atributos com vírgulas.

</dd> <dt>

*nome da operação* 
</dt> <dd>

Especifica a operação nomeada apresentada ao aplicativo.

</dd> </dl>

## <a name="remarks"></a>Comentários

A capacidade de mapear uma função que não pode ser chamada remotamente a uma função remota é particularmente útil em interfaces que têm inúmeros tipos de parâmetro que não podem ser transmitidos pela rede. Em vez de usar muitos **\[** [**representações \_ como**](represent-as.md) **\]** e **\[** [**transmitir \_ como**](transmit-as.md) **\]** tipos, você pode combinar todas as conversões usando **\[ Call \_ as \]** rotinas. Você fornece as duas **\[ chamadas \_ como \]** rotinas (lado do cliente e servidor) para associar a rotina entre as chamadas de aplicativo e as chamadas remotas.

O atributo **\[ Call \_ \]** as pode ser usado para interfaces de objeto. Nesse caso, a definição de interface pode ser usada para chamadas locais, bem como chamadas remotas, porque a **\[ chamada \_ \]** permite que uma interface que não pode ser acessada remotamente seja mapeada de forma transparente para uma interface remota. O atributo **\[ Call \_ \]** as não pode ser usado com o modo [**/OSF**](-osf.md) .

Por exemplo, suponha que a rotina **F1** na interface de objeto **IFace** exige várias conversões entre as chamadas de usuário e o que realmente é transmitido. Os exemplos a seguir descrevem os arquivos IDL e ACF para a interface **IFace**:

No arquivo IDL para a interface **IFace**:

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

No ACF para a interface **IFace**:

``` syntax
[call_as( f1 )] Remf1();
```

Isso faz com que o arquivo de cabeçalho gerado defina a interface usando a definição de **F1**, ainda que também forneça stubs para **Remf1**.

O compilador MIDL irá gerar a seguinte vtable no arquivo de cabeçalho para a interface **IFace**:

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

O proxy do lado do cliente teria um proxy típico gerado por MIDL para **Remf1**, enquanto o stub do lado do servidor para **Remf1** seria igual ao stub típico gerado por MIDL:

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

Em seguida, as duas **\[ chamadas \_ como \]** rotinas de acoplamento (lado do cliente e servidor) devem ser codificadas manualmente:

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

Para interfaces de objeto, esses são os protótipos para as rotinas de acoplamento.

Para o lado do cliente:

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

Para o lado do servidor:

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

Para interfaces que não são de objeto, esses são os protótipos para as rotinas de acoplamento.

Para o lado do cliente:

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

Para o lado do servidor:

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**representar \_ como**](represent-as.md)
</dt> <dt>

[**transmitir \_ como**](transmit-as.md)
</dt> </dl>

 

 




