---
description: 'Impede a geração de instruções de importação para destinos especificados nomeados em um elemento <WSDL: Import> em um arquivo WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827829"
---
# <a name="excludeimport-element"></a>elemento excludeImport

Impede a geração de instruções de importação para destinos especificados nomeados em um elemento <WSDL: Import> em um arquivo WSDL. Isso pode ser usado para impedir que o WsdCodeGen importe destinos conhecidos, como as especificações de WS-Addressing e WS-Eventing, embora esses destinos sejam referenciados no WSDL.

O valor desse elemento deve ser definido como o namespace nomeado no elemento <WSDL: Import> a ser excluído.

## <a name="usage"></a>Uso

``` syntax
<excludeImport/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**WSDL**](wsdl.md)<br/> | Especifica um arquivo WSDL para processar informações de contrato.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




