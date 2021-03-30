---
title: Verificando revogação de certificado
description: Verificando revogação de certificado
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, revogação de certificado
- SDK do Windows Media Format, revogação de certificados
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), revogação de certificado
- DRM (gerenciamento de direitos digitais), revogação de certificado
- DRM (gerenciamento de direitos digitais), revogação de certificados
- DRM (gerenciamento de direitos digitais), revogação de certificados
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, revogação de certificado
- APIs estendidas do cliente, revogação de certificado
- APIs estendidas do cliente DRM, revogação de certificados
- APIs estendidas do cliente, revogação de certificados
- certificados, revogação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbb72dd52870437ef9b69b30cc36a57725abe09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635813"
---
# <a name="checking-certificate-revocation"></a>Verificando revogação de certificado

Ao importar o conteúdo para o Windows Media DRM, você deve garantir que nenhum certificado em uma coleção de certificados tenha sido revogado verificando se nenhum certificado na coleção está na lista de revogação. A lista de revogação é extraída usando o método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .

Em seguida, você usa o método [**IWMDRMSecurity:: CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) para verificar se o certificado não foi revogado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Importação de DRM**](drm-import.md)
</dt> </dl>

 

 




