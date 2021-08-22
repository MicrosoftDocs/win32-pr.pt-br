---
description: Você pode definir os atributos de transação manualmente usando a ferramenta administrativa serviços de componentes ou pode adicionar suporte programático a transações ao escrever seu componente.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Configurando o atributo de transação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6310d2544090d4b551a93782b4756b3d89f2d6d365dfc09aec4658d5d3e1b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546213"
---
# <a name="setting-the-transaction-attribute"></a>Configurando o atributo de transação

Você pode definir os atributos de transação manualmente usando a ferramenta administrativa serviços de componentes ou pode adicionar suporte programático a transações ao escrever seu componente.

Para obter mais informações sobre valores de atributo de transação, consulte [Configuring Transactions](configuring-transactions.md).

**Para definir o valor do atributo usando a ferramenta administrativa serviços de componentes**

1.  Na árvore de console, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do componente, clique na guia **Transações** .

3.  Em **suporte a transações**, selecione a opção para o valor desejado. **Não há suporte** para o valor padrão de todos os componentes.

4.  Clique em **OK**.

Você deve repetir este procedimento para cada componente.

## <a name="to-set-the-attribute-value-programmatically"></a>Para definir o valor do atributo programaticamente

os programadores que usam o Microsoft Visual Basic podem definir o atributo de transação com **MTSTransactionMode**, uma propriedade de módulo de classe para ActiveX projetos DLL. Visual Basic mapeia sua seleção para o valor equivalente de atributo de transação COM+ e publica o valor na biblioteca de tipos do componente.

A tabela a seguir mapeia cada valor constante **MTSTransactionMode** para seu valor de transação com+ equivalente.



| Constante MTSTransactionMode         | Valor da transação COM+             |
|-------------------------------------|------------------------------------|
| NotAnMTSObject (padrão)<br/> | Desabilitado<br/>                |
| Transtransações<br/>           | Sem suporte (padrão)<br/> |
| RequiresTransaction <br/>     | Obrigatório<br/>                |
| UsesTransaction <br/>         | Com suporte<br/>               |
| RequiresNewTransaction <br/>  | Requer novo<br/>            |



 

A propriedade **MTSTransactionMode** também pode ser acessada programaticamente usando a API da biblioteca de administração do com+.

 

 




