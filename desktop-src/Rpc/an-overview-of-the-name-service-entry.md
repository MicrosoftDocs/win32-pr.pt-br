---
title: Uma visão geral da entrada de serviço de nome
description: A entrada de serviço de nome consiste em três seções distintas.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758724"
---
# <a name="an-overview-of-the-name-service-entry"></a>Uma visão geral da entrada de serviço de nome

A entrada de serviço de nome consiste em três seções distintas. A primeira seção é para interfaces (UUID + Version), a segunda seção contém os UUIDs de objeto e a terceira seção é para identificadores de associação. Você fornece um nome para a entrada que servirá como uma maneira de identificá-lo.

Ao chamar [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), o servidor especifica o nome da entrada na qual as informações exportadas são colocadas. Essa interface recentemente exportada é adicionada à seção interface da entrada serviço de nome. Todas as interfaces que já estão presentes na entrada de serviço de nome permanecem também. Esse mesmo processo é seguido para UUIDs de objeto e identificadores de associação.

O cliente chama [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (ou [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) para pesquisar um identificador de associação apropriado. O nome da entrada, o identificador de interface e um UUID de objeto são extraídos. Elas restringem as entradas das quais os identificadores de associação são retornados. Se uma entrada corresponder aos critérios de pesquisa, todos os identificadores de associação nessa entrada serão retornados de [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).

 

 




