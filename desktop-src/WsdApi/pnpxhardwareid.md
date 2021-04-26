---
description: Especifica o identificador de hardware PnP-X do serviço.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Elemento PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996523"
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



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




