---
description: Um executável de Bootstrap configurável (Setup.exe) e a ferramenta de configuração (Msistuff.exe) estão incluídos nos componentes SDK do Windows para os desenvolvedores de Windows Installer.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configurando os recursos de Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105747985"
---
# <a name="configuring-the-setupexe-resources"></a>Configurando os recursos de Setup.exe

Um executável de Bootstrap configurável (Setup.exe) e a ferramenta de configuração ( [Msistuff.exe](msistuff-exe.md)) estão incluídos nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Usando Msistuff.exe para configurar os recursos no Setup.exe, os desenvolvedores podem criar facilmente uma instalação da Web de um pacote Windows Installer. Para obter mais informações, consulte [inicialização de download da Internet](internet-download-bootstrapping.md).

A inserção da linha de comando a seguir configura os recursos para o exemplo descrito em [um exemplo de instalação com base em URL Windows Installer](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continuar](sign-setup-exe-and-mysetup-msi.md)

 

 



