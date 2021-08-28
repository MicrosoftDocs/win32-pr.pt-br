---
title: Propriedade DropDownGallery.MenuLayout
description: Representa um contêiner para layouts de menu suspenso DropDownGallery.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- Propriedade DropDownGallery.MenuLayout Windows Faixa de Opções
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b3fa4c0e2cca92aa2f95f73e0c817314bb71a8260db21a89cb40ec78fff7765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810676"
---
# <a name="dropdowngallerymenulayout-property"></a>Propriedade DropDownGallery.MenuLayout

Representa um contêiner para layouts de menu suspenso [**DropDownGallery.**](windowsribbon-element-dropdowngallery.md)

## <a name="usage"></a>Uso

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
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
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para [**cada elemento DropDownGallery.**](windowsribbon-element-dropdowngallery.md)

> [!Note]  
> Um máximo de um elemento filho ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) é permitido.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para [**o DropDownGallery**](windowsribbon-element-dropdowngallery.md).

Esta seção de código mostra a **declaração de controle DropDownGallery.MenuLayout.**


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controle da Galeria De lista listada**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> </dl>

 

 





