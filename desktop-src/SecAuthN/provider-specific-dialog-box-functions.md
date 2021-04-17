---
description: As funções de caixa de diálogo específicas do provedor permitem que um provedor exiba e manipule informações específicas da rede alterando caixas de diálogo do sistema ou exibindo caixas de diálogo personalizadas.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Funções da caixa de diálogo Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748871"
---
# <a name="provider-specific-dialog-box-functions"></a><span data-ttu-id="c67c1-103">Funções da caixa de diálogo Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="c67c1-103">Provider-Specific Dialog Box Functions</span></span>

<span data-ttu-id="c67c1-104">As funções de caixa de diálogo específicas do provedor permitem que um provedor exiba e manipule informações específicas da rede alterando caixas de diálogo do sistema ou exibindo caixas de diálogo personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c67c1-104">Provider-specific dialog box functions enable a provider to display and handle network-specific information by altering system dialog boxes or displaying custom dialog boxes.</span></span>

<span data-ttu-id="c67c1-105">As funções da caixa de diálogo a seguir adicionam botões à caixa de diálogo **Propriedades** do Gerenciador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c67c1-105">The following dialog box functions add buttons to the File Manager **Properties** dialog box.</span></span> <span data-ttu-id="c67c1-106">Em seguida, o provedor pode manipular os eventos desses botões para executar tarefas específicas da rede.</span><span class="sxs-lookup"><span data-stu-id="c67c1-106">The provider can then handle the events of those buttons to perform network-specific tasks.</span></span> <span data-ttu-id="c67c1-107">Observe que há um limite para o número de botões que podem ser adicionados.</span><span class="sxs-lookup"><span data-stu-id="c67c1-107">Note that there is a limit to the number of buttons that can be added.</span></span> <span data-ttu-id="c67c1-108">Por isso, os provedores devem usar essa funcionalidade com moderação.</span><span class="sxs-lookup"><span data-stu-id="c67c1-108">Because of this, providers should use this capability sparingly.</span></span> <span data-ttu-id="c67c1-109">Além disso, um provedor pode não conseguir adicionar um botão porque o espaço disponível já foi usado por outros provedores.</span><span class="sxs-lookup"><span data-stu-id="c67c1-109">Also, a provider may find itself unable to add a button because the available space has been used already by other providers.</span></span> <span data-ttu-id="c67c1-110">Um provedor de rede deve lidar com essa situação.</span><span class="sxs-lookup"><span data-stu-id="c67c1-110">A network provider should handle this situation.</span></span>



| <span data-ttu-id="c67c1-111">Função</span><span class="sxs-lookup"><span data-stu-id="c67c1-111">Function</span></span>                                           | <span data-ttu-id="c67c1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c67c1-112">Description</span></span>                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c67c1-113">**NPGetPropertyText**</span><span class="sxs-lookup"><span data-stu-id="c67c1-113">**NPGetPropertyText**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | <span data-ttu-id="c67c1-114">Determina os nomes dos botões adicionados a uma caixa de diálogo de propriedade para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="c67c1-114">Determines the names of buttons added to a property dialog box for a specific resource.</span></span><br/>                                      |
| [<span data-ttu-id="c67c1-115">**NPPropertyDialog**</span><span class="sxs-lookup"><span data-stu-id="c67c1-115">**NPPropertyDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | <span data-ttu-id="c67c1-116">Chamado quando um usuário clica em um botão adicionado usando a função [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .</span><span class="sxs-lookup"><span data-stu-id="c67c1-116">Called when a user clicks a button added by using the [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) function.</span></span><br/>               |
| [<span data-ttu-id="c67c1-117">**NPSearchDialog**</span><span class="sxs-lookup"><span data-stu-id="c67c1-117">**NPSearchDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | <span data-ttu-id="c67c1-118">Permite que os provedores de rede implementem sua própria funcionalidade de pesquisa além da fornecida na caixa de diálogo de **conexão** .</span><span class="sxs-lookup"><span data-stu-id="c67c1-118">Enables network providers to implement their own search functionality beyond that provided in the **Connection** dialog box.</span></span><br/> |
| [<span data-ttu-id="c67c1-119">**NPFormatNetworkName**</span><span class="sxs-lookup"><span data-stu-id="c67c1-119">**NPFormatNetworkName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | <span data-ttu-id="c67c1-120">Permite que os provedores de rede formatem ou modifiquem nomes de rede antes de serem apresentados ao usuário.</span><span class="sxs-lookup"><span data-stu-id="c67c1-120">Enables network providers to format or otherwise modify network names before they are presented to the user.</span></span><br/>                 |



 

 

 




