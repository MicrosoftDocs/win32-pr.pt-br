---
title: Empacotamento, implantação e consulta de aplicativos do Windows
description: Crie pacotes de aplicativos para aplicativos do Windows programaticamente e instale, atualize, consulte e desinstale pacotes de aplicativos.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bfd1792e0b7b18f0dee04bca6f352e055b20f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084459"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Empacotamento, implantação e consulta de aplicativos do Windows

Implante, gerencie e serviço aplicativos do Windows (incluindo UWPs e aplicativos de área de trabalho) por meio de pacotes de aplicativos. msix/. Appx com base no formato OPC. Cada pacote de aplicativo contém os arquivos que constituem o aplicativo e um arquivo de manifesto que descreve o software para o Windows.

## <a name="introduction"></a>Introdução

Normalmente, os desenvolvedores criam e assinam pacotes de aplicativos usando o Visual Studio. Para obter mais informações, consulte [empacotar um aplicativo UWP com o Visual Studio](/windows/msix/package/packaging-uwp-apps).

O Microsoft Store facilita a criação, o envio e a venda de seus aplicativos para clientes em todo o mundo. Para obter mais informações, consulte [envios de aplicativos](/windows/uwp/publish/app-submissions).

Os cmdlets do Windows PowerShell permitem que você instale e gerencie aplicativos de linha de negócios do Windows sem usar a loja. Para obter mais informações, consulte [cmdlets do módulo Appx](/powershell/module/appx/index?view=win10-ps).

Usando as APIs de empacotamento, implantação e consulta, você pode executar essas tarefas programaticamente:

-   Criar um pacote de aplicativo para um aplicativo do Windows
-   Implantar um aplicativo do Windows empacotado
-   Enumerar os pacotes de aplicativos instalados em um sistema e obter informações sobre eles de seu manifesto
-   Consumir o conteúdo de um pacote de aplicativo

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                    | Descrição                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como criar um pacote do aplicativo (C++)](how-to-create-a-package.md)                                        | Saiba como criar um pacote de aplicativo usando a API de empacotamento.                                                                                                                           |
| [Como criar um certificado de assinatura de pacote de aplicativos](how-to-create-a-package-signing-certificate.md)      | Saiba como usar [**MakeCert**](/windows-hardware/drivers/devtest/makecert) e [**pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) para criar um certificado de assinatura de código de teste, para que você possa assinar seus pacotes de aplicativos. |
| [Como assinar um pacote de aplicativos usando o SignTool](how-to-sign-a-package-using-signtool.md)                    | Saiba como usar o [**SignTool**](/windows-hardware/drivers/devtest/signtool) para assinar seus pacotes de aplicativos para que eles possam ser implantados.                                                                    |
| [Como solucionar problemas de erros de assinatura do pacote de aplicativo](how-to-troubleshoot-app-package-signature-errors.md) | Uma falha de implantação de aplicativo pode ser causada por uma falha ao validar a assinatura digital do pacote do aplicativo. Saiba como reconhecer essas falhas e o que fazer sobre elas.          |
| [Como assinar programaticamente um pacote do aplicativo (C++)](how-to-programmatically-sign-a-package.md)          | Saiba como assinar um pacote de aplicativo usando a função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .                                                                                   |
| [Como desenvolver um aplicativo OEM que usa um arquivo personalizado](how-to-develop-oem-app-with-custom-file.md)         | Saiba como desenvolver um aplicativo que usa um arquivo personalizado para passar informações do OEM para o aplicativo.                                                                                             |
| [Extrair o conteúdo do pacote de aplicativo (C++)](how-to-extract-content-from-a-package.md)                          | Saiba como extrair arquivos de um pacote de aplicativo usando a API de empacotamento.                                                                                                               |
| [Consultar informações de manifesto do pacote de aplicativo (C++)](how-to-query-package-identity-information.md)                   | Saiba como obter informações de um manifesto de pacote de aplicativo usando a API de empacotamento                                                                                                            |
| [Solução de problemas](troubleshooting.md)                                                                   | Fornece informações para ajudá-lo a solucionar problemas que ocorrem ao empacotar, implantar ou consultar um pacote de aplicativo.                                                                 |
| [Referência de API de empacotamento](interfaces.md)                                                                | A API de empacotamento cria, lê e grava pacotes de aplicativos.                                                                                                                            |
| [Referência de API de implantação](package-deployment-api.md)                                                   | A API de implantação instala, atualiza e desinstala pacotes de aplicativos.                                                                                                                    |
| [Referência de API de consulta](functions.md)                                                                     | A API de consulta obtém informações sobre os pacotes de aplicativos instalados no sistema.                                                                                                               |
| [Ferramentas e cmdlets do PowerShell](appx-packaging-tools.md)                                                 | Use essas ferramentas e cmdlets para criar, instalar e gerenciar pacotes de aplicativos.                                                                                                              |
| [Amostras do SDK](appx-packaging-samples.md)                                                                | Baixe exemplos de SDK que demonstram as APIs de empacotamento, implantação e consulta para aplicativos do Windows.                                                                               |
| [Glossário](appx-packaging-glossary.md)                                                                  | Saiba mais sobre os termos relacionados ao empacotamento, à implantação e à consulta de aplicativos do Windows.                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitos**
</dt> <dt>

[Pacotes de aplicativos e implantação](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**Outra referência**
</dt> <dt>

[Esquema de manifesto do pacote do aplicativo](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows. ApplicationModel. Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel. PackageID**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 