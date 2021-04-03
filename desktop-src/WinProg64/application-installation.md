---
title: Instalação de aplicativos em sistemas de 64 bits
description: O Windows Installer de 64 bits pode instalar diretamente aplicativos baseados em MSI de 32 bits em janelas de 64 bits.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- instalação de aplicativo 64-programação do Windows-bit
- Programação de instalação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084676"
---
# <a name="application-installation-on-64-bit-systems"></a><span data-ttu-id="abae4-105">Instalação de aplicativos em sistemas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="abae4-105">Application Installation on 64-bit Systems</span></span>

<span data-ttu-id="abae4-106">O [Windows Installer de 64 bits](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) pode instalar diretamente aplicativos baseados em MSI de 32 bits em janelas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="abae4-106">The [64-bit Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span> <span data-ttu-id="abae4-107">Para aplicativos mais antigos que usam um stub de 16 bits para iniciar um mecanismo de instalação de 32 bits, o Windows de 64 bits reconhece programas de instalador específicos de 16 bits e substitui uma versão de 32 bits portada.</span><span class="sxs-lookup"><span data-stu-id="abae4-107">For older applications that use a 16-bit stub to launch a 32-bit installation engine, 64-bit Windows recognizes specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span>

<span data-ttu-id="abae4-108">aplicativos DOS de 16 bits, do Windows ou do SO/2 geralmente usam um stub de 16 bits para verificar o tipo de computador e, em seguida, iniciar um mecanismo de instalação de 32 bits para realmente executar a instalação.</span><span class="sxs-lookup"><span data-stu-id="abae4-108">16-bit DOS, Windows, or OS/2 applications often use a 16-bit stub to check the machine type, then launch a 32-bit installation engine to actually perform the installation.</span></span> <span data-ttu-id="abae4-109">Para habilitar a instalação de aplicativos que usam essa técnica, o Windows de 64 bits substitui as versões de 32 bits pelos seguintes programas de instalação de 16 bits:</span><span class="sxs-lookup"><span data-stu-id="abae4-109">To enable installation of applications that use this technique, 64-bit Windows substitutes 32-bit versions for the following 16-bit installer programs:</span></span>

* <span data-ttu-id="abae4-110">Instalação da Microsoft para Windows 1,2</span><span class="sxs-lookup"><span data-stu-id="abae4-110">Microsoft Setup for Windows 1.2</span></span>  
* <span data-ttu-id="abae4-111">Instalação da Microsoft para Windows 2,6</span><span class="sxs-lookup"><span data-stu-id="abae4-111">Microsoft Setup for Windows 2.6</span></span>  
* <span data-ttu-id="abae4-112">Instalação da Microsoft para Windows 3,0</span><span class="sxs-lookup"><span data-stu-id="abae4-112">Microsoft Setup for Windows 3.0</span></span>  
* <span data-ttu-id="abae4-113">Instalação da Microsoft para Windows 3, 1</span><span class="sxs-lookup"><span data-stu-id="abae4-113">Microsoft Setup for Windows 3.01</span></span>  
* <span data-ttu-id="abae4-114">InstallShield 5. x</span><span class="sxs-lookup"><span data-stu-id="abae4-114">InstallShield 5.x</span></span>  

<span data-ttu-id="abae4-115">A lista de substituições é armazenada no registro na seguinte chave: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.</span><span class="sxs-lookup"><span data-stu-id="abae4-115">The list of substitutions is stored in the registry under the following key: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64**.</span></span>

> [!Note]  
> <span data-ttu-id="abae4-116">Esse mecanismo é fornecido apenas para compatibilidade com aplicativos de 32 bits que usam os programas do Microsoft Installer de 16 bits listados neste tópico.</span><span class="sxs-lookup"><span data-stu-id="abae4-116">This mechanism is provided only for compatibility with 32-bit applications that use the 16-bit Microsoft installer programs listed in this topic.</span></span> <span data-ttu-id="abae4-117">Não há suporte para a adição de programas de instalador de terceiros.</span><span class="sxs-lookup"><span data-stu-id="abae4-117">Addition of third-party installer programs is not supported.</span></span>

 

> [!Note]  
> <span data-ttu-id="abae4-118">Esse mecanismo não está incluído no Windows 10 no ARM.</span><span class="sxs-lookup"><span data-stu-id="abae4-118">This mechanism is not included on Windows 10 on ARM.</span></span>

 

 

 