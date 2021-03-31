---
title: represent_as atributo
description: O atributo \ represente \_ como \ ACF associa um tipo de local nomeado no idioma de destino repr com um tipo de transferência denominado-Type que é transferido entre cliente e servidor.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as do atributo MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17d0b8915e75bb3065b394ef76900bd8efb5e0c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006278"
---
# <a name="represent_as-attribute"></a>representar \_ como atributo

O atributo **\[ represente \_ como \]** ACF associa um tipo de local nomeado no idioma de destino *repr* com um tipo de transferência *denominado-Type* que é transferido entre o cliente e o servidor.

``` syntax
typedef [represent_as(repr-type) [[ , type-attribute-list ]] ] named-type; 
void __RPC_USER named-type_from_local (
  repr-type __RPC_FAR * ,
  named-type __RPC_FAR * __RPC_FAR * );
void __RPC_USER named-type_to_local (
  named-type __RPC_FAR * ,
  repr-type __RPC_FAR * ); void __RPC_USER named-type _free_inst ( named-type __RPC_FAR * ); void __RPC_USER named-type _free_local ( repr-type __RPC_FAR * );
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo nomeado* 
</dt> <dd>

Especifica o tipo de dados de transferência nomeado que é transferido entre o cliente e o servidor.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Separe vários atributos com vírgulas.

</dd> <dt>

*repr-tipo* 
</dt> <dd>

Especifica o tipo local representado no idioma de destino que é apresentado aos aplicativos cliente e servidor.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao usar **\[ representar \_ como \]**, você deve fornecer rotinas que são convertidas entre os tipos local e de transferência e a memória livre usada para manter os dados convertidos. O atributo **\[ representar \_ como \]** instrui os stubs a chamar as rotinas de conversão fornecidas pelo usuário.

O tipo de *nome* transferido deve ser resolvido para um tipo base de MIDL, tipo predefinido ou para um identificador de tipo. Para obter mais informações, consulte [tipos base de MIDL](midl-base-types.md).

Você deve fornecer as seguintes rotinas:



| Nome da rotina                   | Descrição                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *\_tipo nomeado * * * \_ do \_ local** | Converte dados do tipo local para o tipo de rede. A rotina aloca memória para o tipo de dados de rede, incluindo memória para todos os dados referenciados por ponteiros no tipo de dados de rede.              |
| *\_tipo nomeado * * * \_ para \_ local**   | Converte dados do tipo de rede para o tipo local. A rotina é responsável por alocar memória para os dados referenciados por ponteiros no tipo local. O RPC aloca memória para o tipo local em si. |
| *\_tipo nomeado * * * \_ \_ local livre** | Libera memória alocada para dados referenciados por ponteiros no tipo local. O RPC libera a memória para o próprio tipo                                                                                             |
| *\_tipo nomeado * * * \_ \_ Inst gratuito**  | Libera memória alocada para os dados referenciados por ponteiros no tipo de rede e para o próprio tipo de rede.                                                                                            |



 

O stub de cliente chama o *tipo nomeado * * * \_ de \_ local** para alocar espaço para o tipo transmitido e para converter os dados do tipo local para o tipo de rede. O stub do servidor aloca espaço para o tipo de dados original e chama o *tipo nomeado * * * \_ para \_ local** para converter os dados do tipo de rede para o tipo local.

Após o retorno do código do aplicativo, os stubs do cliente e do servidor chamam o *tipo nomeado * * * \_ Free \_ Inst** para desalocar o armazenamento para o tipo de rede. O stub de cliente chama o *tipo nomeado * * \_ * \_ local * gratuito* para desalocar o armazenamento retornado pela rotina.

Os tipos a seguir não podem ter um atributo " **\[ representar \_ como \]** ":

-   Matrizes em conformidade, variável ou em conformidade
-   Estruturas nas quais o último membro é uma matriz de conformidade (uma estrutura compatível)
-   Ponteiros ou tipos que contêm um ponteiro
-   Pipes ou tipos que contêm pipes
-   Tipos que são usados como o tipo base para um pipe
-   Tipos predefinidos [**manipulam \_ t**](handle-t.md), [**void**](void.md)
-   Tipos que têm o atributo [**\[ Handle \]**](handle.md)

## <a name="examples"></a>Exemplos

``` syntax
//these data types defined in .IDL or elsewhere
typedef struct  _lbox 
{ 
    long         data; 
    struct _lbox *next; 
} lbox; 
typedef [ref] lbox *PBOX_LOC; 
typedef long LONG4[4]; 
 
//in .ACF file :
interface iface
{
    typedef  [ represent_as(PBOX_LOC) ]  LONG4; 
}
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Storage**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**lidar com \_ t**](handle-t.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 




