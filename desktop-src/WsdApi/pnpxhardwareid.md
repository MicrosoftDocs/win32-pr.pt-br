---
description: Especifica o Identificador de Hardware PnP-X do serviço.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d032974486d4bd43f0a699eba6b8f6b75598c49858eeedb09bae5d3e79b11e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311511"
---
# <a name="pnpxhardwareid-element"></a>Elemento PnPXHardwareId

Especifica o Identificador de Hardware PnP-X do serviço. O PnP corresponde a esse elemento com as descrições de hardware fornecidas na seção \[ PnpxDevice do arquivo \] INF do dispositivo. Com base nessa informação, o serviço PnP seleciona e carrega o driver de dispositivo mais apropriado.

## <a name="usage"></a>Uso

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                             | Descrição                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [**Hospedado**](hosted.md)<br/> | Define elementos para os serviços definidos pelo host de serviço. <br/> <br/> |



## <a name="remarks"></a>Comentários

Para especificar mais de uma ID de hardware, separe os identificadores com um caractere de espaço, por exemplo, "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".

## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




