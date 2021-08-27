---
description: A interface IExtender fornece um conjunto de propriedades básicas que são adicionadas à interface de um controle . Os programadores podem usar essas propriedades como se fossem parte do controle.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Interface IExtender
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: a341f5d8a0ec554f008232f44156486df83d0fd8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625103"
---
# <a name="iextender-interface"></a>Interface IExtender

A interface **IExtender** fornece um conjunto de propriedades básicas que são adicionadas à interface de um controle . Os programadores podem usar essas propriedades como se fossem parte do controle.

## <a name="members"></a>Membros

A interface **IExtender** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **O IExtender** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **interface IExtender** tem esses métodos.



| Método                         | Descrição                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Mover**](iextender-move.md) | Move um MDIForm, formulário ou controle.<br/> |



 

### <a name="properties"></a>Propriedades

A **interface IExtender** tem essas propriedades.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Propriedade</th>
<th >Tipo de acesso</th>
<th >Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td >Alinhar<br/></td>
<td >Leitura/gravação<br/></td>
<td >Retorna ou define um valor que determina se um objeto é exibido em qualquer tamanho em qualquer lugar em um formulário ou se ele é exibido na parte superior, inferior, esquerda ou direita do formulário e é dimensionado automaticamente para se ajustar à largura do formulário.<br/> 
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vbAlignNone 0</td>
<td>(Padrão em um formulário não MDI) Nenhum — tamanho e local podem ser definidos em tempo de design ou no código. A configuração será ignorada se o objeto estiver em um formulário MDI.</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td>(Padrão em um formulário MDI) Superior – o objeto está na parte superior do formulário e sua largura é igual à configuração de propriedade ScaleWidth do formulário.</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>Inferior – o objeto está na parte inferior do formulário e sua largura é igual à configuração de propriedade ScaleWidth do formulário.</td>
</tr>
<tr class="even">
<td>vbAlignLeft 3</td>
<td>Left – o objeto está à esquerda do formulário e sua largura é igual à configuração de propriedade ScaleWidth do formulário.</td>
</tr>
<tr class="odd">
<td>vbAlignRight 4</td>
<td>Direita – o objeto está à direita do formulário e sua largura é igual à configuração de propriedade ScaleWidth do formulário.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><p>Contêiner</p></td>
<td ><p>Somente leitura</p></td>
<td ><p>Retorna o contêiner de um controle em um formulário.</p></td>
</tr>
<tr class="odd">
<td ><p>Habilitada</p></td>
<td ><p>Leitura/gravação</p></td>
<td ><p>Retorna ou define um valor que determina se um formulário ou controle pode responder a eventos gerados pelo usuário.</p></td>
</tr>
<tr class="even">
<td ><p>Altura</p></td>
<td ><p>Leitura/gravação</p></td>
<td ><p>Retorna ou define a altura de um objeto .</p></td>
</tr>
<tr class="odd">
<td ><p>Hwnd</p></td>
<td ><p>Somente leitura</p></td>
<td ><p>Retorna um alça para um formulário ou controle.</p></td>
</tr>
<tr class="even">
<td ><p>Esquerda</p></td>
<td ><p>Leitura/gravação</p></td>
<td ><p>Retorna ou define a distância entre a borda esquerda interna de um objeto e a borda esquerda de seu contêiner.</p></td>
</tr>
<tr class="odd">
<td ><p>Nome</p></td>
<td ><p>Somente leitura</p></td>
<td ><p>Retorna o nome usado no código para identificar um formulário, controle ou objeto de acesso a dados.</p></td>
</tr>
<tr class="even">
<td ><p>Pai</p></td>
<td ><p>Somente leitura</p></td>
<td ><p>Retorna o formulário, o objeto ou a coleção que contém um controle ou outro objeto ou coleção.</p></td>
</tr>
<tr class="odd">
<td ><p>TabStop</p></td>
<td ><p>Leitura/gravação</p></td>
<td ><p>Retorna ou define um valor que indica se um usuário pode usar a tecla <strong>Tab</strong> para dar o foco a um objeto .</p></td>
</tr>
<tr class="even">
<td ><p>Parte superior</p></td>
<td ><p>Leitura/gravação</p></td>
<td ><p>Retorna ou define a distância entre a borda superior interna de um objeto e a borda superior de seu contêiner.</p></td>
</tr>
<tr class="odd">
<td ><p>Visible</p></td>
<td ><p>Leitura/gravação</p></td>
<td ><p>Retorna ou define um valor que indica se um objeto está visível ou oculto.</p></td>
</tr>
<tr class="even">
<td ><p>Largura</p></td>
<td ><p>Leitura/gravação</p></td>
<td ><p>Retorna ou define a largura de um objeto .</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
