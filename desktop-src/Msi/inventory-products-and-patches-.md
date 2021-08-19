---
description: 'usuários e aplicativos com privilégios administrativos podem usar Windows Installer funções para inventariar os aplicativos Windows Installer, os recursos, os componentes e os patches instalados no sistema. a partir do Windows Installer&\# 160; 3.0, os usuários e aplicativos que têm privilégios de administrador podem enumerar os aplicativos Windows Installer, os recursos, os componentes e os patches instalados no sistema por todos os usuários. Os administradores e aplicativos podem obter informações sobre um produto ou patch para um determinado usuário ou todos os usuários no sistema. Os aplicativos podem obter o estado do recurso ou do componente para um usuário específico. as funções de inventário disponíveis a partir do Windows Installer&\# 160; 3.0 podem limitar o escopo dos itens a serem encontrados pelo contexto de instalação e pelo contexto do usuário. Há três contextos de instalação possíveis: por usuário, por computador e gerenciado por usuário. O contexto do usuário pode ser um usuário específico ou todos os usuários no sistema. as versões das funções de inventário de Windows Installer anteriores a Windows Installer&\# 160; 3.0 só podem enumerar itens instalados no sistema no contexto da máquina ou no contexto por usuário do usuário atual. essa limitação impede um inventário completo de todos os produtos Windows Installer e patches instalados no sistema por usuários diferentes do usuário atual. Enumerando ProductsEnumerating PatchesObtaining produto InformationObtaining patch InformationObtaining componente estado InformationObtaining informações de estado do recurso'
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: usando Windows Installer para produtos e patches de inventário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9406d0984e58efdb8344fbf8974234690e3a6aaeb1cc697b5a76e6af940554e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013224"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>usando Windows Installer para produtos e patches de inventário

usuários e aplicativos com privilégios administrativos podem usar Windows Installer funções para inventariar os aplicativos Windows Installer, os recursos, os componentes e os patches instalados no sistema.

a partir do Windows Installer 3,0, os usuários e aplicativos que têm privilégios de administrador podem enumerar os aplicativos Windows Installer, os recursos, os componentes e os patches instalados no sistema por todos os usuários. Os administradores e aplicativos podem obter informações sobre um produto ou patch para um determinado usuário ou todos os usuários no sistema. Os aplicativos podem obter o estado do recurso ou do componente para um usuário específico.

as funções de inventário disponíveis a partir do Windows Installer 3,0 podem limitar o escopo dos itens a serem encontrados pelo contexto de instalação e pelo contexto do usuário. Há três contextos de instalação possíveis: por usuário, por computador e gerenciado por usuário. O contexto do usuário pode ser um usuário específico ou todos os usuários no sistema.

as versões do Windows Installer funções de inventário anteriores a Windows Installer 3,0 só podem enumerar itens instalados no sistema no contexto do computador ou no contexto por usuário do usuário atual. essa limitação impede um inventário completo de todos os produtos Windows Installer e patches instalados no sistema por usuários diferentes do usuário atual.

