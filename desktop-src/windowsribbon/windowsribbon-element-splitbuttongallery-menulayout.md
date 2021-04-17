---
title: Propriedade SplitButtonGallery. MenuLayout
description: Representa um contêiner para layouts de menu suspenso da Galeria de botões de divisão.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- Faixa de SplitButtonGallery de propriedades do Windows. MenuLayout
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782692"
---
# <a name="splitbuttongallerymenulayout-property"></a>Propriedade SplitButtonGallery. MenuLayout

Representa um contêiner para layouts de menu suspenso da [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) .

## <a name="usage"></a>Uso

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Descrição                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Deve ocorrer exatamente uma vez<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

> [!Note]  
> Um máximo de um elemento filho ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) é permitido.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para a [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md).

Esta seção de código mostra a declaração de controle **SplitButtonGallery. MenuLayout** .


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle da Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> </dl>

 

 





