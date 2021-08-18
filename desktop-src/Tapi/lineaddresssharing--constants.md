---
description: As \_ constantes de sinalizador de bit LINEADDRESSSHARING descrevem várias maneiras como um endereço pode ser compartilhado entre as linhas.
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Constantes de LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fe92c92efd75a4f6e731944c487acff2ffd70e173dd04b03244ec9d55e8aba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003124"
---
# <a name="lineaddresssharing_-constants"></a>\_Constantes LINEADDRESSSHARING

As constantes de sinalizador de bit **LINEADDRESSSHARING \_** descrevem várias maneiras como um endereço pode ser compartilhado entre as linhas.

<dl> <dt>

<span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING \_ privado**
</dt> <dd> <dl> <dt>



O endereço é privado para a linha do usuário; Ele não está atribuído a nenhuma outra estação.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING \_ BRIDGEDEXCL**
</dt> <dd> <dl> <dt>



O endereço é ponte para uma ou mais estações. A primeira linha para ativar uma chamada na linha terá acesso exclusivo ao endereço e às chamadas que podem existir nele. Outras linhas não poderão usar o endereço de ponte enquanto estiverem em uso.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING \_ BRIDGEDNEW**
</dt> <dd> <dl> <dt>



O endereço é ponte com uma ou mais estações. A primeira linha para ativar uma chamada na linha terá acesso exclusivo apenas à chamada correspondente. Outros aplicativos que usam o endereço resultarão em aparências de chamada novas e separadas.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING \_ BRIDGEDSHARED**
</dt> <dd> <dl> <dt>



O endereço é ponte com uma ou mais linhas. Todas as partes com ponte podem compartilhar em chamadas no endereço, que, em seguida, funciona como uma conferência.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING \_ monitorado**
</dt> <dd> <dl> <dt>



Esse é um endereço cujo status ocioso/ocupado é disponibilizado para esta linha.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Sem extensibilidade. Todos os 32 bits são reservados.

A maneira como um endereço é compartilhado entre as linhas pode afetar o comportamento desse endereço. [**Linha \_ As mensagens CALLstate**](line-callstate.md) e [**line \_ addressstate**](line-addressstate.md) são enviadas para o aplicativo em resposta às atividades pelas estações de pontes. É por meio dessas mensagens que um aplicativo pode acompanhar o status do endereço.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Endereço de LINHAstate \_**](line-addressstate.md)
</dt> <dt>

[**chamada de LINHAstate \_**](line-callstate.md)
</dt> </dl>

 

 




