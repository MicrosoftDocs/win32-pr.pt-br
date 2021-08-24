---
description: As funções de banco de dados a seguir nunca devem ser chamadas de uma ação personalizada.
ms.assetid: 55fdd82b-9f34-4c2c-a837-8a09f21f568a
title: Funções não para uso em ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaddf6edae9636a599996a4ab8208537c1c673687337b65a9fcb74d1a8fc1f58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649616"
---
# <a name="functions-not-for-use-in-custom-actions"></a>Funções não para uso em ações personalizadas

As [funções de banco de dados](database-functions.md) a seguir nunca devem ser chamadas de uma ação personalizada.

-   [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)
-   [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)
-   [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)
-   [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)
-   [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)
-   [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
-   [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)
-   [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)
-   [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)
-   [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea)
-   [**MsiPreviewBillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda)
-   [**MsiPreviewDialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga)
-   [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

As [funções do instalador](installer-function-reference.md) a seguir nunca devem ser chamadas de uma ação personalizada.

-   [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
-   [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
-   [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
-   [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
-   [**MsiConfigureProductEx**](/windows/desktop/api/Msi/nf-msi-msiconfigureproductexa)
-   [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)
-   [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
-   [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea)
-   [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya)
-   [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta)
-   [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)
-   [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)
-   [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)
-   [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta)
-   [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
-   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   [**MsiUseFeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea)
-   [**MsiUseFeatureEx**](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
-   [**MsiVerifyPackage**](/windows/desktop/api/Msi/nf-msi-msiverifypackagea)

As [funções do instalador](installer-function-reference.md) a seguir nunca devem ser chamadas de uma ação personalizada se isso iniciar outra instalação. Eles podem ser chamados de uma ação personalizada que não inicia outra instalação.

-   [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
-   [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
-   [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa)

uma ação personalizada nunca deve gerar um novo thread que usa funções Windows Installer para alterar o estado do recurso, o estado do componente ou para enviar mensagens de um evento de controle. A tentativa de fazer isso faz com que a instalação falhe.

 

 



