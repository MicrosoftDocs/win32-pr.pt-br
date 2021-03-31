---
title: Importando a licença e o material da chave
description: Importando a licença e o material da chave
ms.assetid: 72ce5901-3e5b-4339-b695-592895ac6bfe
keywords:
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, licenças
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
ms.openlocfilehash: 5a142d0087916a45b6dd8661b67f7e42eaed245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160358"
---
# <a name="importing-license-and-key-material"></a>Importando a licença e o material da chave

Se você tiver conteúdo de mídia que foi criptografado usando um sistema de proteção de conteúdo de terceiros e desejar importar a licença e o material da chave no Windows Media DRM, siga estas etapas:

1.  Recupere a coleção de certificados do computador DRM do Windows Media chamando o método [**IWMDRMSecurity:: GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md) .
2.  Analise a coleção de certificados, garantindo que ela esteja assinada corretamente e seja validada para uma chave pública Microsoft raiz conhecida. A coleção de certificados está de acordo com o esquema XMR. Para obter mais informações, consulte [criando uma licença do XMR](building-an-xmr-license.md).
3.  Opcional: Extraia a lista de revogação chamando o método [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .
4.  Opcional: Certifique-se de que nenhum certificado na coleção seja revogado. Para obter mais informações, consulte [verificando revogação de certificado](checking-certificate-revocation.md).
5.  Gere uma licença no formato XMR que represente os requisitos de política para o conteúdo de importação e contenha o material de chave DRM do Windows Media apropriado. Para obter mais informações, consulte o tópico [criando uma licença do XMR](building-an-xmr-license.md).
6.  Passe a licença XMR para o sistema DRM do Windows Media para processamento, usando o método [**IWMDRMLicenseManagement:: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) .

> [!Note]  
> Os detalhes sobre o esquema XMR serão fornecidos a você quando você licenciar o DRM do Windows Media.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Verificando revogação de certificado**](checking-certificate-revocation.md)
</dt> <dt>

[**Criando uma licença do XMR**](building-an-xmr-license.md)
</dt> <dt>

[**Importação de DRM**](drm-import.md)
</dt> </dl>

 

 




