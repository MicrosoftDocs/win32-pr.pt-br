---
title: Efeitos de segurança na pesquisa
description: A segurança é um filtro implícito ao executar pesquisas, enumerar contêineres ou propriedades de leitura.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- efeitos de segurança na pesquisa Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634968"
---
# <a name="effects-of-security-on-searching"></a>Efeitos de segurança na pesquisa

A segurança é um filtro implícito ao executar pesquisas, enumerar contêineres ou propriedades de leitura.

A ADSI pode não retornar \_ tal \_ propriedade ou nenhum \_ desses erros de \_ objeto, mesmo quando o objeto existir, se você não tiver acesso a atributos de leitura no objeto.

Por exemplo, um chamador pode ser capaz de enumerar os objetos filho em um contêiner, pois o chamador tem direitos de conteúdo da lista \_ no contêiner. Mas o mesmo chamador não poderá acessar os objetos enumerados se o chamador não tiver acesso de leitura aos objetos filho. Nesse caso, uma consulta para um objeto filho pode não retornar nenhum \_ objeto desse tipo, \_ embora o chamador tenha enumerado com êxito o objeto.

Se o chamador não tiver direitos suficientes, os códigos de retorno a seguir poderão ser retornados:

\_objeto de \_ \_ domínio inválido \_ do E ADS

\_Propriedade E \_ ADS \_ sem \_ suporte

\_Propriedade E \_ ADS \_ não \_ encontrada

 

 




