---
description: Os assemblies privados lado a lado podem ser usados para criar componentes que podem ser facilmente atualizados, sem Atualizar também o aplicativo de hospedagem.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Atualizando componentes do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920827"
---
# <a name="updating-application-components"></a>Atualizando componentes do aplicativo

Os assemblies privados lado a lado podem ser usados para criar componentes que podem ser facilmente atualizados, sem Atualizar também o aplicativo de hospedagem. Isso permite que um serviço de atualização instale os componentes atualizados do aplicativo, reinicie o aplicativo e faça com que o aplicativo use as alterações. Ao usar manifestos de aplicativo, a funcionalidade dos componentes hospedados por um aplicativo pode ser atualizada sem a necessidade de alterar o código do aplicativo de hospedagem.

Esse método pode ser usado para atualizar a versão dos recursos de um aplicativo. Por exemplo, se um aplicativo contiver um assembly, o manifesto do aplicativo poderá especificar uma dependência nesse assembly. O aplicativo pode obter o assembly chamando [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para localizar e carregar os arquivos necessários. Um atualizador simplesmente precisa desativar os bits mais novos para o assembly, que pode existir lado a lado com uma versão anterior do assembly.

 

 
