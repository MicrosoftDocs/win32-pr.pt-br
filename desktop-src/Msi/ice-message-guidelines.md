---
description: As ações personalizadas do ICE se comunicam chamando MsiProcessMessage e postando uma mensagem de tipo de usuário do INSTALLMESSAGE \_ .
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Diretrizes de mensagens ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0951f8573fce1b9dbe81b107fba2f2beb674ed063fae53182a7d2694ded35abb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821666"
---
# <a name="ice-message-guidelines"></a>Diretrizes de mensagens ICE

As ações personalizadas do ICE se comunicam chamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e postando uma mensagem de tipo de usuário do INSTALLMESSAGE \_ .

Ao criar uma cadeia de caracteres de mensagem para uma ação personalizada de ICE, formate a cadeia de caracteres da seguinte maneira.

*Nome do Ice* <tab> *Tipo* <tab> de mensagem *Descrição* <tab> do *URL de ajuda ou local* <tab> *Nome* <tab> da tabela *Nome* <tab> da coluna *Chave primária* <tab> *Chave primária* <tab> *Chave primária* . . . (repita para quantas chaves primárias forem necessárias)

Os três primeiros campos da cadeia de caracteres são necessários em cada mensagem.

O campo tipo de mensagem Especifica se o ICE relata uma mensagem de falha, erro, aviso ou informativa.



| Valor | Tipo de mensagem                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Mensagem de falha relatando a falha da ação personalizada do ICE.                                                                                                       |
| 1     | Mensagem de erro que relata a criação do banco de dados que causa comportamento incorreto.                                                                                             |
| 2     | Mensagem de aviso que relata a criação de banco de dados que causa comportamento incorreto em determinados casos. Os avisos também podem relatar efeitos colaterais inesperados de criação de banco de dados. |
| 3     | Mensagem informativa.                                                                                                                                                |



 

Se a ajuda não estiver disponível, o campo URL da ajuda poderá ser a cadeia de caracteres vazia.

Mensagens de erro e de aviso devem fornecer o nome da tabela, o nome da coluna e os campos de chave primária. Se qualquer um desses campos for omitido, todos os campos após o primeiro campo em branco deverão ser deixados fora da mensagem. Por exemplo, é fornecido um nome de tabela sem um nome de coluna e chaves primárias ou um nome de tabela e um nome de coluna é fornecido sem chaves primárias. No entanto, um nome de coluna e chaves primárias não podem ser usados sem um nome de tabela. Várias chaves primárias podem ser listadas até que todas as chaves primárias nessa tabela tenham valores fornecidos.

## <a name="examples"></a>Exemplos

A primeira mensagem ilustrada pelo [Ice de exemplo em C++](sample-ice-in-c-.md):

"ICE01 \\ T3 \\ tCreated 04/29/1998 por <inserir nome do autor aqui>".

A segunda mensagem postada pelo ICE de exemplo:

"ICE01 \\ T3 \\ tLast modificou 05/06/1999 por <inserir nome do autor aqui>".

A terceira mensagem postada pelo ICE de exemplo.

"ICE01 \\ T3 \\ tSimple Ice para ilustrar o conceito de Ice".

 

 



