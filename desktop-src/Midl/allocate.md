---
title: atributo allocate
description: O atributo \ allocate\ ACF permite personalizar a alocação e a desalocação de memória para um tipo definido no arquivo IDL.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- alocar atributo MIDL
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345652b9da5ed5087793606d963d6cf9b8ce225587ee150c27f6410ae99b8d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808427"
---
# <a name="allocate-attribute"></a>atributo allocate

O **\[ atributo \] alocar** ACF permite personalizar a alocação e a desalocação de memória para um tipo definido no arquivo IDL.

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*allocate-option-list* 
</dt> <dd>

Especifica uma ou mais opções de alocação de memória. Selecione um de um **nó \_ único** ou todos  **\_ os** nós ou um de gratuito ou não libera **ou \_** um de cada par. Quando você especificar mais de uma opção, separe as opções com vírgulas.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica outros atributos opcionais do tipo ACF. Ao especificar mais de um atributo de tipo, separe as opções com vírgulas.

</dd> <dt>

*type-name* 
</dt> <dd>

Especifica um tipo definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

O **\[ atributo \] allocate** tem as seguintes opções válidas.



| Opção           | Descrição                                                           |
|------------------|-----------------------------------------------------------------------|
| **todos \_ os nós**   | Faz uma chamada para alocar e liberar memória para todos os nós.             |
| **nó \_ único** | Faz muitas chamadas individuais para alocar e liberar cada nó de memória. |
| **gratuito**         | Libera memória no retorno do stub do servidor.                          |
| **não \_ gratuito**   | Não libera memória no retorno do stub do servidor.                  |



 

Por padrão, os stubs podem alocar armazenamento para dados referenciados por um ponteiro exclusivo ou completo chamando o usuário médio alocar e o usuário médio livre individualmente para cada ponteiro. [**\_ \_**](midl-user-allocate-1.md) [**\_ \_**](midl-user-free-1.md)

Você pode otimizar a velocidade do aplicativo especificando a opção todos **\_ os nós**. Essa opção direciona o stub para calcular o tamanho de toda a memória referenciada por meio do ponteiro do tipo especificado e fazer uma única chamada para o usuário médio [**\_ \_ alocar**](midl-user-allocate-1.md). O stub libera a memória fazendo uma chamada para [**o usuário \_ midl \_ gratuito.**](midl-user-free-1.md)

A **opção \_ não gratuito** direciona o compilador MIDL para gerar um stub de servidor que não chame o usuário [**midl \_ \_ gratuito**](midl-user-free-1.md) para o tipo especificado. A **opção não liberar permite que \_ as** estruturas de ponteiro permaneçam acessíveis para o aplicativo de servidor depois que a chamada de procedimento remoto tiver sido concluída e retornada ao cliente.

O **\[ atributo \] allocate** fará com que qualquer parâmetro **\[ in, out \]** que seja um ponteiro para um tipo qualificado com a opção todos os nós para relocar a memória quando os dados não são desmarcados. **\_** É responsabilidade do aplicativo liberar a memória alocada anteriormente para esse parâmetro. Por exemplo:

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

O tipo de dados PTHISTYPE será [**\[ \]**](out-idl.md) realocado na direção de saída pelo stub antes de desmarcar. Portanto, o aplicativo deve liberar a memória alocada anteriormente para os dados desse parâmetro ou ocorrerá uma perda de memória.

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

[**Em**](in.md)
</dt> <dt>

[**midl \_ user \_ allocate**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> </dl>

 

 




