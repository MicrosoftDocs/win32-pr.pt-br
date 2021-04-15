---
description: Se essa política do sistema por máquina for definida como um valor maior que 0, Windows Installer salvará versões mais antigas de arquivos em um cache quando um patch for aplicado a um aplicativo.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461195"
---
# <a name="maxpatchcachesize"></a><span data-ttu-id="ef830-103">MaxPatchCacheSize</span><span class="sxs-lookup"><span data-stu-id="ef830-103">MaxPatchCacheSize</span></span>

<span data-ttu-id="ef830-104">Se essa [política do sistema](system-policy.md) por máquina for definida como um valor maior que 0, Windows Installer salvará versões mais antigas de arquivos em um cache quando um patch for aplicado a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ef830-104">If this per-machine [system policy](system-policy.md) is set to a value greater than 0, Windows Installer saves older versions of files in a cache when a patch is applied to an application.</span></span> <span data-ttu-id="ef830-105">O Caching pode aumentar o desempenho de instalações futuras que, de outra forma, precisam obter os arquivos antigos de uma fonte de aplicativo original.</span><span class="sxs-lookup"><span data-stu-id="ef830-105">Caching can increase the performance of future installations that otherwise need to obtain the old files from a original application source.</span></span>

<span data-ttu-id="ef830-106">O valor da política MaxPatchCacheSize é o percentual máximo de espaço em disco que o instalador pode usar para o cache de arquivos antigos.</span><span class="sxs-lookup"><span data-stu-id="ef830-106">The value of the MaxPatchCacheSize policy is the maximum percentage of disk space that the installer can use for the cache of old files.</span></span> <span data-ttu-id="ef830-107">Por exemplo, um valor de 20 especifica no máximo 20% de uso.</span><span class="sxs-lookup"><span data-stu-id="ef830-107">For example, a value of 20 specifies no more than 20% be used.</span></span> <span data-ttu-id="ef830-108">Se o tamanho total do cache atingir a porcentagem especificada de espaço em disco, nenhum arquivo adicional será salvo no cache.</span><span class="sxs-lookup"><span data-stu-id="ef830-108">If the total size of the cache reaches the specified percentage of disk space, no additional files are saved to the cache.</span></span> <span data-ttu-id="ef830-109">A política não afeta os arquivos que já foram salvos.</span><span class="sxs-lookup"><span data-stu-id="ef830-109">The policy does not affect files that have already been saved.</span></span>

<span data-ttu-id="ef830-110">Se o valor da política MaxPatchCacheSize for definido como 0, nenhum arquivo adicional será salvo.</span><span class="sxs-lookup"><span data-stu-id="ef830-110">If the value of the MaxPatchCacheSize policy is set to 0, no additional files are saved.</span></span>

<span data-ttu-id="ef830-111">Se a política MaxPatchCacheSize não estiver definida, o valor padrão será 10 e um máximo de 10% do espaço em disco poderá ser usado para salvar arquivos antigos.</span><span class="sxs-lookup"><span data-stu-id="ef830-111">If the MaxPatchCacheSize policy is not set, the default value is 10 and a maximum of 10% of the disk space can be used to save old files.</span></span>

## <a name="registry-key"></a><span data-ttu-id="ef830-112">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="ef830-112">Registry Key</span></span>

<span data-ttu-id="ef830-113">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="ef830-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="ef830-114">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="ef830-114">Data Type</span></span>

<span data-ttu-id="ef830-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ef830-115">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef830-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ef830-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef830-117">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="ef830-117">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



