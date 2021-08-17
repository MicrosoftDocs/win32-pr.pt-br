---
description: Propriedades de extensão MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propriedades de extensão MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0468d249b469c4e768962ab6a920935e7a64b51d8e035af111e8274f7f0b9af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193942"
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

 

 



