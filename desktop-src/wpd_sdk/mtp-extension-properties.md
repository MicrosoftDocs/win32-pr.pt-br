---
description: Propriedades de extensão MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propriedades de extensão MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105808358"
---
# <a name="mtp-extension-properties"></a>Propriedades de extensão MTP

As propriedades descrevem objetos, propriedades, recursos e dispositivos.

## <a name="vendor-extended-object-properties"></a>Fornecedor-Propriedades de objeto estendido

Quando um fabricante de dispositivo cria uma propriedade estendida de fornecedor para um objeto de dispositivo, ele combina o GUID de **\_ Propriedades de \_ \_ \_ objeto estendido do fornecedor \_ \_ MTP** de propriedade com o código de propriedades do objeto para construir uma estrutura **PROPERTYKEY** .

Por exemplo, se o código de Propriedade do objeto for 0xD801, o **PROPERTYKEY** resultante será como mostrado no exemplo a seguir:


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Fornecedor-Propriedades do dispositivo estendido

Quando um fabricante de dispositivo cria uma propriedade estendida do fornecedor para um dispositivo, ele combina o GUID de **\_ Propriedades do \_ \_ \_ \_ dispositivo \_ estendido do fornecedor MTP do provedor** do objeto com o código de propriedade para construir uma estrutura **PROPERTYKEY** .

Por exemplo, se o código de Propriedade do objeto for 0xD001, o **PROPERTYKEY** resultante será como mostrado no exemplo a seguir:


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a extensões de MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



