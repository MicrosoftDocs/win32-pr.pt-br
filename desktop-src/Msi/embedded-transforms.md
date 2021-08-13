---
description: As transformação inseridas são armazenadas dentro .msi arquivo do pacote. Isso garante aos usuários que a transformação sempre estará disponível quando o pacote de instalação estiver disponível. Como alternativa, as transformação podem ser fornecidas aos usuários como arquivos .mst autônomos.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformações inseridas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d7afb2b28599cb9ee2f10c4bc1fb25fbb0939fe68da5e817972eb8fc94236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637458"
---
# <a name="embedded-transforms"></a>Transformações inseridas

As transformação inseridas são armazenadas dentro .msi arquivo do pacote. Isso garante aos usuários que a transformação sempre estará disponível quando o pacote de instalação estiver disponível. Como alternativa, as transformação podem ser fornecidas aos usuários como arquivos .mst autônomos.

Para adicionar uma transformação inserida à lista de transformaçãos, adicione dois-pontos (:) prefixo para o nome do arquivo. Como o instalador sempre pode obter a transformação do armazenamento no arquivo .msi, as transformação inseridas não são armazenadas em cache no computador do usuário. As transformação inseridas podem ser usadas em combinação com as transformação [seguras](secured-transforms.md) ou [as desacuradas.](unsecured-transforms.md) Para obter mais informações, [consulte Aplicando transformações](applying-transforms.md).

 

 



