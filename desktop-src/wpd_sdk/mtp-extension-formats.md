---
description: Formatos de extensão MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formatos de extensão MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808359"
---
# <a name="mtp-extension-formats"></a><span data-ttu-id="5217c-103">Formatos de extensão MTP</span><span class="sxs-lookup"><span data-stu-id="5217c-103">MTP Extension Formats</span></span>

<span data-ttu-id="5217c-104">O formato de um arquivo em um dispositivo pode ser descrito por um valor de GUID.</span><span class="sxs-lookup"><span data-stu-id="5217c-104">The format of a file on a device can be described by a GUID value.</span></span> <span data-ttu-id="5217c-105">Esse valor é especificado pela propriedade de \_ formato de objeto WPD \_ .</span><span class="sxs-lookup"><span data-stu-id="5217c-105">This value is specified by the WPD\_OBJECT\_FORMAT property.</span></span>

## <a name="vendor-extended-formats"></a><span data-ttu-id="5217c-106">Fornecedor-formatos estendidos</span><span class="sxs-lookup"><span data-stu-id="5217c-106">Vendor-Extended Formats</span></span>

<span data-ttu-id="5217c-107">Quando um fabricante de dispositivo dá suporte a um formato estendido de fornecedor, seu driver combina o código de formato do fornecedor (UINT16) com os 16 bits mais altos do **\_ formato de objeto WPD \_ \_ não especificado** GUID.</span><span class="sxs-lookup"><span data-stu-id="5217c-107">When a device manufacturer supports a vendor-extended format, their driver combines the vendor's format code (UINT16) with the highest 16 bits of the **WPD\_OBJECT\_FORMAT\_UNSPECIFIED** GUID.</span></span>

<span data-ttu-id="5217c-108">Por exemplo, se o código estendido pelo fornecedor for 0xB001, o GUID resultante será como mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="5217c-108">For example, if the vendor-extended code is 0xB001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a><span data-ttu-id="5217c-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5217c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5217c-110">Suporte a extensões de MTP</span><span class="sxs-lookup"><span data-stu-id="5217c-110">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



