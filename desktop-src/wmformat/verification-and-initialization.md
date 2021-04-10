---
title: Verificação e inicialização
description: Verificação e inicialização
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- SDK do Windows Media Format, verificação
- SDK do Windows Media Format, inicialização
- DRM (gerenciamento de direitos digitais), verificação
- DRM (gerenciamento de direitos digitais), verificação
- DRM (gerenciamento de direitos digitais), inicialização
- DRM (gerenciamento de direitos digitais), inicialização
- APIs estendidas do cliente DRM, verificação
- APIs estendidas do cliente, verificação
- APIs estendidas do cliente DRM, inicialização
- APIs estendidas do cliente, inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293784"
---
# <a name="verification-and-initialization"></a>Verificação e inicialização

Você deve executar as seguintes etapas para verificar se a criptografia é permitida e inicializar um objeto que descriptografará o conteúdo:

1.  Se você já tiver a ID de chave para o conteúdo, pule para a etapa 5.
2.  Chame a função [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) para criar um objeto do editor de metadados e obter uma instância da interface [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) do objeto.
3.  Chame **IWMMetadataEditor:: QueryInterface** para obter uma instância da interface [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .
4.  Chame [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) para obter a propriedade de **\_ \_ keyid DRMHeader do DRM** .
5.  Inicialize as APIs estendidas do cliente DRM do Windows Media chamando a função [**WMDRMStartup**](wmdrmstartup.md) .
6.  Chame a função [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) para criar um objeto de provedor seguro e obter uma instância da interface [**IWMDRMProvider**](iwmdrmprovider.md) do objeto.
7.  Chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md) para criar um objeto de gerenciamento de licença e obter uma instância de sua interface [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .
8.  Chame [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando a ID da chave e a direita que governa as ações a serem tomadas com o conteúdo depois que ele é criptografado. Essa chamada recuperará uma instância da interface [**IWMDRMLicense**](iwmdrmlicense.md) que pode ser usada para enumerar por meio de qualquer licença correspondente.
9.  Chame [**IWMDRMLicense:: inclusionlist**](iwmdrmlicense-getinclusionlist.md) para recuperar a lista de CPS (sistemas de proteção de conteúdo) autorizados conforme especificado pelo emissor da licença.
10. Analise a lista de inclusão para confirmar se o GUID da saída CPS é permitido pela licença.
11. Se o GUID de exportação desejado não estiver na lista de inclusão, chame [**IWMDRMLicense:: GetNext**](iwmdrmlicense-getnext.md) para obter a próxima licença aplicável (se houver) e repita as etapas 9 e 10. Se nenhuma licença tiver o GUID desejado em sua lista de inclusão, a exportação não poderá ser executada.
12. Chame [**IWMDRMLicense:: CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) para criar um objeto de descriptografia. Passe o certificado de aplicativo de exportação. Essa chamada fornecerá um ponteiro para uma instância da interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) do objeto decodificador e um objeto binário que contém a semente. Somente o tipo de proteção do Windows Media DRM Constant é compatível como um argumento para o parâmetro *dwFlags* no momento. **\_ \_ \_**
13. Use o esquema de criptografia RSA OAEP para descriptografar o vetor de inicialização.
14. Use a biblioteca de análise de ASF fornecida pela Microsoft quando você entra no contrato de exportação do DRM do Windows Media, para localizar o deslocamento em bytes para cada carga.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exportando conteúdo compactado**](exporting-compressed-content.md)
</dt> </dl>

 

 




