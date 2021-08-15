---
description: este exemplo ilustra como criar uma instalação baseada em URL de um pacote de Windows Installer.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: Um exemplo de instalação do Windows Installer baseado em URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c25fb4f84ff3507505be7f16675b8da39afd349cb1b4c78520ee3de004df749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013324"
---
# <a name="a-url-based-windows-installer-installation-example"></a>Um exemplo de instalação do Windows Installer baseado em URL

este exemplo ilustra como criar uma instalação baseada em URL de um pacote de Windows Installer. para obter mais informações sobre como proteger instalações e usar certificados digitais, consulte [diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).

Para reproduzir este exemplo, você precisa do utilitário [SignTool](../seccrypto/signtool.md) . para obter detalhes, consulte a [referência de ferramentas de CryptoAPI](../seccrypto/cryptoapi-tools-reference.md) no sdk (Software Development Kit) do Microsoft Windows. você também precisa de [Msistuff.exe](msistuff-exe.md) e Setup.exe utilitários dos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Para obter mais informações, consulte [inicialização de download da Internet](internet-download-bootstrapping.md).

O exemplo tem as seguintes especificações:

-   Quando os usuários visitam seu site e clicam no link "MySetup Installation", eles são apresentados com a opção de salvar ou executar a partir desse local. se o usuário selecionar a execução nesse local, o Setup.exe atualizará a versão do Windows Installer em seu computador, se necessário, verificará a assinatura digital no pacote do instalador e instalará o pacote em seu computador.
-   Há um certificado digital, MyCert. cer, fornecido com uma chave privada, MyCert. pvk.
-   A URL do site hipotético que um cliente visitaria para instalar o pacote é https: \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   O layout do servidor Web é o seguinte. 

    | URL                                                               | Arquivo        | Descrição                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https: \/ /www.blueyonderairlines.com/products/mySetup/               | Setup.exe   | Setup.exe bootstrapper.                        |
    | https: \/ /www.blueyonderairlines.com/products/mySetup/               | MySetup.msi | Pacote de instalação                           |
    | https: \/ /www.blueyonderairlines.com/products/mySetup/               | Cab1.cab    | Gabinete do arquivo de origem \# 1                        |
    | https: \/ /www.blueyonderairlines.com/products/mySetup/               | Cab2.cab    | Gabinete do arquivo de origem \# 2                        |
    | https: \/ /www.blueyonderairlines.com/products/Common/InstMsi/ANSI    | Instmsi.exe | ANSI Windows Installer 2,0 redistribuível.    |
    | https: \/ /www.blueyonderairlines.com/products/Common/InstMsi/Unicode | Instmsi.exe | Unicode Windows Installer 2,0 redistribuível. |

    

     

[Continuar](configuring-the-setup-exe-resources.md)

 

 
