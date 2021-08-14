---
description: Formatos de extensão MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formatos de extensão MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a490c29c98b454b7d563e8af46131b040f123b9de2ef689ea5ede1a2ac100ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193952"
---
# <a name="mtp-extension-formats"></a>Formatos de extensão MTP

O formato de um arquivo em um dispositivo pode ser descrito por um valor de GUID. Esse valor é especificado pela propriedade de \_ formato de objeto WPD \_ .

## <a name="vendor-extended-formats"></a>Fornecedor-formatos estendidos

Quando um fabricante de dispositivo dá suporte a um formato estendido de fornecedor, seu driver combina o código de formato do fornecedor (UINT16) com os 16 bits mais altos do **\_ formato de objeto WPD \_ \_ não especificado** GUID.

Por exemplo, se o código estendido pelo fornecedor for 0xB001, o GUID resultante será como mostrado no exemplo a seguir:


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a extensões de MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



