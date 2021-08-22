---
title: Empacotamento, implantação e consulta de Windows aplicativos
description: Crie pacotes de aplicativos programaticamente para Windows aplicativos e instale, atualize, consulte e desinstale pacotes de aplicativos.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79d235aa8d0d69c887eb67704d30137cf36a7583471f28269ac939a26b2a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814269"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>Empacotamento, implantação e consulta de Windows aplicativos

Implante, gerencie e Windows aplicativos (incluindo UWPs e aplicativos da área de trabalho) por meio de pacotes de aplicativos .msix/.appx com base no formato OPC. Cada pacote de aplicativos contém os arquivos que constituem o aplicativo e um arquivo de manifesto que descreve o software a ser Windows.

## <a name="introduction"></a>Introdução

Normalmente, os desenvolvedores criam e assinam pacotes de aplicativos usando Visual Studio. Para obter mais informações, [consulte Empacote um aplicativo UWP com Visual Studio](/windows/msix/package/packaging-uwp-apps).

O Microsoft Store torna mais fácil criar, enviar e vender seus aplicativos para clientes em todo o mundo. Para obter mais informações, consulte [Envios de aplicativo.](/windows/uwp/publish/app-submissions)

Windows PowerShell cmdlets permitem que você instale e gerencie aplicativos de linha de negócios Windows aplicativos sem usar a Store. Para obter mais informações, consulte [Appx Module Cmdlets](/powershell/module/appx/index?view=win10-ps).

Usando as APIs de empacotamento, implantação e consulta, você pode executar programaticamente estas tarefas:

-   Criar um pacote de aplicativos para um Windows aplicativo
-   Implantar um aplicativo Windows pacote
-   Enumerar os pacotes de aplicativos instalados em um sistema e obter informações sobre eles no manifesto
-   Consumir o conteúdo de um pacote de aplicativos

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                    | Descrição                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Como criar um pacote do aplicativo (C++)](how-to-create-a-package.md)                                        | Saiba como criar um pacote de aplicativos usando a API de empacotamento.                                                                                                                           |
| [Como criar um certificado de assinatura de pacote de aplicativos](how-to-create-a-package-signing-certificate.md)      | Saiba como usar [**MakeCert**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx para**](/windows-hardware/drivers/devtest/pvk2pfx) criar um certificado de assinatura de código de teste para que você possa assinar seus pacotes de aplicativos. |
| [Como assinar um pacote de aplicativos usando o SignTool](how-to-sign-a-package-using-signtool.md)                    | Saiba como usar o [**SignTool**](/windows-hardware/drivers/devtest/signtool) para assinar seus pacotes de aplicativos para que eles possam ser implantados.                                                                    |
| [Como solucionar problemas de erros de assinatura do pacote de aplicativos](how-to-troubleshoot-app-package-signature-errors.md) | Uma falha na implantação do aplicativo pode ser causada por uma falha ao validar a assinatura digital do pacote do aplicativo. Saiba como reconhecer essas falhas e o que fazer com elas.          |
| [Como assinar programaticamente um pacote de aplicativos (C++)](how-to-programmatically-sign-a-package.md)          | Saiba como assinar um pacote de aplicativos usando a [**função SignerSignEx2.**](/windows/desktop/SecCrypto/signersignex2)                                                                                   |
| [Como desenvolver um aplicativo OEM que usa um arquivo personalizado](how-to-develop-oem-app-with-custom-file.md)         | Saiba como desenvolver um aplicativo que usa um arquivo personalizado para passar informações do OEM para o aplicativo.                                                                                             |
| [Extrair conteúdo do pacote do aplicativo (C++)](how-to-extract-content-from-a-package.md)                          | Saiba como extrair arquivos de um pacote de aplicativos usando a API de empacotamento.                                                                                                               |
| [Consultar informações do manifesto do pacote do aplicativo (C++)](how-to-query-package-identity-information.md)                   | Saiba como obter informações de um manifesto do pacote de aplicativos usando a API de empacotamento                                                                                                            |
| [Solução de problemas](troubleshooting.md)                                                                   | Fornece informações para ajudá-lo a solucionar problemas que você tem ao empacotar, implantar ou consultar um pacote de aplicativos.                                                                 |
| [Referência da API de Empacotamento](interfaces.md)                                                                | A API de empacotamento cria, lê e grava pacotes de aplicativos.                                                                                                                            |
| [Referência da API de implantação](package-deployment-api.md)                                                   | A API de implantação instala, atualiza e desinstala pacotes de aplicativos.                                                                                                                    |
| [Referência da API de Consulta](functions.md)                                                                     | A API de consulta obtém informações sobre os pacotes de aplicativos instalados no sistema.                                                                                                               |
| [Ferramentas e cmdlets do PowerShell](appx-packaging-tools.md)                                                 | Use essas ferramentas e cmdlets para criar, instalar e gerenciar pacotes de aplicativos.                                                                                                              |
| [Amostras do SDK](appx-packaging-samples.md)                                                                | Baixe exemplos do SDK que demonstram o empacotamento, a implantação e as APIs de consulta para Windows aplicativos.                                                                               |
| [Glossário](appx-packaging-glossary.md)                                                                  | Saiba mais sobre os termos relacionados ao empacotamento, à implantação e à consulta de Windows aplicativos.                                                                                              |



 

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

[**Windows. ApplicationModel.Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel.PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 