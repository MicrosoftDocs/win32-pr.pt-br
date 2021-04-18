---
title: Como desenvolver um aplicativo OEM que usa um arquivo personalizado
description: Saiba como desenvolver um aplicativo que usa um arquivo personalizado para passar informações do OEM para o aplicativo.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105763318"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>Como desenvolver um aplicativo OEM que usa um arquivo personalizado

Para obter mais informações sobre como criar e usar arquivos de dados personalizados, consulte [Opções de manutenção do pacote do aplicativo do DISM (. Appx ou. appxbundle) Command-Line](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).

Saiba como desenvolver um aplicativo que usa um arquivo personalizado para passar informações do OEM para o aplicativo.

Para aplicativos que você cria para a implantação do OEM, você pode usar um arquivo personalizado para passar informações do OEM para os aplicativos. Para passar informações de OEM para um aplicativo, você cria um arquivo. Data personalizado na pasta microsoft.system. Package. Metadata. Esse nome de arquivo é especial para o sistema operacional e é executado automaticamente durante as atualizações do sistema operacional. Os OEMs podem usar esse arquivo para passar identificadores personalizados, para que os aplicativos saibam quando os OEMs o implantaram. Você pode ter apenas um arquivo. Data personalizado por aplicativo. Os aplicativos devem ser capazes de procurar e ler esse arquivo corretamente. Os desenvolvedores tratam o arquivo como dados não confiáveis.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Início rápido: consultar informações de manifesto do pacote de aplicativo](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>Pré-requisitos

-   Você precisa da ferramenta [DISM (gerenciamento e manutenção de imagens de implantação)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) para adicionar o pacote do aplicativo com o arquivo de dados personalizado.

## <a name="instructions"></a>Instruções

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>Etapa 1: criar um arquivo personalizado e adicioná-lo à pasta de metadados do pacote

Você pode criar seu aplicativo para usar qualquer formato escolhido para os dados personalizados. Por exemplo, você pode usar XML, um arquivo de texto ou outro tipo de arquivo para organizar seus dados. Recomendamos que você considere como você pode testar e validar o arquivo. Por exemplo, você pode criar um esquema XML para validar um arquivo XML.

Você pode especificar qualquer tipo de arquivo com qualquer nome de arquivo para os dados personalizados. Quando você adiciona o pacote do aplicativo com o arquivo de dados personalizado usando a ferramenta [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , o DISM renomeia o arquivo personalizado para Custom. Data e salva o arquivo na pasta microsoft.system. Package. Metadata.

> [!Note]  
> O arquivo de dados personalizado não pode ser modificado pelo aplicativo. É um recurso somente leitura.

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>Etapa 2: acessar o arquivo de dados personalizado para um aplicativo

Você pode acessar o arquivo. Data personalizado para um aplicativo do seu código usando as APIs do Windows para obter informações para o pacote atual. Por exemplo:

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

Para obter mais informações sobre como desenvolver com a propriedade [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) , consulte [início rápido: consultar informações de manifesto do pacote de aplicativo](how-to-query-package-identity-information.md).

Para obter mais informações sobre como acessar o arquivo Custom. Data por meio de [**IStorageFolder. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) e usando objetos [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) , consulte [acessando dados e arquivos](/previous-versions/windows/apps/hh464959(v=win.10)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Início rápido: consultar informações de manifesto do pacote de aplicativo](how-to-query-package-identity-information.md)
</dt> </dl>

 

 