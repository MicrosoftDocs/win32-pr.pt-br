---
title: Redistribuindo o Windows Media Player 11
description: Redistribuindo o Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005292"
---
# <a name="redistributing-windows-media-player-11"></a><span data-ttu-id="734fa-103">Redistribuindo o Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="734fa-103">Redistributing Windows Media Player 11</span></span>

<span data-ttu-id="734fa-104">Você pode instalar o Windows Media Player 11 no Windows XP usando um dos programas de instalação a seguir, em que *LocaleID* é um identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="734fa-104">You can install Windows Media Player 11 on Windows XP by using one of the following setup programs, where *localeId* is a locale identifier.</span></span>

-   <span data-ttu-id="734fa-105">wmp11-windowsxp-x86-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="734fa-105">wmp11-windowsxp-x86-*localeId*.exe</span></span>
-   <span data-ttu-id="734fa-106">wmp11-windowsxp-x64-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="734fa-106">wmp11-windowsxp-x64-*localeId*.exe</span></span>

<span data-ttu-id="734fa-107">Aqui está um exemplo de uma linha de comando para instalação sem interface do usuário e nenhum prompt de reinicialização ou reinicialização.</span><span class="sxs-lookup"><span data-stu-id="734fa-107">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="734fa-108">A tabela a seguir mostra parâmetros adicionais que você pode usar com o programa de instalação do Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="734fa-108">The following table shows additional parameters that you can use with the Windows Media Player 11 setup program.</span></span>



| <span data-ttu-id="734fa-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="734fa-109">Parameter</span></span>              | <span data-ttu-id="734fa-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="734fa-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="734fa-111">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="734fa-111">/NoMigrate</span></span>             | <span data-ttu-id="734fa-112">Impedir a migração da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="734fa-112">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="734fa-113">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="734fa-113">/NestedRestore</span></span>         | <span data-ttu-id="734fa-114">Crie um ponto de restauração do sistema aninhado.</span><span class="sxs-lookup"><span data-stu-id="734fa-114">Create a nested system restore point.</span></span> <span data-ttu-id="734fa-115">Use esta se o aplicativo criar um ponto de restauração do sistema para aninhar o ponto de restauração do Windows Media Player no ponto de restauração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="734fa-115">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="734fa-116">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="734fa-116">/DisallowSystemRestore</span></span> | <span data-ttu-id="734fa-117">Não permitir a criação de um ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="734fa-117">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="734fa-118">Esse sinalizador desabilitará a criação de um ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="734fa-118">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="734fa-119">Na maioria das circunstâncias, esse sinalizador não deve ser usado para a redistribuição de software geral.</span><span class="sxs-lookup"><span data-stu-id="734fa-119">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="734fa-120">Isso deve ser usado somente quando você pode fazer uma escolha explícita em nome do usuário final para não oferecer suporte à reversão dos arquivos do Windows Media Player para uma versão anterior do Player.</span><span class="sxs-lookup"><span data-stu-id="734fa-120">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="734fa-121">Esse sinalizador deve ser usado somente para a implantação corporativa ou para a instalação do OEM (fabricante original do equipamento).</span><span class="sxs-lookup"><span data-stu-id="734fa-121">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="734fa-122">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="734fa-122">/DefaultService</span></span>        | <span data-ttu-id="734fa-123">Defina o repositório online inicial.</span><span class="sxs-lookup"><span data-stu-id="734fa-123">Set the initial online store.</span></span> <span data-ttu-id="734fa-124">Para obter mais informações, consulte [parâmetros de linha de comando de instalação para lojas online](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="734fa-124">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="734fa-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="734fa-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="734fa-126">**Redistribuindo o software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="734fa-126">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




