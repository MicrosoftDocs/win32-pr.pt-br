---
description: As transformações protegidas às vezes são necessárias por motivos de segurança.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Transformações protegidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e07c36b70827c301117bff7d98b30aae2990efb80f892bda24b0be35cbba5316
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040836"
---
# <a name="secured-transforms"></a>Transformações protegidas

As transformações protegidas às vezes são necessárias por motivos de segurança. As transformações protegidas são armazenadas localmente no computador do usuário em um local em que, em um sistema de arquivos seguro, o usuário não tem acesso de gravação. Essas transformações são armazenadas em cache nesse local durante a instalação ou o anúncio do pacote. Somente administradores e sistema local têm acesso de gravação a esse local. Um usuário não administrador não poderá modificar o arquivo de transformação. Durante as instalações subsequentes de [instalação sob demanda](installation-on-demand.md) ou [manutenção](maintenance-installation.md) do pacote, o instalador usa as transformações em cache.

Para especificar o armazenamento de transformação seguro, defina a [política TransformsSecure](transformssecure-policy.md), defina a propriedade [**TransformsSecure**](transformssecure.md) ou passe o símbolo @ ou \| na lista transformações. Observe que você não pode incluir transformações seguras e não seguras na mesma lista de transformações. Consulte [aplicando transformações](applying-transforms.md).

A remoção do produto por qualquer usuário remove todas as transformações protegidas desse produto do computador do usuário.

Se o instalador descobrir que uma transformação segura não está disponível localmente, ele tentará restaurar o cache de transformação de uma origem. As transformações seguras podem ser seguras-em-fonte ou caminho completo seguro:

-   As [transformações seguras no código-fonte](secure-at-source-transforms.md) que estão faltando no cache de transformação local são restauradas da raiz da origem do arquivo de .msi.
-   [Seguras-as transformações de caminho completo](secure-full-path-transforms.md) que estão ausentes do cache de transformação local são restauradas do caminho completo original especificado pela lista de transformações.

 

 



