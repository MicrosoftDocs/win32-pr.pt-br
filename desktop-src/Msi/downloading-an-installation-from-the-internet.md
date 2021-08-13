---
description: Windows O instalador aceita um URL (Uniform Resource Locator) como uma origem válida para uma instalação.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Baixando uma instalação da Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5195b0ec0e5c36e7b6866232c498c02a9f4022d207cd86cc229a49ec5a5e8bac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637763"
---
# <a name="downloading-an-installation-from-the-internet"></a>Baixando uma instalação da Internet

Windows O instalador aceita um URL (Uniform Resource Locator) como uma origem válida para uma instalação. Windows O instalador pode instalar pacotes, patches e transformações de um local de URL.

Se o banco de dados de instalação estiver em uma URL, o instalador baixará o banco de dados para um local de cache antes de iniciar a instalação. O instalador também baixa os arquivos e arquivos de gabinete da origem da Internet que são apropriados para as seleções do usuário. consulte [um exemplo de instalação de Windows Installer baseado em URL](a-url-based-windows-installer-installation-example.md) para obter mais informações.

Por exemplo, para instalar um pacote com uma origem localizada em um servidor Web em https://server/share/package.msi , você pode usar as opções de [linha de comando](command-line-options.md) para instalar o pacote e definir propriedades [públicas](public-properties.md) .

msiexec/i https://server/share/package.msi *propriedade = valor*

Uma linha de comando como a mostrada anteriormente deve ser passada para o instalador para iniciar uma instalação de um navegador da Web. Em geral, você não deve baixar e instalar o pacote simplesmente clicando duas vezes no arquivo de .msi de dentro do navegador. Isso baixa o arquivo de .msi na pasta Temporary Internet Files e passa o seguinte comando para o instalador:

**msiexec/i c: \\ \\ arquivos de Internet temporários do Windows \\package.msi**

A instalação falhará se o pacote exigir arquivos de origem externos ou gabinetes, pois eles não estão localizados no mesmo local que o arquivo de .msi.

Observe que, como o objeto do [**instalador**](installer-object.md) não está marcado como [SafeForScripting](safeforscripting.md) no computador do usuário, os usuários precisam ajustar as configurações de segurança do navegador para que o exemplo funcione corretamente.

O método [**InstallProduct**](installer-installproduct.md) pode ser usado para executar o comando anterior de um navegador como um evento de clique.


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



Observe que, como alguns servidores Web diferenciam maiúsculas de minúsculas, o campo FileName na tabela de [arquivos](file-table.md) deve corresponder ao caso dos arquivos de origem exatamente para garantir o suporte de downloads da Internet.

Consulte [baixar e instalar um patch da Internet](downloading-and-installing-a-patch-from-the-internet.md). para obter mais informações sobre como proteger instalações e usar certificados digitais, consulte [diretrizes para a criação de instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md). para obter mais informações sobre como criar uma instalação da web de um pacote de Windows Installer, consulte [inicialização de Download da Internet](internet-download-bootstrapping.md).

## <a name="available-internet-protocols"></a>Protocolos de Internet disponíveis

a partir do Windows Server 2003 e Windows XP, o instalador pode usar os protocolos HTTP, HTTPS e FILE. O instalador não dá suporte aos protocolos FTP e GOPHER.

Windows A versão 2,0 do instalador pode usar os protocolos HTTP, arquivo e FTP e não pode usar os protocolos HTTPS e GOPHER.

 

 



