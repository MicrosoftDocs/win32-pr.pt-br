---
description: Especifica uma versão localizada do nome do fabricante.
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: elemento manufacturerLS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5b6922e0d914048003b976ecf1f9a7b82febc2a9802334f1a125e357985e319
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794026"
---
# <a name="manufacturerls-element"></a>elemento manufacturerLS

Especifica uma versão localizada do nome do fabricante.

## <a name="usage"></a>Uso

``` syntax
<manufacturerLS
  Language = "language identifier string"
  Data = "localized manufacturer name string"/>
```

## <a name="attributes"></a>Atributos



| Atributo               | Type                                          | Obrigatório       | Descrição                                                             |
|-------------------------|-----------------------------------------------|----------------|-------------------------------------------------------------------------|
| **Dados**<br/>     | Cadeia de caracteres do nome do fabricante localizado<br/> | Sim<br/> | O nome do fabricante localizado.<br/> <br/>                 |
| **Idioma**<br/> | Cadeia de caracteres do identificador de idioma<br/>         | Sim<br/> | O idioma do nome do fabricante localizado.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                   | Descrição                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Define os metadados de modelo e fabricante para o dispositivo a ser implementado.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




