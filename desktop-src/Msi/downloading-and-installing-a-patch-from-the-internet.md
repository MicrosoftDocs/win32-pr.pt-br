---
description: O Microsoft Windows Installer aceita uma URL (Uniform Resource Locator) como uma fonte válida para um patch.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Baixando e instalando um patch da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f662279ac929d831bb69acc597358c8eddc509738fc71a43df44ec186120c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947350"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>Baixando e instalando um patch da Internet

O Microsoft Windows Installer aceita uma URL (Uniform Resource Locator) como uma fonte válida para um [patch](patch-packages.md). Para instalar um patch localizado em um servidor Web em , use a https://MyWeb/MyPatch.msp seguinte linha de comando:

**msiexec /p https://MyWeb/MyPatch.msp**

Para evitar resultados inesperados, não iniciar um patch clicando no link na página da Web mostrando a URL do arquivo de patch. Você também pode instalar um patch usando um script como o seguinte:


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



Observe que, como o objeto [**Instalador**](installer-object.md) não está marcado como [SafeForScripting](safeforscripting.md) no computador do usuário, os usuários precisam ajustar as configurações de segurança do navegador para que o exemplo funcione corretamente.

Para obter mais informações, consulte [Diretrizes para a implantação de](guidelines-for-authoring-secure-installations.md) instalações seguras e [assinaturas digitais e Windows Instalador .](digital-signatures-and-windows-installer.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pacotes de patch](patch-packages.md)
</dt> <dt>

[Criando um pacote de patch](creating-a-patch-package.md)
</dt> <dt>

[Aplicando patches em aplicativos personalizados](patching-customized-applications.md)
</dt> <dt>

[Baixando uma instalação da Internet](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



