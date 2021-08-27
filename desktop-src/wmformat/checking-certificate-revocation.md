---
title: Verificando a revogação de certificado
description: Verificando a revogação de certificado
ms.assetid: 498bd2a5-4336-4fc4-9718-6c5fe2db9066
keywords:
- Windows SDK de formato de mídia, importação de DRM
- Windows SDK de Formato de Mídia, importar
- Windows SDK de formato de mídia, revogação de certificado
- Windows SDK de Formato de Mídia, revogação de certificados
- DRM (gerenciamento de direitos digitais), importação
- DRM (gerenciamento de direitos digitais), importação
- DRM (gerenciamento de direitos digitais), revogação de certificado
- DRM (gerenciamento de direitos digitais), revogação de certificado
- DRM (gerenciamento de direitos digitais), revogação de certificados
- DRM (gerenciamento de direitos digitais), revogação de certificados
- APIs estendidas do cliente DRM, importação
- APIs estendidas do cliente, importação
- APIs estendidas do cliente DRM, revogação de certificado
- APIs estendidas do cliente, revogação de certificado
- APIs Estendidas do Cliente DRM, revogação de certificados
- APIs estendidas do cliente, revogação de certificados
- certificados, revogação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d9f8aaa299873513f88a2be258cf2ddd96147934e461cbde49630542fd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028064"
---
# <a name="checking-certificate-revocation"></a>Verificando a revogação de certificado

Ao importar conteúdo para Windows DRM de Mídia, você deve garantir que nenhum certificado em uma coleção de certificados tenha sido revogado verificando se nenhum certificado na coleção está na lista de revogação. A lista de revogação é extraída usando o [**método IWMDRMSecurity::GetRevocationData.**](iwmdrmsecurity-getrevocationdata.md)

Em seguida, use [**o método IWMDRMSecurity::CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md) para verificar se o certificado não foi revogado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Importação de DRM**](drm-import.md)
</dt> </dl>

 

 




