---
title: Modificando as interfaces de usuário existentes
description: O painel de resultados do snap-in Active Directory usuários e computadores do MMC exibe várias colunas de dados de atributo para objetos dentro de um contêiner, como os atributos Name e Description.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modificando o AD de interfaces de usuário existentes
- Snap-in de usuários e computadores AD, modificando a exibição
- Snap-in de usuários e computadores AD, adicionando colunas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822263"
---
# <a name="modifying-existing-user-interfaces"></a><span data-ttu-id="dbf46-106">Modificando as interfaces de usuário existentes</span><span class="sxs-lookup"><span data-stu-id="dbf46-106">Modifying Existing User Interfaces</span></span>

<span data-ttu-id="dbf46-107">O painel de resultados do snap-in Active Directory usuários e computadores do MMC exibe várias colunas de dados de atributo para objetos dentro de um contêiner, como os atributos **Name** e **Description** .</span><span class="sxs-lookup"><span data-stu-id="dbf46-107">The results pane of the Active Directory Users and Computers MMC snap-in displays several columns of attribute data for objects within a container, such as the **Name** and **Description** attributes.</span></span> <span data-ttu-id="dbf46-108">O snap-in permite que o usuário adicione e remova as colunas exibidas no painel de resultados do snap-in do.</span><span class="sxs-lookup"><span data-stu-id="dbf46-108">The snap-in enables the user to add and remove the columns displayed in the results pane of the snap-in.</span></span>

<span data-ttu-id="dbf46-109">Para alterar a exibição, o usuário usa o menu suspenso **Exibir** e seleciona **Adicionar/remover colunas**.</span><span class="sxs-lookup"><span data-stu-id="dbf46-109">To change the display, the user uses the **View** pull-down menu and selects **Add/Remove Columns**.</span></span> <span data-ttu-id="dbf46-110">Na caixa de diálogo **Adicionar/remover colunas** , há uma lista de colunas que o usuário pode escolher para exibir no painel de resultados.</span><span class="sxs-lookup"><span data-stu-id="dbf46-110">In the **Add/Remove Columns** dialog box, there is a list of columns that the user can choose from to display in the results pane.</span></span>

<span data-ttu-id="dbf46-111">O snap-in Active Directory usuários e computadores do MMC que está incluído no Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition e Windows Server 2003, Datacenter Edition, fornece a capacidade de modificar a lista de colunas que podem ser exibidas no painel de resultados do snap-in para um contêiner.</span><span class="sxs-lookup"><span data-stu-id="dbf46-111">The Active Directory Users and Computers MMC snap-in that is included with Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition, provides the ability to modify the list of columns that can be displayed in the results pane of the snap-in for a container.</span></span> <span data-ttu-id="dbf46-112">Esse recurso só existe se o snap-in for direcionado a uma floresta com o esquema do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dbf46-112">This feature only exists if the snap-in is targeted at a forest with Windows Server 2003 schema.</span></span>

<span data-ttu-id="dbf46-113">Para adicionar uma coluna à lista, adicione um valor ao atributo **extraColumns** do especificador de exibição para o tipo de objeto ao qual o atributo está associado.</span><span class="sxs-lookup"><span data-stu-id="dbf46-113">To add a column to the list, add a value to the **extraColumns** attribute of the display specifier for the object type that the attribute is associated with.</span></span> <span data-ttu-id="dbf46-114">O atributo **extraColumns** é um atributo de cadeia de caracteres com valores múltiplos, em que cada cadeia de caracteres está no formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="dbf46-114">The **extraColumns** attribute is a multi-valued string attribute where each string is in the following format.</span></span>


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



<span data-ttu-id="dbf46-115">A tabela a seguir lista o conteúdo desses valores.</span><span class="sxs-lookup"><span data-stu-id="dbf46-115">The following table lists the contents of these values.</span></span>



