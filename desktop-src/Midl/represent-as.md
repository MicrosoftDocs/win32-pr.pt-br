---
title: represent_as atributo
description: O atributo \ represent as\ ACF associa um tipo local nomeado no tipo de repr do idioma de destino a um tipo de transferência chamado tipo que é transferido entre o \_ cliente e o servidor.
ms.assetid: ae44d220-e8f3-47a3-8f5e-a2668ac75411
keywords:
- represent_as atributo MIDL
topic_type:
- apiref
api_name:
- represent_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c76576a7d6710c54573ff78186b3cf6d347afc8c4c242fd6e4c1d49865fb521f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146359"
---
# <a name="represent_as-attribute"></a>representar \_ como atributo

O **\[ representa como \_ atributo \]** ACF associa um tipo local nomeado no tipo *de repr do* idioma de destino a um tipo de transferência chamado *tipo* que é transferido entre o cliente e o servidor.

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

*type-attribute-list* 
</dt> <dd>

Especifica um ou mais atributos que se aplicam ao tipo. Separe vários atributos com vírgulas.

</dd> <dt>

*repr-type* 
</dt> <dd>

Especifica o tipo local representado no idioma de destino que é apresentado aos aplicativos cliente e servidor.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao usar **\[ representar \_ como \]**, você deve fornecer rotinas que são convertidas entre os tipos local e de transferência e a memória livre usada para manter os dados convertidos. O **\[ atributo representar \_ como \]** instrui os stubs a chamar as rotinas de conversão fornecidas pelo usuário.

O tipo nomeado *transferido deve ser* resolvido para um tipo base MIDL, tipo predefinido ou para um identificador de tipo. Para obter mais informações, consulte [Tipos base MIDL](midl-base-types.md).

Você deve fornecer as seguintes rotinas:



| Nome da rotina                   | Descrição                                                                                                                                                                                                |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *tipo \_ nomeado*** \_ do \_ local** | Converte dados do tipo local para o tipo de rede. A rotina aloca memória para o tipo de dados de rede, incluindo memória para todos os dados referenciados por ponteiros no tipo de dados de rede.              |
| *tipo \_ nomeado*** \_ para \_ local**   | Converte dados do tipo de rede para o tipo local. A rotina é responsável por alocar memória para dados referenciados por ponteiros no tipo local. O RPC aloca memória para o próprio tipo local. |
| *tipo \_ nomeado*** \_ \_ local gratuito** | Libera a memória alocada para dados referenciados por ponteiros no tipo local. O RPC libera memória para o próprio tipo                                                                                             |
| *named \_ type*** \_ \_ free inst**  | Libera a memória alocada para os dados referenciados por ponteiros no tipo de rede e para o próprio tipo de rede.                                                                                            |



 

O stub do cliente chama *named-type*** de \_ \_ local** para alocar espaço para o tipo transmitido e converter os dados do tipo local para o tipo de rede. O stub do servidor aloca espaço para o tipo de dados original e chama *named-type*** \_ \_ para local** para converter os dados do tipo de rede para o tipo local.

Após o retorno do código do aplicativo, os stubs de cliente e servidor chamam *named-type*** \_ free \_ inst** para desalocar o armazenamento para o tipo de rede. O stub do cliente *chama named-type*** \_ local \_ gratuito** para desalocar o armazenamento retornado pela rotina.

Os seguintes tipos não podem ter uma **\[ representação \_ como \]** atributo:

-   Matrizes compatíveis, variáveis ou de variáveis compatíveis
-   Estruturas nas quais o último membro é uma matriz compatível (uma estrutura compatível)
-   Ponteiros ou tipos que contêm um ponteiro
-   Pipes ou tipos que contêm pipes
-   Tipos que são usados como o tipo base para um pipe
-   Tipos predefinidos [**\_ lidam com t**](handle-t.md), [**void**](void.md)
-   Tipos que têm o [**\[ atributo handle \]**](handle.md)

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

[**matrizes**](arrays-1.md)
</dt> <dt>

[Tipos base MIDL](midl-base-types.md)
</dt> <dt>

[**handle \_ t**](handle-t.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Vazio**](void.md)
</dt> </dl>

 

 




