---
title: comutador/Error
description: A opção/Error determina os tipos de erro de verificação de que os stubs gerados serão executados em tempo de execução.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- MIDL do comutador/Error
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7af27de3d83171c8f1f89d0b860bf0b38ddfb6639a12bf40f90a58f06a273cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105626"
---
# <a name="error-switch"></a>comutador/Error

A opção **/Error** determina os tipos de erro de verificação de que os stubs gerados serão executados em tempo de execução.

> [!Note]  
> Este recurso está obsoleto e não tem mais suporte. O uso da opção [**/robust**](-robust.md) é recomendado.

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span id="allocation"></span><span id="ALLOCATION"></span>alocação * * * *


</dt> <dd>

Verifica se [**a \_ \_ alocação de usuário MIDL**](midl-user-allocate-1.md) retorna um valor **nulo** , indicando um erro de memória insuficiente.

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span id="stub_data"></span><span id="STUB_DATA"></span>dados de stub * * * * \_


</dt> <dd>

Gera um stub que captura exceções de desempacotamento no lado do servidor e as propaga de volta para o cliente.

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span id="ref"></span><span id="REF"></span>Ref * * * *


</dt> <dd>

Gera um código que executa uma verificação em tempo de execução para garantir que nenhum ponteiro de referência **nulo** esteja sendo passado para os stubs do cliente e gere uma \_ exceção de ponteiro ref de RPC X \_ NULL \_ \_ se encontrar algum.

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>verificação de limites * * * * \_


</dt> <dd>

Verifica o tamanho das matrizes em conformidade e variáveis variáveis em relação à especificação do comprimento da transmissão.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>nenhum * * * *


</dt> <dd>

Não executa nenhuma verificação de erro.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>todos * * * *


</dt> <dd>

Executa todas as verificações de erro. Em vigor com o MIDL versão 5,0, essa é uma opção de compilador padrão.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

A opção **/Error** seleciona o número de verificações de erro que serão executadas pelos arquivos stub gerados. Em vigor com o MIDL versão 5,0, a configuração padrão é **/Error All**.

Os erros de enumeração que são verificados (por padrão em todas as versões de MIDL) são erros de truncamento causados durante a conversão entre os tipos de **Enumeração longos** (inteiros de 32 bits) e os tipos de **Enumeração curtos** (a representação de dados de rede de [**enum**](enum.md)) e o número de identificadores em uma enumeração que excedem 32.767.

A verificação de erro de acesso à memória (também por padrão em todas as versões de MIDL) é para ponteiros que excedem o final do buffer no código de marshaling e para matrizes compatíveis cujo tamanho é menor que zero. Use o sinalizador de **\_ verificação de limites de/Error** para verificar outros limites de matriz inválidos.

Quando você especifica a **alocação/Error**, os stubs incluem o código que gera uma exceção quando o [**usuário de MIDL \_ \_ aloca**](midl-user-allocate-1.md) retorna 0.

A opção de **\_ dados stub/Error** impede que os dados do cliente falhem no servidor durante o desempacotamento, fornecendo efetivamente um método mais robusto para lidar com a operação de desempacotamento.

Em vigor com o WindowsÂ 2000, o mecanismo de marshaling de NDR de tempo de execução subjacente executa a maioria dessas verificações. Isso significa que, se você estiver usando um dos modos totalmente interpretados ([**/Oi**](-oi.md), **/OIF**) de geração de stub, a escolha de opções de verificação de erros diferentes não terá um efeito marcado no desempenho.

## <a name="examples"></a>Exemplos

**nome de arquivo de alocação/Error de MIDL. idl**

**MIDL/Error None filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




