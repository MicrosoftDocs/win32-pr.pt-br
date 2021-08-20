---
description: Este exemplo ilustra como criar uma instalação baseada em URL de um Windows instalador.
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

Este exemplo ilustra como criar uma instalação baseada em URL de um Windows instalador. Para obter mais informações sobre como proteger instalações e usar certificados digitais, consulte [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).

Para reproduzir este exemplo, você precisa do [utilitário SignTool.](../seccrypto/signtool.md) Para obter detalhes, consulte a [Referência das Ferramentas de CryptoAPI](../seccrypto/cryptoapi-tools-reference.md) no Microsoft Windows Software Development Kit (SDK). Você também precisa [Msistuff.exe](msistuff-exe.md) e Setup.exe utilitários do SDK do Windows para desenvolvedores [Windows Instalador.](platform-sdk-components-for-windows-installer-developers.md) Para obter mais informações, consulte [Inicialização de download da Internet.](internet-download-bootstrapping.md)

O exemplo tem as seguintes especificações:

-   Quando os usuários visitam seu site e clicam no link "Instalação do MySetup", eles têm a opção de salvar ou executar nesse local. Se o usuário optar por executar a partir desse local, o Setup.exe atualizará a versão do Instalador do Windows em seu computador, se necessário, verificará a assinatura digital no pacote do instalador e instalará o pacote em seu computador.
-   Há um certificado digital, Mycert.cer, fornecido com uma chave privada, Mycert.pvk.
-   A URL do site hipotético que um cliente visitaria para instalar o pacote é https: \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   O layout do servidor Web é o seguinte. 

    | URL                                                               | Arquivo        | Descrição                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Setup.exe   | Setup.exe bootstrapper.                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | MySetup.msi | Pacote de instalação                           |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab1.cab    | Gabinete de arquivo de \# origem 1                        |
    | https: \/ /www.blueyonderairlines.com/Products/MySetup/               | Cab2.cab    | Gabinete de arquivo de origem \# 2                        |
    | https: \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Ansi    | Instmsi.exe | ANSI Windows Instalador 2.0 redistribuível.    |
    | https: \/ /www.blueyonderairlines.com/Products/Common/InstMsi/Unicode | Instmsi.exe | Unicode Windows Instalador 2.0 redistribuível. |

    

     

[Continuar](configuring-the-setup-exe-resources.md)

 

 
