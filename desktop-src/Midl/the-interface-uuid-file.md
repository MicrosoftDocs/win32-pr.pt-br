---
title: O arquivo UUID de interface
description: O arquivo de UUID de interface coleta as definições dos identificadores de interface de todas as interfaces no arquivo IDL processado.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL e MIDL de COM, interfaces, arquivos UUID de proxy
- arquivo UUID de interface MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636887"
---
# <a name="the-interface-uuid-file"></a>O arquivo UUID de interface

O arquivo de UUID de interface coleta as definições dos identificadores de interface de todas as interfaces no arquivo IDL processado. Semelhante ao arquivo stub e ao arquivo de cabeçalho, o fechamento do fluxo de entrada é definido pelo arquivo IDL atual e pelos arquivos incluídos. Por exemplo, para a interface IFace, o compilador gera uma IFace de IID constante \_ e a inicializa para o UUID da interface especificado no arquivo IDL. Os aplicativos cliente e a DLL de proxy usam essa constante para identificar a interface.

O nome padrão para um arquivo de interface IID gerado a partir de um arquivo. idl é o arquivo \_ i.c. A opção de compilador [**/IID nomedearquivo**](-iid.md) MIDL substitui o nome padrão do arquivo UUID da interface.

 

 