-   [Enumerando produtos](#enumerating-products)
-   [Enumerando patches](#enumerating-patches)
-   [Obtendo informações sobre o produto](#obtaining-product-information)
-   [Obtendo informações de patch](#obtaining-patch-information)
-   [Obtendo informações de estado do componente](#obtaining-component-state-information)
-   [Obtendo informações de estado do recurso](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>Enumerando produtos

Use a função [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para enumerar Windows Installer aplicativos que estão instalados no sistema. Essa função pode localizar todas as instalações por máquina e instalações de aplicativos por usuário (gerenciados e não gerenciados) para o usuário atual e outros usuários no sistema. Use o parâmetro *dwContext* para especificar o contexto de instalação a ser encontrado. Você pode especificar qualquer uma das combinações dos possíveis contextos de instalação. Use o parâmetro *szUserSid* para especificar o contexto de usuário dos aplicativos a serem encontrados.

## <a name="enumerating-patches"></a>Enumerando patches

Use a função [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) para encontrar patches aplicados a um aplicativo. Essa função pode encontrar patches aplicados a um aplicativo específico ou a todos os aplicativos no sistema. Essa função pode encontrar patches aplicados a todas as instalações por máquina e instalações por usuário de aplicativos (gerenciados e não gerenciados) para o usuário atual e outros usuários no sistema.

Você pode usar o contexto de instalação e o contexto de usuário para restringir a enumeração de patch para um contexto específico ou entre todos os contextos. Use o parâmetro *dwContext* para especificar o contexto de instalação a ser encontrado. Você pode especificar qualquer uma das combinações dos possíveis contextos de instalação. Use o parâmetro *szUserSid* para especificar o contexto de usuário dos aplicativos a serem encontrados.

**Para enumerar os patches aplicados a todos os produtos anunciados ou instalados por todos os usuários no sistema**

-   Chame a função [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) .
    -   Use **NULL** para o valor do parâmetro *szProductCode* .
    -   Use "s-1-1-0" para o valor do parâmetro *szUserSid* .
    -   Use "MSIINSTALLCONTEXT \_ All" para o valor do parâmetro *dwContext* .

**Para enumerar os patches aplicados a todos os produtos anunciados ou instalados por todos os usuários no sistema**

1.  Chame a função [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) .

    -   Use **NULL** para o valor do parâmetro *szProductCode* .
    -   Use "s-1-1-0" para o valor do parâmetro *szUserSid* .
    -   Use "MSIINSTALLCONTEXT \_ All" para o valor do parâmetro *dwContext* .

    A função fornece um código de produto, contexto de usuário e contexto de instalação para cada aplicativo encontrado.

2.  Para cada aplicativo enumerado na etapa 1, chame [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) para enumerar os patches.

    Use os códigos de produto, contextos de usuário e contextos de instalação obtidos de [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) para os valores de *szProductCode*, *szUserSid* e *DwContext*, e cada chamada de função **MsiEnumProductsEx** .

## <a name="obtaining-product-information"></a>Obtendo informações sobre o produto

Use a função [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) para obter informações sobre aplicativos que são anunciados ou instalados no sistema e as propriedades que podem ser recuperadas. Essa função pode obter informações para uma instância de um aplicativo instalado em uma conta de usuário que não seja o usuário atual, mas não pode consultar uma instância de um produto anunciado em um contexto não gerenciado por usuário para uma conta de usuário que não seja o usuário atual.

Você pode especificar o contexto de instalação e o contexto do usuário para restringir informações para aplicativos instalados em um contexto específico. Use o parâmetro *dwContext* para especificar o contexto de instalação a ser encontrado. Você pode especificar apenas um dos possíveis contextos de instalação. Use o parâmetro *szUserSid* para especificar o contexto de usuário dos aplicativos a serem encontrados.

## <a name="obtaining-patch-information"></a>Obtendo informações de patch

Um aplicativo pode chamar a função [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) para consultar informações sobre o aplicativo de um patch para uma instância especificada de um produto. Propriedades como **LocalPackage**, [**transformações**](transforms.md)e **estado** podem ser recuperadas usando essa função. Nem todos os valores de propriedade têm garantia de estar disponíveis para aplicativos não gerenciados por usuário se o usuário não estiver conectado no momento no computador. Você pode especificar apenas um dos possíveis contextos de instalação.

Você pode especificar o contexto de instalação e o contexto do usuário para restringir informações a patches aplicados a aplicativos instalados em um contexto específico. Use o parâmetro *dwContext* para especificar o contexto de instalação a ser encontrado. Você pode especificar apenas um dos possíveis contextos de instalação. Use o parâmetro *szUserSid* para especificar o contexto de usuário dos aplicativos a serem encontrados.

## <a name="obtaining-component-state-information"></a>Obtendo informações de estado do componente

Os aplicativos podem chamar a função [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) para obter o estado instalado de um componente. Essa função determina se o componente está instalado localmente ou instalado para ser executado da origem. A função pode consultar um componente de uma instância de um aplicativo que é instalado em contas de usuário que não seja o usuário atual, desde que o produto não seja anunciado no contexto não gerenciado por usuário para uma conta de usuário que não seja o usuário atual.

Você pode especificar um contexto de instalação e um contexto de usuário para obter o estado dos componentes para aplicativos instalados em um contexto específico. Use o parâmetro *dwContext* para especificar o contexto de instalação a ser encontrado. Você pode especificar apenas um dos possíveis contextos de instalação. Use o parâmetro *szUserSid* para especificar o contexto de usuário dos aplicativos a serem encontrados.

## <a name="obtaining-feature-state-information"></a>Obtendo informações de estado do recurso

Os aplicativos podem chamar a função [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) para obter o estado instalado de um recurso do produto. Essa função determina se o recurso é anunciado, instalado localmente ou instalado para ser executado da origem. A função pode ser usada para consultar qualquer recurso de uma instância de um aplicativo instalado na conta do computador ou qualquer contexto na conta de usuário atual ou no contexto gerenciado por usuário em qualquer conta de usuário que não seja o usuário atual. Essa função não pode consultar um aplicativo instalado no contexto não gerenciado por usuário para uma conta de usuário que não seja o usuário atual. Você pode especificar apenas um dos possíveis contextos de instalação.

Você pode especificar um contexto de instalação e um contexto de usuário para obter o estado dos recursos para aplicativos instalados em um contexto específico. Use o parâmetro *dwContext* para especificar o contexto de instalação a ser encontrado. Você pode especificar apenas um dos possíveis contextos de instalação. Use o parâmetro *szUserSid* para especificar o contexto de usuário dos aplicativos a serem encontrados.

 

 



