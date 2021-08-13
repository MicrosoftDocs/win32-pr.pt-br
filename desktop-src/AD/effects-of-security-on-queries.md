---
title: Efeitos da segurança na pesquisa
description: A segurança é um filtro implícito ao executar pesquisas, enumerar contêineres ou ler propriedades.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- efeitos da segurança na pesquisa do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 429150489f2ab4d00015744beff72ee2b90b0399afd3d43f9263d39cadbaecd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191616"
---
# <a name="effects-of-security-on-searching"></a>Efeitos da segurança na pesquisa

A segurança é um filtro implícito ao executar pesquisas, enumerar contêineres ou ler propriedades.

ADSI pode retornar erros NO SUCH PROPERTY ou NO SUCH OBJECT mesmo quando o objeto existir se você não tiver acesso para ler \_ \_ atributos no \_ \_ objeto.

Por exemplo, um chamador pode ser capaz de enumerar os objetos filho em um contêiner porque o chamador tem direitos LIST \_ CONTENTS no contêiner. Mas o mesmo chamador poderá não conseguir acessar os objetos enumerados se o chamador não tiver acesso de leitura aos objetos filho. Nesse caso, uma consulta para um objeto filho pode retornar NO SUCH OBJECT, mesmo que o \_ \_ chamador tenha enumerado o objeto com êxito.

Se o chamador não tiver direitos suficientes, os seguintes códigos de retorno poderão ser retornados:

E \_ ADS OBJETO DE DOMÍNIO \_ \_ \_ INVÁLIDO

PROPRIEDADE \_ E ADS SEM \_ \_ \_ SUPORTE

PROPRIEDADE \_ E ADS NÃO \_ \_ \_ ENCONTRADA

 

 




