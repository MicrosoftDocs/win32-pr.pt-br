---
description: 'Os valores do registro WFP estão localizados na seguinte chave do registro: HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: Valores de registro de WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758263"
---
# <a name="wfp-registry-values"></a><span data-ttu-id="dfb3f-103">Valores de registro de WFP</span><span class="sxs-lookup"><span data-stu-id="dfb3f-103">WFP Registry Values</span></span>

<span data-ttu-id="dfb3f-104">\[Não há suporte para valores de registro WFP a partir do Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="dfb3f-104">\[WFP registry values are not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="dfb3f-105">A WFP usa vários valores de registro para configurações de personalização.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-105">WFP uses several registry values for customization settings.</span></span> <span data-ttu-id="dfb3f-106">Os valores do registro WFP estão localizados na seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="dfb3f-106">The WFP registry values are located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

<span data-ttu-id="dfb3f-107">A seguir estão os valores do registro WFP.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-107">The following are the WFP registry values.</span></span>

<dl> <dt>

<span data-ttu-id="dfb3f-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span><span class="sxs-lookup"><span data-stu-id="dfb3f-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span></span>
</dt> <dd>

<span data-ttu-id="dfb3f-109">Local do cache.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-109">Location of the cache.</span></span> <span data-ttu-id="dfb3f-110">Esse deve ser um caminho local.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-110">This must be a local path.</span></span> <span data-ttu-id="dfb3f-111">O valor padrão é% SystemRoot% \\ System32 \\ dllcache.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-111">The default value is %systemroot%\\system32\\dllcache.</span></span>

</dd> <dt>

<span data-ttu-id="dfb3f-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span><span class="sxs-lookup"><span data-stu-id="dfb3f-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span></span>
</dt> <dd>

<span data-ttu-id="dfb3f-113">Opções de cota.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-113">Quota options.</span></span> <span data-ttu-id="dfb3f-114">Esse valor de registro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-114">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="dfb3f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb3f-115">Value</span></span>                  | <span data-ttu-id="dfb3f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="dfb3f-116">Meaning</span></span>                                                  |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="dfb3f-117">\_ \_ todos os arquivos da cota Sfc \_</span><span class="sxs-lookup"><span data-stu-id="dfb3f-117">SFC\_QUOTA\_ALL\_FILES</span></span> | <span data-ttu-id="dfb3f-118">O tamanho do cache de DLL é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-118">Size of the DLL cache is unlimited.</span></span> <span data-ttu-id="dfb3f-119">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-119">This is the default.</span></span> |
| <span data-ttu-id="dfb3f-120">Outros valores</span><span class="sxs-lookup"><span data-stu-id="dfb3f-120">Other values</span></span>           | <span data-ttu-id="dfb3f-121">Tamanho do cache de DLL, em arquivos.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-121">Size of the DLL cache, in files.</span></span>                         |



 

</dd> <dt>

<span data-ttu-id="dfb3f-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span><span class="sxs-lookup"><span data-stu-id="dfb3f-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span></span>
</dt> <dd>

<span data-ttu-id="dfb3f-123">Opções de verificação.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-123">Scan options.</span></span> <span data-ttu-id="dfb3f-124">Esse valor de registro pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-124">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="dfb3f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="dfb3f-125">Value</span></span>             | <span data-ttu-id="dfb3f-126">Significado</span><span class="sxs-lookup"><span data-stu-id="dfb3f-126">Meaning</span></span>                                                   |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="dfb3f-127">\_verificação \_ normal do Sfc</span><span class="sxs-lookup"><span data-stu-id="dfb3f-127">SFC\_SCAN\_NORMAL</span></span> | <span data-ttu-id="dfb3f-128">Não verificar arquivos protegidos na inicialização.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-128">Do not scan protected files at boot.</span></span> <span data-ttu-id="dfb3f-129">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-129">This is the default.</span></span> |
| <span data-ttu-id="dfb3f-130">verificação de SFC \_ \_ sempre</span><span class="sxs-lookup"><span data-stu-id="dfb3f-130">SFC\_SCAN\_ALWAYS</span></span> | <span data-ttu-id="dfb3f-131">Verificar arquivos protegidos em cada inicialização.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-131">Scan protected files at every boot.</span></span>                       |
| <span data-ttu-id="dfb3f-132">verificação de SFC \_ \_ uma vez</span><span class="sxs-lookup"><span data-stu-id="dfb3f-132">SFC\_SCAN\_ONCE</span></span>   | <span data-ttu-id="dfb3f-133">Verificar arquivos protegidos na próxima inicialização.</span><span class="sxs-lookup"><span data-stu-id="dfb3f-133">Scan protected files at the next boot.</span></span>                    |



 

</dd> </dl>

 

 



