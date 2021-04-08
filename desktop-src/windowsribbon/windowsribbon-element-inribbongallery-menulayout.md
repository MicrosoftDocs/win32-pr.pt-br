---
title: Propriedade InRibbonGallery. MenuLayout
description: Representa um contêiner para layouts de menu suspenso da Galeria de In-Ribbon.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Faixa de InRibbonGallery de propriedades do Windows. MenuLayout
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008952"
---
# <a name="inribbongallerymenulayout-property"></a>Propriedade InRibbonGallery. MenuLayout

Representa um contêiner para layouts de menu suspenso [da Galeria de faixa de](windowsribbon-controls-inribbongallery.md) opção.

## <a name="usage"></a>Uso

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Descrição                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Deve ocorrer exatamente uma vez<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada elemento [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .

> [!Note]  
> Um máximo de um elemento filho ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) é permitido.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para a [Galeria na faixa de](windowsribbon-controls-inribbongallery.md)opções.

Esta seção de código mostra a declaração de controle **InRibbonGallery. MenuLayout** .


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle da Galeria de faixa de bits](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> </dl>

 

 





