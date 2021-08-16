---
title: Enumerando licenças no armazenamento de licenças local
description: Enumerando licenças no armazenamento de licenças local
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows SDK de Formato de Mídia, enumerando licenças
- Windows SDK de Formato de Mídia, licenças
- Windows SDK de Formato de Mídia, armazenamento de licenças local
- DRM (gerenciamento de direitos digitais), enumerando licenças
- DRM (gerenciamento de direitos digitais), enumerando licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), armazenamento de licenças local
- DRM (gerenciamento de direitos digitais), armazenamento de licenças local
- APIs Estendidas do Cliente DRM, enumerando licenças
- APIs estendidas do cliente, enumerando licenças
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, armazenamento de licenças local
- APIs estendidas do cliente, armazenamento de licenças local
- licenças, enumerando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27913a5a35ce9af1f5a4d6fa3cbae808bc2abe89afd5edb05aa927fe4c39227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848192"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Enumerando licenças no armazenamento de licenças local

A enumeração é um processo de obter informações sobre as licenças no armazenamento de licenças local, passando por elas uma por uma. Você pode criar uma enumeração de licença chamando [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).

O motivo mais comum para enumerar por meio de licenças no armazenamento é encontrar uma licença específica para descriptografia de algum conteúdo.

A interface [**IWMDRMLicense**](iwmdrmlicense.md) serve como um portal para os resultados individuais da licença e como o enumerador. Quando a enumeração de licença é criada, a primeira licença na lista é carregada na interface **IWMDRMLicense.** A maioria dos métodos de **IWMDRMLicense** permite que você receba informações sobre a licença ou crie objetos para criptografar ou descriptografar conteúdo com base na licença. No entanto, há dois métodos que controlam a enumeração: [**GetNext**](iwmdrmlicense-getnext.md) e [**ResetEnumeration.**](iwmdrmlicense-resetenumeration.md) **GetNext** carrega a próxima licença na lista na interface . **ResetEnumeration** retorna a enumeração para o estado em que estava quando foi criada pela primeira vez. Quando a enumeração é redefinida, a primeira licença na lista é carregada de volta na interface **IWMDRMLicense.**

Quando você tiver atingido a última licença na lista, a próxima chamada para **GetNext** retornará ERROR \_ NO MORE \_ \_ ITEMS.

Se seu aplicativo executar uma ação com o conteúdo coberto pelo DRM, você deverá verificar as licenças no armazenamento de licenças local quanto aos direitos e outros fatores limitadores, como níveis de proteção de saída (OPLs).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obter informações de licenças no armazenamento de licenças local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




