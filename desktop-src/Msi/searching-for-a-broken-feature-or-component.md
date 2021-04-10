---
description: O instalador pode aumentar a resiliência do aplicativo reinstalando automaticamente os componentes danificados.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Pesquisando um componente ou recurso desfeito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170049"
---
# <a name="searching-for-a-broken-feature-or-component"></a><span data-ttu-id="b7a96-103">Pesquisando um componente ou recurso desfeito</span><span class="sxs-lookup"><span data-stu-id="b7a96-103">Searching for a Broken Feature or Component</span></span>

<span data-ttu-id="b7a96-104">O instalador pode aumentar a [resiliência](resiliency.md) do aplicativo reinstalando automaticamente os componentes danificados.</span><span class="sxs-lookup"><span data-stu-id="b7a96-104">The installer can increase application [resiliency](resiliency.md) by automatically reinstalling damaged components.</span></span> <span data-ttu-id="b7a96-105">Especificamente, o instalador reinstalará um componente ou recurso se descobrir que o arquivo ou a chave do registro especificado na coluna KeyPath da [tabela de componentes](component-table.md) está ausente.</span><span class="sxs-lookup"><span data-stu-id="b7a96-105">Specifically, the installer reinstalls a component or feature if it finds that the file or registry key specified in the KeyPath column of the [Component table](component-table.md) is missing.</span></span>

<span data-ttu-id="b7a96-106">Se o caminho-fonte do componente de um recurso estiver danificado na origem ou se houver um erro em como o caminho keyé criado no banco de dados, o instalador poderá tentar abrir um pacote de instalação e reinstalar o recurso sempre que o atalho do recurso for ativado.</span><span class="sxs-lookup"><span data-stu-id="b7a96-106">If the KeyPath of a feature's component is damaged in the source, or if there is an error in how the KeyPath is authored in the database, the installer may attempt to open an installation package and reinstall the feature each time the feature's shortcut is activated.</span></span>

<span data-ttu-id="b7a96-107">Para determinar a causa de tentativas repetidas de reinstalar um recurso ou aplicativo, verifique o log de eventos em busca de duas entradas, como as seguintes.</span><span class="sxs-lookup"><span data-stu-id="b7a96-107">To determine the cause of repeated attempts to reinstall a feature or application, check the Event Log for two entries such as the following.</span></span>

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

<span data-ttu-id="b7a96-108">A primeira mensagem informa qual componente no pacote do produto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b7a96-108">The first message states which component in the product's package was being installed.</span></span> <span data-ttu-id="b7a96-109">Esse é o componente referenciado na \_ coluna componente da [tabela de atalho](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="b7a96-109">This is the component referenced in the Component\_ column of the [Shortcut table](shortcut-table.md).</span></span>

<span data-ttu-id="b7a96-110">A segunda mensagem informa qual componente está falhando na detecção.</span><span class="sxs-lookup"><span data-stu-id="b7a96-110">The second message states which component is failing detection.</span></span> <span data-ttu-id="b7a96-111">Esse é o componente com o caminho keyausente ou danificado que está disparando a reinstalação.</span><span class="sxs-lookup"><span data-stu-id="b7a96-111">This is the component with the missing or damaged KeyPath that's triggering the reinstall.</span></span>

 

 



