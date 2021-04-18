---
description: Windows Installer pode instalar, remover e atualizar assemblies do Win32 e assemblies usados pelo Common Language Runtime da estrutura de Microsoft .NET.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757131"
---
# <a name="assemblies"></a>Assemblies

Windows Installer pode instalar, remover e atualizar assemblies do Win32 e assemblies usados pelo Common Language Runtime da estrutura de Microsoft .NET. Um assembly é manipulado pelo Windows Installer como um único componente de instalador. Todos os arquivos que constituem um assembly devem estar contidos em um único componente de instalador listado na tabela de [componentes](component-table.md) .

Windows Installer em execução no Windows Vista e no Windows XP podem instalar assemblies lado a lado. Os assemblies lado a lado podem compartilhar com segurança assemblies entre vários aplicativos e podem deslocar os efeitos negativos do compartilhamento de assembly, como conflitos de DLL. Em vez de uma única versão de um assembly que assume compatibilidade com versões anteriores com todos os aplicativos, o compartilhamento de assembly lado a lado permite que várias versões de um assembly COM ou Win32 sejam executadas simultaneamente no sistema. Esse recurso aprimorado para isolar aplicativos é uma parte importante da estrutura de Microsoft .NET. Para obter mais informações, consulte [aplicativos isolados e assemblies lado a lado](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

As seções a seguir descrevem o uso de assemblies com o Windows Installer.

-   [Adicionando assemblies a um pacote](adding-assemblies-to-a-package.md)
-   [Instalando e removendo assemblies](installing-and-removing-assemblies.md)
-   [Atualizando assemblies](updating-assemblies.md)
-   [Modos de reinstalação de assemblies do Common Language Runtime](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Chaves do registro de assembly gravadas por Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)

Para obter informações sobre como instalar aplicativos COM e COM+ 1,0, consulte [instalando um aplicativo com+ com o Windows Installer](installing-a-com--application-with-the-windows-installer.md), [instalando um componente com em um local privado](installing-a-com-component-to-a-private-location.md)e [tornar um componente com em um pacote existente privado](make-a-com-component-in-an-existing-package-private.md).

 

 
