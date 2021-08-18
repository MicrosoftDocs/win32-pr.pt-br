---
description: Windows O instalador aceita uma URL (Uniform Resource Locator) como uma fonte válida para uma instalação.
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

Windows O instalador aceita uma URL (Uniform Resource Locator) como uma fonte válida para uma instalação. Windows O instalador pode instalar pacotes, patches e transformar de um local de URL.

Se o banco de dados de instalação estiver em uma URL, o instalador baixará o banco de dados para um local de cache antes de iniciar a instalação. O instalador também baixa os arquivos e arquivos de gabinete da fonte da Internet apropriados para as seleções do usuário. Consulte [Um exemplo de instalação do Windows instalador baseado](a-url-based-windows-installer-installation-example.md) em URL para obter mais informações.

Por exemplo, para instalar um pacote com uma origem localizada em um servidor Web em , você pode usar as opções de linha de comando para instalar o pacote e https://server/share/package.msi definir [propriedades](public-properties.md) públicas. [](command-line-options.md)

msiexec /i https://server/share/package.msi *PROPERTY=VALUE*

Uma linha de comando como a mostrada anteriormente deve ser passada para o instalador para iniciar uma instalação de um navegador da Web. Em geral, você não deve baixar e instalar o pacote simplesmente clicando duas vezes no arquivo .msi de dentro do navegador. Isso baixa o arquivo .msi para a pasta de arquivos temporários da Internet e passa o seguinte comando para o instalador:

**msiexec /i c: arquivos de Internet temporários \\ do Windows \\ \\package.msi**

A instalação falhará se o pacote exigir arquivos de origem externos ou gabinetes porque eles não estão localizados no mesmo local que o arquivo .msi.

Observe que, como o objeto [**Instalador**](installer-object.md) não está marcado como [SafeForScripting](safeforscripting.md) no computador do usuário, os usuários precisam ajustar as configurações de segurança do navegador para que o exemplo funcione corretamente.

O [**método InstallProduct**](installer-installproduct.md) pode ser usado para executar o comando anterior de um navegador como um evento ao clicar.


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



Observe que, como alguns servidores Web são sensíveis a minúsculas, o campo FileName na tabela Arquivo deve corresponder ao caso dos arquivos de origem exatamente para garantir o suporte de downloads da Internet. [](file-table.md)

Consulte [Baixando e instalando um patch da Internet.](downloading-and-installing-a-patch-from-the-internet.md) Para obter mais informações sobre como proteger instalações e usar certificados digitais, consulte [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md). Para obter mais informações sobre como criar uma instalação da Web de um pacote Windows Instalador da Internet, consulte [Inicialização de Download da Internet](internet-download-bootstrapping.md).

## <a name="available-internet-protocols"></a>Protocolos de Internet disponíveis

A partir do Windows Server 2003 e Windows XP, o instalador pode usar os protocolos HTTP, HTTPS e FILE. O instalador não dá suporte aos protocolos FTP e GOPHER.

Windows O instalador versão 2.0 pode usar os protocolos HTTP, FILE e FTP e não pode usar os protocolos HTTPS e GOPHER.

 

 



