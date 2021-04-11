---
description: Microsoft Windows Installer aceita um URL (Uniform Resource Locator) como uma fonte válida para um patch.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Baixando e instalando um patch da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090784"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>Baixando e instalando um patch da Internet

Microsoft Windows Installer aceita um URL (Uniform Resource Locator) como uma fonte válida para um [patch](patch-packages.md). Para instalar um patch localizado em um servidor Web em https://MyWeb/MyPatch.msp , use a seguinte linha de comando:

**msiexec/p https://MyWeb/MyPatch.msp**

Para evitar resultados inesperados, não inicie um patch clicando no link na página da Web mostrando a URL do arquivo de patch. Você também pode instalar um patch usando um script como o seguinte:


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



Observe que, como o objeto do [**instalador**](installer-object.md) não está marcado como [SafeForScripting](safeforscripting.md) no computador do usuário, os usuários precisam ajustar as configurações de segurança do navegador para que o exemplo funcione corretamente.

Para obter mais informações, consulte [diretrizes para criar instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pacotes de patch](patch-packages.md)
</dt> <dt>

[Criando um pacote de patch](creating-a-patch-package.md)
</dt> <dt>

[Aplicação de patch em aplicativos personalizados](patching-customized-applications.md)
</dt> <dt>

[Baixando uma instalação da Internet](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



