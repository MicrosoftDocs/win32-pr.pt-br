---
description: Um executável de inicialização configurável (Setup.exe) e uma ferramenta de configuração ( Msistuff.exe) estão incluídos nos Componentes do SDK do Windows para desenvolvedores do Windows Installer.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configurando os recursos Setup.exe dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c181453f689b7f2c273ba8726097e5d1cd134d1b9675c8ffc42de42d902b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638725"
---
# <a name="configuring-the-setupexe-resources"></a>Configurando os recursos Setup.exe dados

Um executável de inicialização configurável (Setup.exe) e uma ferramenta de configuração ( [Msistuff.exe](msistuff-exe.md)) estão incluídos nos Componentes do [SDK](platform-sdk-components-for-windows-installer-developers.md)do Windows para desenvolvedores do Windows Installer . Usando o Msistuff.exe para configurar os recursos no Setup.exe, os desenvolvedores podem criar facilmente uma instalação da Web de um Windows instalador. Para obter mais informações, consulte [Inicialização de download da Internet.](internet-download-bootstrapping.md)

Inserir a linha de comando a seguir configura os recursos para o exemplo descrito em Exemplo de instalação do instalador baseado [em URL Windows .](a-url-based-windows-installer-installation-example.md)

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continuar](sign-setup-exe-and-mysetup-msi.md)

 

 



