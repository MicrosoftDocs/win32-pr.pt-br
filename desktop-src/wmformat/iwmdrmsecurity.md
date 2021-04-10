---
title: Interface IWMDRMSecurity
description: A interface IWMDRMSecurity gerencia uma variedade de informações relacionadas à segurança para o computador cliente e o subsistema DRM (gerenciamento de direitos digitais). Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Formato de mídia do Windows da interface IWMDRMSecurity
- Formato de mídia do Windows da interface IWMDRMSecurity, descrito
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293264"
---
# <a name="iwmdrmsecurity-interface"></a>Interface IWMDRMSecurity

A interface **IWMDRMSecurity** gerencia uma variedade de informações relacionadas à segurança para o computador cliente e o subsistema DRM (gerenciamento de direitos digitais).

Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passe **\_ IWMDRMSecurity IID** como o parâmetro *riid* .

## <a name="members"></a>Membros

A interface **IWMDRMSecurity** herda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMSecurity** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMSecurity** tem esses métodos.



| Método                                                                                      | Descrição                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md)                     | Determina se um certificado foi revogado.<br/>                                                    |
| [**GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | Recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados revogados.<br/> |
| [**GetContentEnablersFromHashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | Recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados com hash.<br/>  |
| [**GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | Recupera o certificado do computador do subsistema DRM no computador cliente.<br/>                        |
| [**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)                               | Recupera uma lista de certificados revogados do repositório local.<br/>                                         |
| [**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)                 | Recupera o número de versão de uma lista de certificados revogados no repositório local.<br/>                     |
| [**GetSecurityVersion**](iwmdrmsecurity-getsecurityversion.md)                             | Recupera a versão do subsistema DRM no computador cliente.<br/>                                    |
| [**PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md)                       | Inicia uma atualização de segurança para o subsistema DRM no computador cliente.<br/>                              |
| [**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)                               | Define uma lista de certificados revogados no repositório local.<br/>                                                |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Exemplo de individualização de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





