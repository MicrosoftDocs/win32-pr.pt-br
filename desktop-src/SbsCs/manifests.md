---
description: Os manifestos são arquivos XML que acompanham e descrevem assemblies lado a lado ou aplicativos isolados.
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: Manifestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2536e518f39791b400b9e99002b9575f4428d64d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748746"
---
# <a name="manifests"></a>Manifestos

Os manifestos são arquivos XML que acompanham e descrevem assemblies lado a lado ou aplicativos isolados. Os manifestos identificam exclusivamente o assembly por meio do elemento **AssemblyIdentity** do assembly. Elas contêm informações usadas para associação e ativação, como classes COM, interfaces e bibliotecas de tipos, que tradicionalmente foram armazenadas no registro. Os manifestos também especificam os arquivos que compõem o assembly e podem incluir classes do Windows se o autor do assembly quiser que eles tenham controle de versão. Os assemblies lado a lado não são registrados no sistema, mas estão disponíveis para aplicativos e outros assemblies no sistema que especificam dependências em arquivos de manifesto.

Os arquivos de manifesto permitem que os administradores e aplicativos gerenciem versões lado a lado do assembly após a implantação. Cada assembly lado a lado deve ter um manifesto associado a ele. A instalação do Windows XP instala os [assemblies lado a lado da Microsoft com suporte](supported-microsoft-side-by-side-assemblies.md) com seus manifestos. Se você desenvolver seus próprios assemblies lado a lado, também deverá instalar os arquivos de manifesto. Para obter mais informações, consulte [instalação de assemblies lado a lado](installing-side-by-side-assemblies.md) e [referência de arquivos de manifesto](manifest-files-reference.md).

Manifestos e arquivos de configuração não são localizados.

Os seguintes tipos de manifestos são usados com assemblies lado a lado:

-   Os [manifestos de assembly](assembly-manifests.md) descrevem assemblies lado a lado. Eles são usados para gerenciar os nomes, as versões, os recursos e os assemblies dependentes de assemblies lado a lado. Os manifestos de [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies) são armazenados na pasta WinSxS do sistema. Os manifestos de assembly privado são armazenados como um recurso na DLL ou na pasta do aplicativo
-   Os [manifestos do aplicativo](application-manifests.md) descrevem [aplicativos isolados](isolated-applications.md). Eles são usados para gerenciar os nomes e as versões de assemblies compartilhados lado a lado que o aplicativo deve associar em tempo de execução. Os manifestos de aplicativo são copiados na mesma pasta que o arquivo executável do aplicativo ou incluídos como um recurso no arquivo executável do aplicativo.
-   [Arquivos de configuração de aplicativo](application-configuration-files.md), são manifestos usados para substituir e redirecionar as versões de assemblies dependentes usadas por assemblies e aplicativos lado a lado.
-   [Os arquivos de configuração do Publicador](publisher-configuration-files.md)são manifestos usados para redirecionar a versão de um assembly lado a lado para outra versão compatível. A versão para a qual o assembly está sendo redirecionado deve ter os mesmos valores principal. Minor que a versão original.

 

 
