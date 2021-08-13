---
description: Windows O instalador pode instalar, remover e atualizar assemblies e assemblies Win32 usados pelo Common Language Runtime do Microsoft .NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assemblies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a228dfad8155b9282f7ed5ee5c288a858f55c74c432ec6d21fd98aae58f98472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639268"
---
# <a name="assemblies"></a>Assemblies

Windows O instalador pode instalar, remover e atualizar assemblies e assemblies Win32 usados pelo Common Language Runtime do Microsoft .NET Framework. Um assembly é tratado pelo Windows instalador como um único componente do instalador. Todos os arquivos que constituem um assembly devem estar contidos por um único componente do instalador listado na [tabela Componente.](component-table.md)

Windows O instalador em execução no Windows Vista e Windows XP pode instalar assemblies lado a lado. Assemblies lado a lado podem compartilhar assemblies com segurança entre vários aplicativos e podem compensar os efeitos negativos do compartilhamento de assembly, como conflitos de DLL. Em vez de uma única versão de um assembly que assume compatibilidade com versões anteriores com todos os aplicativos, o compartilhamento de assembly lado a lado permite que várias versões de um assembly COM ou Win32 executem simultaneamente no sistema. Essa funcionalidade aprimorada para isolar aplicativos é uma parte importante do Microsoft .NET Framework. Para obter mais informações, [consulte Aplicativos isolados e Assemblies lado a lado.](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)

As seções a seguir descrevem o uso de assemblies com o Windows Instalador.

-   [Adicionando assemblies a um pacote](adding-assemblies-to-a-package.md)
-   [Instalando e removendo assemblies](installing-and-removing-assemblies.md)
-   [Atualizando assemblies](updating-assemblies.md)
-   [Modos de reinstalação de assemblies do Common Language Runtime](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Chaves do Registro de Assembly escritas pelo Windows Instalador](assembly-registry-keys-written-by-windows-installer-.md)

Para obter informações sobre como instalar aplicativos COM e COM+ 1.0, consulte [Installing a COM+ Application](installing-a-com--application-with-the-windows-installer.md)with the Windows Installer , [Installing](installing-a-com-component-to-a-private-location.md)a COM Component to a Private Location e [Make a COM Component in an Existing Package Private](make-a-com-component-in-an-existing-package-private.md).

 

 
