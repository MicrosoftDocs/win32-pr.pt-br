---
title: Propriedade SplitButtonGallery. MenuGroups
description: Representa um contêiner para um conjunto de itens de menu suspenso em um controle SplitButtonGallery.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- propriedade SplitButtonGallery. MenuGroups Windows Ribbon
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 931a66ffca192a1655f3eeffc405c4c02c8e298c28fe9cb9d0d8c6612e29d793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441708"
---
# <a name="splitbuttongallerymenugroups-property"></a>Propriedade SplitButtonGallery. MenuGroups

Representa um contêiner para um conjunto de itens de menu suspenso em um controle [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="usage"></a>Uso

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                         | Descrição                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**Grupo Backstage**](windowsribbon-element-menugroup.md)<br/> | Deve ocorrer pelo menos uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez para cada elemento [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o elemento **SplitButtonGallery. MenuGroups** .

Esta seção de código mostra a declaração de controle **SplitButtonGallery. MenuGroups** .


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
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle da Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> </dl>

 

 





