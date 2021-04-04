---
title: API de consulta de pacote
description: Saiba mais sobre a API de consulta de pacote, que pode ser usada para obter informações sobre os pacotes de aplicativos instalados no sistema. Cada pacote de aplicativo contém os arquivos que constituem um aplicativo do Windows e um arquivo de manifesto que descreve o software para o Windows.
ms.assetid: EDDFC8B1-E224-4921-BED6-FC81711BA5BF
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 5632edf661b4ea82177473bbb35f2674674500c6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007373"
---
# <a name="package-query-api"></a>API de consulta de pacote

Saiba mais sobre a API de consulta de pacote, que pode ser usada para obter informações sobre os pacotes de aplicativos instalados no sistema. Cada pacote de aplicativo contém os arquivos que constituem um aplicativo do Windows e um arquivo de manifesto que descreve o software para o Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                 | Descrição                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosePackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-closepackageinfo)<br/>                                               | Fecha uma referência às informações do pacote especificado.<br/>                                                                                              |
| [**FindPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-findpackagesbypackagefamily)<br/>                         | Localiza os pacotes com o nome de família especificado para o usuário atual. <br/>                                                                              |
| [**FormatApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-formatapplicationusermodelid)<br/>                       | Constrói uma [ID de modelo de usuário de aplicativo](appx-packaging-glossary.md) a partir do nome da família de pacotes e da ID do aplicativo relativa ao pacote (PRAID). <br/> |
| [**GetApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelid)<br/>                             | Obtém a [ID do modelo de usuário do aplicativo](appx-packaging-glossary.md) para o processo especificado.<br/>                                                          |
| [**GetApplicationUserModelIdFromToken**](/windows/desktop/api/Appmodel/nf-appmodel-getapplicationusermodelidfromtoken)<br/>           | Obtém a [ID do modelo de usuário do aplicativo](appx-packaging-glossary.md) para o token especificado.<br/>                                                            |
| [**GetCurrentApplicationUserModelId**](/windows/desktop/api/Appmodel/nf-appmodel-getcurrentapplicationusermodelid)<br/>               | Obtém a [ID do modelo de usuário do aplicativo](appx-packaging-glossary.md) para o processo atual.<br/>                                                            |
| [**GetCurrentPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefamilyname)<br/>                         | Obtém o nome da família de pacotes para o processo de chamada.<br/>                                                                                                 |
| [**GetCurrentPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagefullname)<br/>                             | Obtém o nome completo do pacote para o processo de chamada.<br/>                                                                                                   |
| [**GetCurrentPackageId**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageid)<br/>                                         | Obtém o identificador do pacote (ID) do processo de chamada.<br/>                                                                                             |
| [**GetCurrentPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo)<br/>                                     | Obtém as informações do pacote para o processo de chamada.<br/>                                                                                                 |
| [**GetCurrentPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackageinfo2)<br/>                                     | Obtém as informações do pacote para o processo de chamada, com a opção de especificar o tipo de pasta do pacote.<br/>                                                                                               |
| [**GetCurrentPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath)<br/>                                     | Obtém o caminho do pacote para o processo de chamada.<br/>                                                                                                        |
| [**GetCurrentPackagePath2**](/windows/desktop/api/AppModel/nf-appmodel-getcurrentpackagepath2)<br/>                                     | Obtém o caminho do pacote para o processo de chamada, com a opção de especificar o tipo de pasta do pacote.<br/>                                                                                                        |
| [**GetPackageApplicationIds**](/windows/desktop/api/AppModel/nf-appmodel-getpackageapplicationids)<br/>                               | Obtém as IDs de aplicativos no pacote especificado.<br/>                                                                                                        |
| [**GetPackageFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilyname)<br/>                                       | Obtém o nome da família de pacotes para o processo especificado.<br/>                                                                                               |
| [**GetPackageFamilyNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefamilynamefromtoken)<br/>                     | Obtém o nome da família de pacotes para o token especificado.<br/>                                                                                                 |
| [**GetPackageFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullname)<br/>                                           | Obtém o nome completo do pacote para o processo especificado.<br/>                                                                                                 |
| [**GetPackageFullNameFromToken**](/windows/desktop/api/AppModel/nf-appmodel-getpackagefullnamefromtoken)<br/>                         | Obtém o nome completo do pacote para o token especificado.<br/>                                                                                                   |
| [**Getpackageid**](/windows/desktop/api/AppModel/nf-appmodel-getpackageid)<br/>                                                       | Obtém o identificador do pacote (ID) para o processo especificado.<br/>                                                                                           |
| [**GetPackageInfo**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo)<br/>                                                   | Obtém as informações do pacote especificado.<br/>                                                                                               |
| [**GetPackageInfo2**](/windows/desktop/api/AppModel/nf-appmodel-getpackageinfo2)<br/>                                                   | Obtém as informações do pacote especificado, com a opção de especificar o tipo de pasta do pacote.<br/>                                                                                               |
| [**GetPackagePath**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepath)<br/>                                                   | Obtém o caminho para o pacote especificado.<br/>                                                                                                              |
| [**GetPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname)<br/>                               | Obtém o caminho do pacote especificado.<br/>                                                                                                               |
| [**GetPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getpackagepathbyfullname2)<br/>                               | Obtém o caminho do pacote especificado, com a opção de especificar o tipo de pasta do pacote.<br/>                                                                                                               |
| [**GetPackagesByPackageFamily**](/windows/desktop/api/AppModel/nf-appmodel-getpackagesbypackagefamily)<br/>                           | Obtém os pacotes com o nome de família especificado para o usuário atual. <br/>                                                                               |
| [**GetStagedPackageOrigin**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackageorigin)<br/>                                   | Obtém a origem do pacote especificado.<br/>                                                                                                             |
| [**GetStagedPackagePathByFullName**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname)<br/>                   | Obtém o caminho do pacote de preparação especificado.<br/>                                                                                                        |
| [**GetStagedPackagePathByFullName2**](/windows/desktop/api/AppModel/nf-appmodel-getstagedpackagepathbyfullname2)<br/>                   | Obtém o caminho do pacote de preparação especificado, com a opção de especificar o tipo de pasta do pacote.<br/>                                                                                                        |
| [**OpenPackageInfoByFullName**](/windows/desktop/api/AppModel/nf-appmodel-openpackageinfobyfullname)<br/>                             | Abre as informações de pacote do pacote especificado.<br/>                                                                                               |
| [**PackageFamilyNameFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromfullname)<br/>                     | Obtém o nome da família de pacotes para o nome completo do pacote especificado.<br/>                                                                                     |
| [**PackageFamilyNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefamilynamefromid)<br/>                                 | Obtém o nome da família de pacotes para o identificador de pacote especificado.<br/>                                                                                    |
| [**PackageFullNameFromId**](/windows/desktop/api/AppModel/nf-appmodel-packagefullnamefromid)<br/>                                     | Obtém o nome completo do pacote para o identificador de pacote (ID) especificado.<br/>                                                                                 |
| [**PackageIdFromFullName**](/windows/desktop/api/AppModel/nf-appmodel-packageidfromfullname)<br/>                                     | Obtém o identificador do pacote (ID) para o nome completo do pacote especificado.<br/>                                                                                 |
| [**PackageNameAndPublisherIdFromFamilyName**](/windows/desktop/api/AppModel/nf-appmodel-packagenameandpublisheridfromfamilyname)<br/> | Obtém o nome do pacote e o identificador do Publicador (ID) para o nome da família de pacotes especificado.<br/>                                                            |
| [**ParseApplicationUserModelId**](/windows/desktop/api/AppModel/nf-appmodel-parseapplicationusermodelid)<br/>                         | Desconstrói uma [ID de modelo de usuário de aplicativo](appx-packaging-glossary.md) para o nome da família de pacotes e a ID de aplicativo relativa (PRAID) do pacote.<br/>      |
| [**PackageOrigin**](/windows/desktop/api/AppModel/ne-appmodel-packageorigin)<br/>                                                     | Especifica a origem de um pacote. <br/>                                                                                                                   |
| [**Constantes de identidade**](identity-constants.md)<br/>                                           | Especifica o comprimento das cadeias de caracteres para os campos de identidade do pacote.<br/>                                                                                |
| [**Constantes de pacote**](package-constants.md)<br/>                                             | Especifica como os pacotes devem ser processados.<br/>                                                                                                           |
| [**ID do pacote \_**](/windows/desktop/api/AppModel/ns-appmodel-package_id)<br/>                                                          | Representa informações de identificação do pacote, como nome, versão e Publicador.<br/>                                                                  |
| [**informações do pacote \_**](/windows/desktop/api/AppModel/ns-appmodel-package_info)<br/>                                                      | Representa as informações de identificação do pacote que incluem o identificador do pacote, o nome completo e o local de instalação.<br/>                                  |
| [**versão do pacote \_**](/windows/desktop/api/AppModel/ns-appmodel-package_version)<br/>                                                | Representa as informações de versão do pacote.<br/>                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitos**
</dt> <dt>

[Pacotes de aplicativos e implantação](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

[Glossário](appx-packaging-glossary.md)
</dt> <dt>

**Referência**
</dt> <dt>

[Esquema de manifesto do pacote do aplicativo](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[API de empacotamento](interfaces.md)
</dt> <dt>

[API de implantação do pacote](package-deployment-api.md)
</dt> </dl>

 

