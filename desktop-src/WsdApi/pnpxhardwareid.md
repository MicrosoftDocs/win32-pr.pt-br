---
description: Especifica o identificador de hardware PnP-X do serviço.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781578"
---
# <a name="pnpxhardwareid-element"></a>Elemento PnPXHardwareId

Especifica o identificador de hardware PnP-X do serviço. O PnP corresponde a esse elemento com as descrições de hardware fornecidas na \[ seção PnpxDevice \] do arquivo inf do dispositivo. Com base nessas informações, o serviço PnP seleciona e carrega o driver de dispositivo mais apropriado.

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
| [**hospedado**](hosted.md)<br/> | Define elementos para os serviços definidos pelo host de serviço. <br/> <br/> |



## <a name="remarks"></a>Comentários

Para especificar mais de uma ID de hardware, separe os identificadores com um caractere de espaço, por exemplo, "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".

## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




