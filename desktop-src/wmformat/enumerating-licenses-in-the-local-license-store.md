---
title: Enumerando licenças no repositório de licenças local
description: Enumerando licenças no repositório de licenças local
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- SDK do Windows Media Format, enumerando licenças
- SDK do Windows Media Format, licenças
- SDK do Windows Media Format, armazenamento de licença local
- DRM (gerenciamento de direitos digitais), enumerando licenças
- DRM (gerenciamento de direitos digitais), enumerando licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), repositório de licenças local
- DRM (gerenciamento de direitos digitais), repositório de licenças local
- APIs estendidas do cliente DRM, enumerando licenças
- APIs estendidas do cliente, enumerando licenças
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, repositório de licenças local
- APIs estendidas do cliente, repositório de licenças local
- licenças, enumerando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363818"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Enumerando licenças no repositório de licenças local

A enumeração é um processo de obter informações sobre as licenças no repositório de licenças local, percorrendo-as uma a uma. Você pode criar uma enumeração de licenças chamando o [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).

O motivo mais comum para enumerar por meio de licenças no repositório é encontrar uma licença específica para descriptografia de algum conteúdo.

A interface [**IWMDRMLicense**](iwmdrmlicense.md) serve como um portal para os resultados de licença individuais e como o enumerador. Quando a enumeração de licença é criada, a primeira licença da lista é carregada na interface **IWMDRMLicense** . A maioria dos métodos de **IWMDRMLicense** permite que você obtenha informações sobre a licença ou crie objetos para criptografar ou descriptografar conteúdo com base na licença. No entanto, há dois métodos que controlam a enumeração: [**GetNext**](iwmdrmlicense-getnext.md) e [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md). **GetNext** carrega a próxima licença na lista na interface. **ResetEnumeration** retorna a enumeração para o estado em que estava quando ela foi criada pela primeira vez. Quando a enumeração é redefinida, a primeira licença na lista é carregada de volta para a interface **IWMDRMLicense** .

Quando você tiver atingido a última licença na lista, a próxima chamada para **GetNext** retornará um erro \_ sem \_ mais \_ itens.

Se seu aplicativo executar uma ação com o conteúdo coberto pelo DRM, você deverá verificar as licenças no repositório de licenças local para obter os direitos e outros fatores de limitação, como OPLs (níveis de proteção de saída).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obtendo informações de licenças no repositório de licenças local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




