---
title: Redistribuindo o Windows Media Player 10
description: Redistribuindo o Windows Media Player 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635038"
---
# <a name="redistributing-windows-media-player-10"></a><span data-ttu-id="606f9-103">Redistribuindo o Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="606f9-103">Redistributing Windows Media Player 10</span></span>

<span data-ttu-id="606f9-104">Você pode instalar o Windows Media Player 10 no Windows XP usando o programa de instalação a seguir.</span><span class="sxs-lookup"><span data-stu-id="606f9-104">You can install Windows Media Player 10 on Windows XP by using the following setup program.</span></span>

-   <span data-ttu-id="606f9-105">MP10Setup.exe</span><span class="sxs-lookup"><span data-stu-id="606f9-105">MP10Setup.exe</span></span>

<span data-ttu-id="606f9-106">Aqui está um exemplo de uma linha de comando para instalação sem interface do usuário e nenhum prompt de reinicialização ou reinicialização.</span><span class="sxs-lookup"><span data-stu-id="606f9-106">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="606f9-107">A tabela a seguir mostra parâmetros adicionais que você pode usar com o programa de instalação do Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="606f9-107">The following table shows additional parameters that you can use with the Windows Media Player 10 setup program.</span></span>



| <span data-ttu-id="606f9-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="606f9-108">Parameter</span></span>              | <span data-ttu-id="606f9-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="606f9-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="606f9-110">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="606f9-110">/NoMigrate</span></span>             | <span data-ttu-id="606f9-111">Impedir a migração da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="606f9-111">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="606f9-112">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="606f9-112">/NestedRestore</span></span>         | <span data-ttu-id="606f9-113">Crie um ponto de restauração do sistema aninhado.</span><span class="sxs-lookup"><span data-stu-id="606f9-113">Create a nested system restore point.</span></span> <span data-ttu-id="606f9-114">Use esta se o aplicativo criar um ponto de restauração do sistema para aninhar o ponto de restauração do Windows Media Player no ponto de restauração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="606f9-114">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="606f9-115">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="606f9-115">/DisallowSystemRestore</span></span> | <span data-ttu-id="606f9-116">Não permitir a criação de um ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="606f9-116">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="606f9-117">Esse sinalizador desabilitará a criação de um ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="606f9-117">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="606f9-118">Na maioria das circunstâncias, esse sinalizador não deve ser usado para a redistribuição de software geral.</span><span class="sxs-lookup"><span data-stu-id="606f9-118">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="606f9-119">Isso deve ser usado somente quando você pode fazer uma escolha explícita em nome do usuário final para não oferecer suporte à reversão dos arquivos do Windows Media Player para uma versão anterior do Player.</span><span class="sxs-lookup"><span data-stu-id="606f9-119">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="606f9-120">Esse sinalizador deve ser usado somente para a implantação corporativa ou para a instalação do OEM (fabricante original do equipamento).</span><span class="sxs-lookup"><span data-stu-id="606f9-120">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="606f9-121">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="606f9-121">/DefaultService</span></span>        | <span data-ttu-id="606f9-122">Defina o repositório online inicial.</span><span class="sxs-lookup"><span data-stu-id="606f9-122">Set the initial online store.</span></span> <span data-ttu-id="606f9-123">Para obter mais informações, consulte [parâmetros de linha de comando de instalação para lojas online](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="606f9-123">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="606f9-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="606f9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="606f9-125">**Redistribuindo o software Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="606f9-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> <dt>

[<span data-ttu-id="606f9-126">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="606f9-126">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




