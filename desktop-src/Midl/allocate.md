---
title: alocar atributo
description: O atributo \ Allocate \ ACF permite que você personalize a alocação de memória e a desalocação de um tipo definido no arquivo IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- alocar o atributo MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823195"
---
# <a name="allocate-attribute"></a>alocar atributo

O atributo **\[ ALLOCATE \]** ACF permite que você personalize a alocação de memória e a desalocação de um tipo definido no arquivo IDL.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de opções de alocação* 
</dt> <dd>

Especifica uma ou mais opções de alocação de memória. Selecione um dos nós **únicos \_** ou **todos, \_** ou uma das opções **gratuito** ou **não \_ livre**, ou um de cada par. Quando você especificar mais de uma opção, separe as opções com vírgulas.

</dd> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica outros atributos de tipo ACF opcionais. Quando você especificar mais de um atributo de tipo, separe as opções com vírgulas.

</dd> <dt>

*nome do tipo* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O atributo **\[ ALLOCATE \]** tem as seguintes opções válidas.



| Opção           | Descrição                                                           |
|------------------|-----------------------------------------------------------------------|
| **todos os \_ nós**   | Faz uma chamada para alocar e liberar memória para todos os nós.             |
| **\_nó único** | Faz muitas chamadas individuais para alocar e liberar cada nó de memória. |
| **gratuito**         | Libera memória no retorno do stub do servidor.                          |
| **Não \_ livre**   | Não libera memória no retorno do stub do servidor.                  |



 

Por padrão, os stubs podem alocar armazenamento para dados referenciados por um ponteiro exclusivo ou completo chamando o [**usuário de MIDL \_ \_**](midl-user-allocate-1.md) e o [**usuário de MIDL \_ \_ gratuito**](midl-user-free-1.md) individualmente para cada ponteiro.

Você pode otimizar a velocidade do seu aplicativo especificando a opção **todos os \_ nós**. Essa opção direciona o stub para computar o tamanho de toda a memória referenciada por meio do ponteiro do tipo especificado e fazer uma única chamada para o [**usuário de MIDL \_ \_ alocar**](midl-user-allocate-1.md). O stub libera a memória fazendo uma chamada para o [**\_ usuário MIDL \_ gratuitamente**](midl-user-free-1.md).

A opção **não \_ livre** DIRECIONA o compilador MIDL para gerar um stub de servidor que não chama o [**\_ usuário MIDL \_ livre**](midl-user-free-1.md) para o tipo especificado. A opção **não \_ livre** permite que as estruturas de ponteiro permaneçam acessíveis para o aplicativo de servidor após a chamada de procedimento remoto ser concluída e retornada ao cliente.

O atributo **\[ ALLOCATE \]** causará qualquer parâmetro **\[ in \] , out** que seja um ponteiro para um tipo qualificado com a opção **todos os \_ nós** para realocar a memória quando os dados forem desempacotados. É responsabilidade do aplicativo liberar a memória alocada anteriormente para esse parâmetro. Por exemplo:

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

O tipo de dados PTHISTYPE será realocado na direção de [**\[ saída \]**](out-idl.md) pelo stub antes do desempacotamento. Portanto, o aplicativo deve liberar a memória alocada anteriormente para os dados desse parâmetro ou ocorrerá um vazamento de memória.

## <a name="examples"></a>Exemplos

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**\_alocar usuário de MIDL \_**](midl-user-allocate-1.md)
</dt> <dt>

[**usuário de MIDL \_ \_ gratuito**](midl-user-free-1.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> </dl>

 

 




