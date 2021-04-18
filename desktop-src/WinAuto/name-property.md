---
title: Propriedade Name
description: A propriedade Name é uma cadeia de caracteres usada pelos clientes para identificar, localizar ou anunciar um objeto para o usuário. Todos os objetos dão suporte à propriedade Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105807892"
---
# <a name="name-property"></a><span data-ttu-id="d5775-104">Propriedade Name</span><span class="sxs-lookup"><span data-stu-id="d5775-104">Name Property</span></span>

<span data-ttu-id="d5775-105">A propriedade **Name** é uma cadeia de caracteres usada pelos clientes para identificar, localizar ou anunciar um objeto para o usuário.</span><span class="sxs-lookup"><span data-stu-id="d5775-105">The **Name** property is a string used by clients to identify, find, or announce an object for the user.</span></span> <span data-ttu-id="d5775-106">Todos os objetos dão suporte à propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="d5775-106">All objects support the **Name** property.</span></span>

<span data-ttu-id="d5775-107">Por exemplo, o texto em um controle de botão é seu nome, enquanto o nome de uma caixa de listagem ou controle de edição é o texto estático que precede imediatamente o controle na ordem de tabulação.</span><span class="sxs-lookup"><span data-stu-id="d5775-107">For example, the text on a button control is its name, while the name for a list box or edit control is the static text that immediately precedes the control in the tabbing order.</span></span> <span data-ttu-id="d5775-108">Até mesmo objetos gráficos que não exibem um nome fornecem texto quando consultados para a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="d5775-108">Even graphic objects that do not display a name provide text when queried for the **Name** property.</span></span>

<span data-ttu-id="d5775-109">A propriedade **Name** é recuperada chamando [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span><span class="sxs-lookup"><span data-stu-id="d5775-109">The **Name** property is retrieved by calling [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span></span>

## <a name="selecting-names"></a><span data-ttu-id="d5775-110">Selecionando nomes</span><span class="sxs-lookup"><span data-stu-id="d5775-110">Selecting Names</span></span>

<span data-ttu-id="d5775-111">O nome de um objeto deve ser intuitivo para que os usuários compreendam o significado ou a finalidade do objeto.</span><span class="sxs-lookup"><span data-stu-id="d5775-111">An object's name should be intuitive so that users understand the object's meaning or purpose.</span></span> <span data-ttu-id="d5775-112">Além disso, a propriedade **Name** deve ser exclusiva em relação a qualquer objeto irmão no pai.</span><span class="sxs-lookup"><span data-stu-id="d5775-112">Also, the **Name** property should be unique relative to any sibling objects in the parent.</span></span>

<span data-ttu-id="d5775-113">A navegação dentro de tabelas apresenta problemas especialmente difíceis para alguns usuários.</span><span class="sxs-lookup"><span data-stu-id="d5775-113">Navigation within tables presents especially difficult problems for some users.</span></span> <span data-ttu-id="d5775-114">Portanto, os desenvolvedores de servidor devem tornar os nomes de célula da tabela o mais descritivo possível.</span><span class="sxs-lookup"><span data-stu-id="d5775-114">Therefore, server developers should make table cell names as descriptive as possible.</span></span> <span data-ttu-id="d5775-115">Por exemplo, você pode criar um nome de célula combinando os nomes da linha e coluna que ele ocupa, como "a1".</span><span class="sxs-lookup"><span data-stu-id="d5775-115">For example, you could create a cell name by combining the names of the row and column it occupies, such as "A1."</span></span> <span data-ttu-id="d5775-116">No entanto, geralmente é melhor usar nomes mais descritivos, como "Nancy, fevereiro", em que "Nancy" é a linha atual e "fevereiro" é a coluna atual.</span><span class="sxs-lookup"><span data-stu-id="d5775-116">However, it is generally better to use more descriptive names, such as "Nancy, February" where "Nancy" is the current row and "February" is the current column.</span></span>

## <a name="delegating-requests"></a><span data-ttu-id="d5775-117">Delegando solicitações</span><span class="sxs-lookup"><span data-stu-id="d5775-117">Delegating Requests</span></span>

<span data-ttu-id="d5775-118">Se um objeto não tiver acesso à sua propriedade **Name** , ele delegará solicitações para seu pai, identificando-se por sua ID filho.</span><span class="sxs-lookup"><span data-stu-id="d5775-118">If an object does not have access to its **Name** property, it delegates requests to its parent, identifying itself by its child ID.</span></span> <span data-ttu-id="d5775-119">Por exemplo, se um cliente chama a propriedade **Name** de um controle de edição, o controle de edição delega a consulta para seu pai, que retorna o valor do controle de texto estático que rotula o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="d5775-119">For example, if a client calls an edit control's **Name** property, the edit control delegates the query to its parent, which returns the value of the static text control that labels the edit control.</span></span>

 

 




