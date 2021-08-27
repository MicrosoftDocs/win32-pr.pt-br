---
description: Assemblies privados lado a lado podem ser usados para criar componentes que podem ser facilmente atualizados sem também atualizar o aplicativo de hospedagem.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Atualizando componentes do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02948355143bc6f08c759ec6c2fe6009399cc6d8ca4b2bbd687e3d206c0e771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101586"
---
# <a name="updating-application-components"></a>Atualizando componentes do aplicativo

Assemblies privados lado a lado podem ser usados para criar componentes que podem ser facilmente atualizados sem também atualizar o aplicativo de hospedagem. Isso permite que um serviço de atualização instale os componentes atualizados do aplicativo, reinicie o aplicativo e que o aplicativo use as alterações. Ao usar manifestos do aplicativo, a funcionalidade dos componentes hospedados por um aplicativo pode ser atualizada sem a necessidade de alterar o código do aplicativo de hospedagem.

Esse método pode ser usado para atualizar a versão dos recursos de um aplicativo. Por exemplo, se um aplicativo contiver um assembly, o manifesto do aplicativo poderá especificar uma dependência nesse assembly. O aplicativo pode obter o assembly chamando [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para encontrar e carregar os arquivos necessários. Um atualizador simplesmente precisa trazer os bits mais novos para o assembly, que podem existir lado a lado com uma versão anterior do assembly.

 

 
