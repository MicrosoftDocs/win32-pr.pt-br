---
description: Para instalar assemblies lado a lado como assemblies privados, você pode instalar o assembly como um componente de um pacote do instalador.
ms.assetid: 1cfd836f-a1b9-4339-8756-5488c88b3c2b
title: Instalando assemblies lado a lado como assemblies privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7719a9887f9e92d81e2ad65fe2e75424f0b6957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748553"
---
# <a name="installing-side-by-side-assemblies-as-private-assemblies"></a><span data-ttu-id="44f5f-103">Instalando assemblies lado a lado como assemblies privados</span><span class="sxs-lookup"><span data-stu-id="44f5f-103">Installing Side-by-side Assemblies as Private Assemblies</span></span>

<span data-ttu-id="44f5f-104">Para instalar [assemblies lado a lado](about-side-by-side-assemblies-.md) como [assemblies privados](/windows/desktop/Msi/private-assemblies), você pode instalar o assembly como um componente de um pacote do instalador.</span><span class="sxs-lookup"><span data-stu-id="44f5f-104">To install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [private assemblies](/windows/desktop/Msi/private-assemblies), you can install the assembly as a component of an installer package.</span></span> <span data-ttu-id="44f5f-105">Esse pode ser o mesmo pacote de instalação usado para instalar ou atualizar seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44f5f-105">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="44f5f-106">Windows Installer versão 2,0 ou posterior é necessária para instalar assemblies.</span><span class="sxs-lookup"><span data-stu-id="44f5f-106">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="44f5f-107">Para obter mais informações, consulte o SDK do [Windows Installer](../msi/windows-installer-portal.md) e as seções em [instalação de assemblies do Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="44f5f-107">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="44f5f-108">Como alternativa, você pode usar o instalador para copiar um assembly privado e um manifesto na mesma pasta que o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44f5f-108">As an alternative, you can use the installer to copy a private assembly and manifest into the same folder as the application's executable file.</span></span>

 

 
