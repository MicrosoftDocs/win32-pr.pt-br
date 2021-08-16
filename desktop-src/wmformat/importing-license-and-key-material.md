---
title: Importando licença e material de chave
description: Importando licença e material de chave
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows SDK de formato de mídia, importação de DRM
- Windows SDK de Formato de Mídia, importar
- Windows SDK de Formato de Mídia, licenças
- DRM (gerenciamento de direitos digitais), importação
- DRM (gerenciamento de direitos digitais), importação
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), material de chave
- DRM (gerenciamento de direitos digitais), material de chave
- APIs estendidas do cliente DRM, importação
- APIs estendidas do cliente, importação
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs Estendidas do Cliente DRM, material de chave
- APIs estendidas do cliente, material de chave
- licenças, importação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9852102ab282c983488c2e5c35b7187bf0daccb62d347c312d1afb343b60f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702500"
---
# <a name="importing-license-and-key-material"></a>Importando licença e material de chave

Se você tiver conteúdo de mídia criptografado usando um sistema de proteção de conteúdo de terceiros e quiser importar a licença e o material da chave para Windows DRM de Mídia, siga estas etapas:

1.  Recupere a coleção Windows de certificados do computador DRM de mídia chamando o método [**IWMDRMSecurity::GetMachineCertificate.**](iwmdrmsecurity-getmachinecertificate.md)
2.  Analisar a coleção de certificados, garantindo que ela seja assinada corretamente e seja validada para uma chave pública raiz da Microsoft conhecida. A coleção de certificados está em conformidade com o esquema XMR. Para obter mais informações, consulte [Criando uma licença XMR.](building-an-xmr-license.md)
3.  Opcional: extraia a lista de revogação chamando o [**método IWMDRMSecurity::GetRevocationData.**](iwmdrmsecurity-getrevocationdata.md)
4.  Opcional: garantir que nenhum certificado na coleção seja revogado. Para obter mais informações, consulte [Verificando a revogação de certificado.](checking-certificate-revocation.md)
5.  Gere uma licença no formato XMR que representa os requisitos de política para o conteúdo de importação e contenha o material de chave Windows DRM de Mídia apropriado. Para obter mais informações, consulte o tópico [Criando uma licença XMR.](building-an-xmr-license.md)
6.  Passe a licença XMR para o sistema Windows DRM de Mídia para processamento, usando o [**método IWMDRMLicenseManagement::StoreLicense.**](iwmdrmlicensemanagement-storelicense.md)

> [!Note]  
> Detalhes sobre o esquema XMR serão fornecidos quando você licenciar Windows DRM de Mídia.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Verificando a revogação de certificado**](checking-certificate-revocation.md)
</dt> <dt>

[**Criando uma licença XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importação de DRM**](drm-import.md)
</dt> </dl>

 

 