| <span data-ttu-id="dbf46-116">Valor</span><span class="sxs-lookup"><span data-stu-id="dbf46-116">Value</span></span>                        | <span data-ttu-id="dbf46-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbf46-117">Description</span></span>                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf46-118">" &lt; ldapDisplayName &gt; "</span><span class="sxs-lookup"><span data-stu-id="dbf46-118">"&lt;ldapdisplayname&gt;"</span></span>    | <span data-ttu-id="dbf46-119">Contém uma cadeia de caracteres que representa o **ldapDisplayName** do atributo.</span><span class="sxs-lookup"><span data-stu-id="dbf46-119">Contains a string that represents the **ldapDisplayName** of the attribute.</span></span>                                                         |
| <span data-ttu-id="dbf46-120">" &lt; cabeçalho da coluna &gt; "</span><span class="sxs-lookup"><span data-stu-id="dbf46-120">"&lt;column header&gt;"</span></span>      | <span data-ttu-id="dbf46-121">Contém uma cadeia de caracteres que representa o texto exibido no cabeçalho da coluna.</span><span class="sxs-lookup"><span data-stu-id="dbf46-121">Contains a string that represents the text displayed in the header for the column.</span></span>                                                  |
| <span data-ttu-id="dbf46-122">" &lt; visibilidade padrão &gt; "</span><span class="sxs-lookup"><span data-stu-id="dbf46-122">"&lt;default visibility&gt;"</span></span> | <span data-ttu-id="dbf46-123">Contém um valor numérico que será 0 se o atributo estiver oculto por padrão ou 1 se o atributo estiver visível por padrão.</span><span class="sxs-lookup"><span data-stu-id="dbf46-123">Contains a numeric value that is 0 if the attribute is hidden by default or 1 if the attribute is visible by default.</span></span>               |
| <span data-ttu-id="dbf46-124">" &lt; largura &gt; "</span><span class="sxs-lookup"><span data-stu-id="dbf46-124">"&lt;width&gt;"</span></span>              | <span data-ttu-id="dbf46-125">Contém a largura da coluna, em pixels.</span><span class="sxs-lookup"><span data-stu-id="dbf46-125">Contains the width of the column, in pixels.</span></span> <span data-ttu-id="dbf46-126">Se esse valor for-1, a largura da coluna será definida com a largura do cabeçalho da coluna.</span><span class="sxs-lookup"><span data-stu-id="dbf46-126">If this value is -1, the width of the column is set to the width of the column header.</span></span> |
| <span data-ttu-id="dbf46-127">" &lt; não utilizado &gt; "</span><span class="sxs-lookup"><span data-stu-id="dbf46-127">"&lt;unused&gt;"</span></span>             | <span data-ttu-id="dbf46-128">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="dbf46-128">Unused.</span></span> <span data-ttu-id="dbf46-129">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dbf46-129">Must be zero.</span></span>                                                                                                               |



 

<span data-ttu-id="dbf46-130">Por exemplo, para adicionar uma coluna que exibirá o nome canônico de objetos em uma unidade organizacional, um valor para o atributo **canôniconame** será adicionado ao atributo **extraColumns** do objeto de **exibição OrganizationalUnit** no contêiner exibir especificadores.</span><span class="sxs-lookup"><span data-stu-id="dbf46-130">For example, to add a column that will display the canonical name for objects in an organizational unit, a value for the **canonicalName** attribute is added to the **extraColumns** attribute of the **organizationalUnit-Display** object in the display specifiers container.</span></span> <span data-ttu-id="dbf46-131">A cadeia de caracteres adicionada ao atributo **extraColumns** do objeto de **exibição OrganizationalUnit** será semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="dbf46-131">The string added to the **extraColumns** attribute of the **organizationalUnit-Display** object will look like the following.</span></span>


```C++
canonicalName,Canonical Name,0,150,0
```



<span data-ttu-id="dbf46-132">A caixa de diálogo **Adicionar/remover colunas** exibe somente as colunas contidas no atributo **ExtraColumns** do objeto **displaySpecifier** do tipo de contêiner que está sendo exibido.</span><span class="sxs-lookup"><span data-stu-id="dbf46-132">The **Add/Remove Columns** dialog box displays only the columns that are contained in the **extraColumns** attribute of the **displaySpecifier** object of the container type that is being displayed.</span></span> <span data-ttu-id="dbf46-133">Se o atributo **extraColumns** não contiver nenhum valor, a caixa de diálogo **Adicionar/remover colunas** exibirá um conjunto fixo de colunas.</span><span class="sxs-lookup"><span data-stu-id="dbf46-133">If the **extraColumns** attribute does not contain any values, the **Add/Remove Columns** dialog box will display a fixed set of columns.</span></span> <span data-ttu-id="dbf46-134">Uma cópia do conjunto fixo de colunas está contida no atributo **extraColumns** do objeto de **exibição padrão** .</span><span class="sxs-lookup"><span data-stu-id="dbf46-134">A copy of the fixed set of columns is contained in the **extraColumns** attribute of the **default-Display** object.</span></span>

<span data-ttu-id="dbf46-135">Para adicionar uma ou mais colunas à lista de colunas de um objeto específico, você deve copiar todos os valores de **extraColumns** do objeto de **exibição padrão** para o objeto de destino e, em seguida, adicionar as colunas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="dbf46-135">To add one or more columns to the list of columns for a specific object, you must copy all of the **extraColumns** values from the **default-Display** object to the target object and then add the custom columns.</span></span> <span data-ttu-id="dbf46-136">Se você especificar o atributo **extraColumns** em uma determinada classe, essa classe usará essas colunas e não as mesclará com as colunas especificadas na classe de **exibição padrão** .</span><span class="sxs-lookup"><span data-stu-id="dbf46-136">If you specify the **extraColumns** attribute on a given class, then that class will use those columns and will not merge them with the columns that are specified in the **default-Display** class.</span></span> <span data-ttu-id="dbf46-137">Portanto, outras alterações na classe de **exibição padrão** não terão nenhum efeito sobre esse objeto.</span><span class="sxs-lookup"><span data-stu-id="dbf46-137">Therefore, further changes to the **default-Display** class will have no effect on that object.</span></span>

<span data-ttu-id="dbf46-138">Para exibir uma coluna personalizada para todos os tipos de contêiner que não têm nenhuma coluna personalizada registrada, adicione um valor para a coluna ao atributo **extraColumns** do objeto de **exibição padrão** .</span><span class="sxs-lookup"><span data-stu-id="dbf46-138">To display a custom column for all container types that do not have any custom columns registered, add a value for the column to the **extraColumns** attribute of the **default-Display** object.</span></span>

 

 




