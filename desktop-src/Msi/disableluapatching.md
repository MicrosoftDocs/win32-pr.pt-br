---
description: Se essa política do sistema por máquina estiver definida como &\# 0034; 1&\# 0034;, o instalador impedirá que não administradores usem a aplicação de patches do controle de conta de usuário (UAC) para qualquer aplicativo instalado no computador.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778724"
---
# <a name="disableluapatching"></a><span data-ttu-id="54457-103">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="54457-103">DisableLUAPatching</span></span>

<span data-ttu-id="54457-104">Se essa política do sistema por máquina for definida como "1", o instalador impedirá que não administradores usem a [aplicação de patch do controle de conta de usuário (UAC)](user-account-control--uac--patching.md) para qualquer aplicativo instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="54457-104">If this per-machine system policy is set to "1", the installer prevents non-administrators from using [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for any application installed on the computer.</span></span> <span data-ttu-id="54457-105">Quando a política do sistema por máquina não é definida ou definida como 0, os não administradores podem aplicar patches de usuário com privilégios mínimos a aplicativos habilitados para patches de conta de usuário com privilégios mínimos.</span><span class="sxs-lookup"><span data-stu-id="54457-105">When the per-machine system policy is not set or set to 0, non-administrators can apply least-privilege user patches to applications that are enabled for least-privilege user account patching.</span></span>

<span data-ttu-id="54457-106">Use a propriedade [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) para impedir a aplicação de patches com privilégios mínimos de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54457-106">Use the [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) property to prevent the least-privilege patching of an application.</span></span>

<span data-ttu-id="54457-107">A política DisableLUAPatching está disponível a partir do Windows Installer versão 3,0.</span><span class="sxs-lookup"><span data-stu-id="54457-107">The DisableLUAPatching policy is available beginning with Windows Installer version 3.0.</span></span>

## <a name="registry-key"></a><span data-ttu-id="54457-108">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="54457-108">Registry Key</span></span>

<span data-ttu-id="54457-109">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="54457-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="54457-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="54457-110">Data Type</span></span>

<span data-ttu-id="54457-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="54457-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="54457-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54457-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54457-113">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="54457-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



