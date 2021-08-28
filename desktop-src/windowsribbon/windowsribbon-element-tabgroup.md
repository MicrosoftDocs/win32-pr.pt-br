---
title: Elemento TabGroup
description: Representa um conjunto contextual de controles guia.
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- elemento TabGroup da faixa de Windows
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e2801ae8726fe10933b45e592e6f633f6455ea
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622092"
---
# <a name="tabgroup-element"></a>Elemento TabGroup

Representa um conjunto contextual de controles [guia](windowsribbon-controls-tabgroup.md) .

## <a name="usage"></a>Uso

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Type</th>
<th>Obrigatório</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                             | Descrição                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**Tab**](windowsribbon-element-tab.md)<br/> | Deve ocorrer pelo menos uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                 |
|-----------------------------------------------------------------------------------------|
| [**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer pelo menos uma vez para cada elemento [**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o elemento **TabGroup** .

Esta seção de código mostra uma declaração de comando **TabGroup** com duas guias contextuais.


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



Esta seção de código mostra as declarações de controle **TabGroup** correspondentes.


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



## <a name="element-information"></a>Informações do elemento

- **sistema mínimo com suporte**: Windows 7 
- **Pode estar vazio**: não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de grupo de guias](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[Controle guia](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





