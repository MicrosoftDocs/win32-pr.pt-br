---
title: Importando a licença e o material da chave
description: Importando a licença e o material da chave
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- Windows SDK de formato de mídia, importação de DRM
- Windows SDK do formato de mídia, importar
- Windows SDK do formato de mídia, licenças
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), material da chave
- DRM (gerenciamento de direitos digitais), material da chave
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, material da chave
- APIs estendidas do cliente, material da chave
- licenças, importando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9852102ab282c983488c2e5c35b7187bf0daccb62d347c312d1afb343b60f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702500"
---
# <a name="importing-license-and-key-material"></a>Importando a licença e o material da chave

se você tiver conteúdo de mídia que foi criptografado usando um sistema de proteção de conteúdo de terceiros e quiser importar a licença e o material da chave para o DRM Windows media, siga estas etapas:

1.  recupere a coleção de certificados do computador DRM de mídia Windows chamando o método [**IWMDRMSecurity:: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .
2.  Analise a coleção de certificados, garantindo que ela esteja assinada corretamente e seja validada para uma chave pública Microsoft raiz conhecida. A coleção de certificados está de acordo com o esquema XMR. Para obter mais informações, consulte [criando uma licença do XMR](building-an-xmr-license.md).
3.  Opcional: Extraia a lista de revogação chamando o método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
4.  Opcional: Certifique-se de que nenhum certificado na coleção seja revogado. Para obter mais informações, consulte [verificando revogação de certificado](checking-certificate-revocation.md).
5.  gere uma licença no formato XMR que represente os requisitos de política para o conteúdo de importação e contenha o material de chave DRM de mídia Windows apropriado. Para obter mais informações, consulte o tópico [criando uma licença do XMR](building-an-xmr-license.md).
6.  passe a licença XMR para o sistema de DRM de mídia Windows para processamento, usando o método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

> [!Note]  
> os detalhes sobre o esquema XMR serão fornecidos a você quando você licencia Windows mídia DRM.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Verificando revogação de certificado**](checking-certificate-revocation.md)
</dt> <dt>

[**Criando uma licença do XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importação de DRM**](drm-import.md)
</dt> </dl>

 

 




