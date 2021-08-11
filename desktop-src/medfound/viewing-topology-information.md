---
description: Exibindo informações de topologia
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Exibindo informações de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fd1d7d28de3d7fa5420241abf793295323532dca29d3d68d1271545aa460dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237368"
---
# <a name="viewing-topology-information"></a>Exibindo informações de topologia

No TopoEdit, cada item de topologia, como nós, entradas de nó e saídas de nó, tem um repositório de atributos associado que gerencia o comportamento do nó. Para ver os atributos, selecione o item e o **painel atributos** exibe as informações. Para topologias que são carregadas de um arquivo XML, alguns dos nós podem não exibir todo o repositório de atributos. Para ver todo o repositório de atributos, resolva a topologia. Para obter mais informações, consulte [resolvendo uma topologia com TopoEdit](resolving-a-topology-with-topoedit.md).

A tabela a seguir mostra o item de topologia e os atributos que o painel exibe.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item de topologia</th>
<th>Atributos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nós de topologia</td>
<td><ul>
<li><a href="topology-node-attributes.md">Atributos de nó de topologia</a> para todos os nós.<br/></li>
<li><a href="presentation-descriptor-attributes.md">Atributos de descritor de apresentação</a> somente para nós de origem.<br/></li>
<li>Informações de autoridade de confiança de entrada e saída para nós de transformação e saída.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Entrada de nó</td>
<td><ul>
<li><a href="media-type-attributes.md">Atributos de tipo de mídia</a> para todos os nós.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Saída de nó</td>
<td><ul>
<li><a href="stream-descriptor-attributes.md">Atributos de descritor de fluxo</a> somente para nós de origem.<br/></li>
<li><a href="media-type-attributes.md">Atributos de tipo de mídia</a> para todos os nós.<br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

Os valores de atributo, exceto para referências de ponteiro e valores de matriz, podem ser alterados. Para alterar um valor de atributo, digite o novo valor ao lado do atributo e clique em **salvar** no **painel atributos**. O novo valor é atualizado no repositório de atributos e aplicado à topologia somente depois que ele é resolvido.

## <a name="to-add-a-new-attribute-for-a-node"></a>Para adicionar um novo atributo para um nó

1.  Selecione o nó clicando nele no **painel topologia**.

    Os atributos definidos no nó são mostrados no **painel atributos**.

2.  No **painel atributos**, clique em **Adicionar**.

    Isso abre a caixa de diálogo **Adicionar atributo** .

3.  Na primeira lista suspensa, escolha a categoria de atributo.

    As categorias dependem do nó de topologia. Por exemplo, para o nó de origem, a lista suspensa mostra **atributos de descritor de apresentação** e atributos de **nó** como as categorias disponíveis.

4.  Na segunda lista suspensa, escolha o atributo que você deseja definir no nó.

5.  Na caixa de edição, adicione o valor para o atributo.

6.  Clique em **Adicionar** para adicionar o atributo e retornar à janela principal, ou clique em **Cancelar** para cancelar a operação.

7.  No menu **topologia** , clique em **resolver topologia** para definir o novo atributo para a topologia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




