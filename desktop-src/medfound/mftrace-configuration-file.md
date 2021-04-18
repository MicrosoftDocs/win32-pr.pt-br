---
description: A ferramenta MFTrace pode ler um arquivo de configuração XML que especifica um ou mais provedores de rastreamento.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: Arquivo de configuração MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748727"
---
# <a name="mftrace-configuration-file"></a><span data-ttu-id="40a97-103">Arquivo de configuração MFTrace</span><span class="sxs-lookup"><span data-stu-id="40a97-103">MFTrace Configuration File</span></span>

<span data-ttu-id="40a97-104">A ferramenta [MFTrace](mftrace.md) pode ler um arquivo de configuração XML que especifica um ou mais provedores de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="40a97-104">The [MFTrace](mftrace.md) tool can read an XML configuration file that specifies one or more trace providers.</span></span>

<span data-ttu-id="40a97-105">O elemento [**Providers**](providers.md) é o elemento raiz no arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="40a97-105">The [**providers**](providers.md) element is the root element in the configuration file.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="40a97-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="40a97-106">In this section</span></span>

-   [<span data-ttu-id="40a97-107">**chaves**</span><span class="sxs-lookup"><span data-stu-id="40a97-107">**keyword**</span></span>](keyword.md)
-   [<span data-ttu-id="40a97-108">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="40a97-108">**mfdetours**</span></span>](mfdetours.md)
-   [<span data-ttu-id="40a97-109">**operador**</span><span class="sxs-lookup"><span data-stu-id="40a97-109">**provider**</span></span>](provider.md)
-   [<span data-ttu-id="40a97-110">**fornecedor**</span><span class="sxs-lookup"><span data-stu-id="40a97-110">**providers**</span></span>](providers.md)

## <a name="example"></a><span data-ttu-id="40a97-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="40a97-111">Example</span></span>

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a><span data-ttu-id="40a97-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40a97-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40a97-113">MFTrace</span><span class="sxs-lookup"><span data-stu-id="40a97-113">MFTrace</span></span>](mftrace.md)
</dt> </dl>

 

 



