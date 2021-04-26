---
description: 'Impede a geração de instruções de importação para destinos especificados nomeados em um elemento wsdl: Import em um arquivo WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: elemento excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995873"
---
# <a name="excludeimport-element"></a>elemento excludeImport

Impede a geração de instruções de importação para destinos especificados nomeados em um \<wsdl:import> elemento em um arquivo WSDL. Isso pode ser usado para impedir que o WsdCodeGen importe destinos conhecidos, como as especificações de WS-Addressing e WS-Eventing, embora esses destinos sejam referenciados no WSDL.

O valor desse elemento deve ser definido como o namespace nomeado no \<wsdl:import> elemento a ser excluído.

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



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Sim           |



 

 




