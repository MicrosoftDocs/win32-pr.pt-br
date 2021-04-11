---
title: Interface IWMDRMLicenseManagement
description: A interface IWMDRMLicenseManagement fornece métodos que executam operações gerais relacionadas ao armazenamento de licença local. Para obter uma instância dessa interface, chame IWMDRMProvider CreateObject. Passe \_ IWMDRMLICENSEMANAGEMENT IID como o parâmetro riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Formato de mídia do Windows da interface IWMDRMLicenseManagement
- Formato de mídia do Windows da interface IWMDRMLicenseManagement, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293173"
---
# <a name="iwmdrmlicensemanagement-interface"></a>Interface IWMDRMLicenseManagement

A interface **IWMDRMLicenseManagement** fornece métodos que executam operações gerais relacionadas ao armazenamento de licença local.

Para obter uma instância dessa interface, chame [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Passe **\_ IWMDRMLicenseManagement IID** como o parâmetro *riid* .

## <a name="members"></a>Membros

A interface **IWMDRMLicenseManagement** herda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMLicenseManagement** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMDRMLicenseManagement** tem esses métodos.



| Método                                                                                               | Descrição                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Adquire de forma assíncrona uma licença de uma URL especificada.<br/>                                                      |
| [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Cria um backup das licenças no repositório de licenças local.<br/>                                                 |
| [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Remove as licenças marcadas do repositório de licenças e desfragmenta o armazenamento para melhorar o desempenho.<br/>             |
| [**CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Cria um objeto enumerador de licenças populado com informações de licença com base em valores de parâmetro.<br/>            |
| [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Gera um desafio de revogação de licença.<br/>                                                                    |
| [**DeleteLicense**](iwmdrmlicensemanagement-deletelicense.md)                                       | Exclui uma licença do armazenamento de licença local temporário.<br/>                                                    |
| [**MonitorLicenseAcquisition**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | Inicia o monitoramento de um processo de aquisição de licença.<br/>                                                      |
| [**ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | Exclui uma licença que foi importada para o conteúdo originalmente protegido com outro sistema de proteção de conteúdo.<br/> |
| [**ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | Revoga licenças do repositório de licenças local.<br/>                                                               |
| [**RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md)                                   | Restaura as licenças de backup anteriormente.<br/>                                                                      |
| [**StoreLicense**](iwmdrmlicensemanagement-storelicense.md)                                         | Adiciona uma licença ao repositório de licenças local.<br/>                                                                   |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





