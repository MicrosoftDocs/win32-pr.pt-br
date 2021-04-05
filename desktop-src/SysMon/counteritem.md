---
title: Objeto de coitem (Isysmon. h)
description: Use essa classe para recuperar o caminho e o valor de um contador e para especificar a cor usada para grafar o contador. Para recuperar esse objeto, chame Counters. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Objeto de coitem SysMon
- Objeto de coitem SysMon, descrito
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644753"
---
# <a name="counteritem-object"></a>Objeto de coitem

Use essa classe para recuperar o caminho e o valor de um contador e para especificar a cor usada para grafar o contador.

Para recuperar esse objeto, chame [**Counters. Item**](counters-item.md).

## <a name="members"></a>Membros

O objeto de **coitem** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto de **coitem** tem esses métodos.



| Método                                             | Descrição                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetDataAt**](counteritem-getdataat.md)         | Recupera os dados do contador de um ponto específico no gráfico de linhas.<br/> |
| [**Getstatistics**](counteritem-getstatistics.md) | Recupera os valores médio, máximo e mínimo para o contador.<br/> |
| [**GetValue**](counteritem-getvalue.md)           | Recupera o último valor do contador.<br/>                            |



 

### <a name="properties"></a>Propriedades

O objeto de **coitem** tem essas propriedades.



| Propriedade                                                  | Descrição                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Cor**](counteritem-color.md)<br/>             | Recupera ou define a cor usada para grafar o valor do contador.<br/>         |
| [**Estilo de Linha**](counteritem-linestyle.md)<br/>     | Recupera ou define o estilo de linha usado para grafar o valor do contador.<br/>    |
| [**Caminho**](counteritem-path.md)<br/>               | Recupera o caminho do contador.<br/>                                   |
| [**ScaleFactor**](counteritem-scalefactor.md)<br/> | Recupera ou define o fator de escala usado para grafar o valor do contador.<br/>  |
| [**Selected**](counteritem-selected.md)<br/>       | Recupera ou define um valor que indica se o contador está selecionado.<br/> |
| [**Valor**](counteritem-value.md)<br/>             | Recupera o valor atual do contador.<br/>                          |
| [**Visible**](counteritem-visible.md)<br/>         | Recupera ou define um valor que indica se o contador está grafado.<br/>  |
| [**Largura**](counteritem-width.md)<br/>             | Recupera ou define a largura da linha usada para grafar o valor do contador.<br/>    |



 

## <a name="remarks"></a>Comentários

O [**valor**](counteritem-value.md) é a propriedade padrão do **item de itens**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes SYSMON](sysmon-classes.md)
</dt> </dl>

 

 





