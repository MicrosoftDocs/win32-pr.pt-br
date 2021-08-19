---
title: byte_count atributo
description: O atributo \ contagem de \ bytes \_ \ ACF é um atributo de parâmetro que associa um tamanho, em bytes, à área de memória indicada pelo ponteiro.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count do atributo MIDL
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffd42e27be4768fc0817aa76bb366429e236b3a82c45d081a05485b8520a23a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807819"
---
# <a name="byte_count-attribute"></a>atributo de contagem de bytes \_

O atributo ACF de **\[ \_ contagem \] de bytes** é um atributo de parâmetro que associa um tamanho, em bytes, à área de memória indicada pelo ponteiro.

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de atributos de função* 
</dt> <dd>

Especifica zero ou mais atributos de função de ACF.

</dd> <dt>

*Nome da função* 
</dt> <dd>

Especifica o nome da função definida no arquivo IDL. O nome da função é obrigatório.

</dd> <dt>

*nome-variável de comprimento* 
</dt> <dd>

Especifica o nome do parâmetro [**\[ em \]**](in.md)apenas que especifica o tamanho, em bytes, da área de memória referenciada pelo *nome do parâmetro*.

</dd> <dt>

*nome do parâmetro* 
</dt> <dd>

Especifica o nome do parâmetro de ponteiro somente [**\[ out \]**](out-idl.md)definido no arquivo IDL.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **\[ \_ contagem \] de bytes** do atributo ACF representa uma extensão da Microsoft para o DCE IDL. Portanto, esse atributo não está disponível quando você usa o switch do compilador MIDL [**/OSF**](-osf.md).

> [!Note]  
> Não há mais suporte para o atributo **\[ contagem \] de bytes** na sintaxe NDR64 devido à dificuldade de estimar o tamanho necessário para todos os parâmetros de [**\[ saída \]**](out-idl.md) .

 

A memória referenciada pelo parâmetro Pointer é contígua e não é alocada ou liberada pelos stubs do cliente. Esse recurso do atributo **\[ \_ contagem \] de bytes** permite que você crie uma área de buffer persistente na memória do cliente que pode ser reutilizada durante mais de uma chamada para o procedimento remoto.

A capacidade de desativar a alocação de memória de stub de cliente permite que você ajuste o aplicativo para ter eficiência. Por exemplo, o atributo **\[ \_ contagem \] de bytes** pode ser usado por funções de provedor de serviço que usam o Microsoft RPC. Quando um aplicativo de usuário chama a API do provedor de serviço e envia um ponteiro para um buffer, o provedor de serviços pode passar o ponteiro de buffer para a função remota. O provedor de serviços pode reutilizar o buffer durante várias chamadas remotas sem forçar o usuário a realocar a área de memória.

A área memória pode conter estruturas de dados complexas que consistem em vários ponteiros. Como a área de memória é contígua, o aplicativo não precisa fazer várias chamadas para liberar individualmente cada ponteiro e estrutura. Em vez disso, ele pode alocar ou liberar a área de memória com uma chamada para a alocação de memória ou a rotina gratuita.

O buffer deve ser um parâmetro somente [**\[ out \]**](out-idl.md), enquanto o comprimento do buffer em bytes deve ser um parâmetro somente [**\[ no \]**](in.md).

Especifique um buffer que seja grande o suficiente para conter todos os parâmetros de [**\[ saída \]**](out-idl.md) . Devido ao preenchimento oculto, use estimativas em vez de contagens exatas. Por exemplo, ponteiros de 4 bytes não são empacotados em um limite alinhado de 4 bytes em plataformas de 32 bits e ponteiros de 8 bytes em um limite de 8 bytes em plataformas de 64 bits. Portanto, o preenchimento de alinhamento que os stubs executará deve ser contabilizado no espaço para o buffer. Além disso, os níveis de embalagem usados durante a compilação de linguagem C podem variar. Use um valor de contagem de bytes que leva em conta os bytes de empacotamento adicionais adicionados para o nível de embalagem usado durante a compilação em linguagem C. Uma prática segura que abrange plataformas de 32 bits e plataformas de 64 bits é assumir que cada objeto que entra no bloco de memória grande começa em um endereço que é um múltiplo de 8.

## <a name="examples"></a>Exemplos

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**no**](in.md)
</dt> <dt>

[**comprimento \_ é**](length-is.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**fora**](out-idl.md)
</dt> <dt>

[**o tamanho \_ é**](size-is.md)
</dt> </dl>

 

 




