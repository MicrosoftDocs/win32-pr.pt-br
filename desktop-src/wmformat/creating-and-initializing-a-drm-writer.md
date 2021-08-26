---
title: Criando e inicializando um gravador de DRM
description: Criando e inicializando um gravador de DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows SDK do formato de mídia, gravadores DRM
- DRM (gerenciamento de direitos digitais), criando gravadores de DRM
- DRM (gerenciamento de direitos digitais), criando gravadores de DRM
- DRM (gerenciamento de direitos digitais), inicializando gravadores DRM
- DRM (gerenciamento de direitos digitais), inicializando gravadores DRM
- APIs estendidas do cliente DRM, gravadores DRM
- APIs estendidas do cliente, gravadores DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24067e082de38bc396153be918025e2608246e39185c45eaa84bfe0e5c02407
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007046"
---
# <a name="creating-and-initializing-a-drm-writer"></a>Criando e inicializando um gravador de DRM

as etapas a seguir são necessárias para inicializar um objeto do gravador ASF para importar exemplos de mídia criptografada em Windows media DRM.

1.  Siga as etapas 1 a 4 da [importação de licença e material de chave](importing-license-and-key-material.md).
2.  crie e inicialize um objeto do gravador ASF usando o material da chave DRM de mídia Windows apropriado. Para obter mais informações, consulte [habilitando o suporte a DRM](enabling-drm-support.md).
3.  Defina cada um dos seguintes atributos chamando [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):
    -   \_HEADERSIGNPRIVKEY DRM
    -   \_V1LICENSEACQURL DRM
    -   \_Keyid DRM
    -   \_LICENSEACQURL DRM
4.  se uma versão licenciada do Windows gerenciador de direitos de mídia não estiver instalada no computador que executa o software, os quatro atributos a seguir também deverão ser definidos:
    -   \_LASIGNATUREROOTCERT DRM
    -   \_LASIGNATURECERT DRM
    -   \_LASIGNATURELICSRVCERT DRM
    -   \_LASIGNATUREPRIVKEY DRM
    -   o aplicativo para os certificados de criptografia necessários pode ser concluído preenchendo o [WMLA (contrato de licenciamento de mídia Windows)](https://www.microsoft.com/licensing/default) online.
5.  Crie uma chave de sessão e preencha uma estrutura de [**\_ chave de \_ sessão \_ de importação WMDRM**](wmdrm-import-session-key.md) . A chave de sessão será usada para criptografar uma chave de conteúdo. Para obter um exemplo, consulte o [exemplo de Create Session Key](create-session-key-example.md).
6.  Crie uma chave de conteúdo de um vetor de inicialização RC4 aleatório e preencha uma estrutura de [**chave de conteúdo de importação do WMDRM \_ \_ \_**](wmdrm-import-content-key.md) . A chave de conteúdo é usada para criptografar os exemplos de mídia. Para obter um exemplo, consulte [criar exemplo de chave de conteúdo](create-content-key-example.md).
7.  Criptografe a chave de conteúdo com a chave de sessão usando a criptografia RC4.
8.  Extraia a chave de coleção de certificados do computador. Para obter um exemplo, consulte [obter o exemplo de certificado de máquina](get-machine-certificate-example.md).
9.  Criptografe a chave de sessão com a chave pública extraída do certificado.
10. Preencha uma estrutura [**de \_ \_ \_ struct init de importação do WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .
11. chame o método [**IWMDRMWriter3:: SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) para notificar o SDK de que os exemplos que chegam ao gravador já estão protegidos e devem ser enviados diretamente para o Windows cliente DRM de mídia para importação.
12. Chame [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

as etapas restantes para criar um arquivo protegido por DRM são documentadas no guia de programação Windows Media Format SDK. Para obter mais informações, consulte [criando arquivos protegidos](creating-protected-files.md).

A próxima etapa é iterar por meio de cada exemplo de mídia, criptografá-la e passá-la para o objeto do gravador. Para obter mais informações, consulte a [criptografia e a importação de amostras de mídia](encrypting-and-importing-media-samples.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Importação de DRM**](drm-import.md)
</dt> </dl>

 

 




