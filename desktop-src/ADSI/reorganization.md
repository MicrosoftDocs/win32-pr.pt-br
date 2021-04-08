---
title: Reorganização
description: A organização de vendas mudou para uma nova organização \ 8212; \ 0034; Vendas e suporte. \ 0034; Julie Bankert foi promovido para Vice-Presidente e conduzirá a nova organização.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- ADSI de reorganização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004863"
---
# <a name="reorganization"></a><span data-ttu-id="5866b-105">Reorganização</span><span class="sxs-lookup"><span data-stu-id="5866b-105">Reorganization</span></span>

<span data-ttu-id="5866b-106">A organização de vendas mudou para uma nova organização: "vendas e suporte".</span><span class="sxs-lookup"><span data-stu-id="5866b-106">The sales organization has moved to a new organization — "Sales and Support."</span></span> <span data-ttu-id="5866b-107">Julie Bankert foi promovido para Vice-Presidente e conduzirá a nova organização.</span><span class="sxs-lookup"><span data-stu-id="5866b-107">Julie Bankert has been promoted to vice president and will lead the new organization.</span></span> <span data-ttu-id="5866b-108">Joe Worden, administrador corporativo, deve mover a UO de vendas para uma nova UO, vendas e suporte.</span><span class="sxs-lookup"><span data-stu-id="5866b-108">Joe Worden, the enterprise administrator, must move Sales OU to a new OU, Sales and Support.</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



<span data-ttu-id="5866b-109">Com este exemplo de código, todos os objetos na unidade organizacional Sales, incluindo as unidades de suborganização, são movidos para a nova unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="5866b-109">With this code example, all objects in the sales organizational unit, including the sub-organizational units, are moved to the new organizational unit.</span></span>

<span data-ttu-id="5866b-110">Agora, Joe pode mover Julie para a unidade organizacional Sales and Support.</span><span class="sxs-lookup"><span data-stu-id="5866b-110">Now, Joe can move Julie into the Sales and Support organizational unit.</span></span>


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



<span data-ttu-id="5866b-111">Lembre-se de que o link de relatório direto de gerente entre Julie Bankert e Chris Gray é atualizado automaticamente pelo Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5866b-111">Be aware that the manager-direct report link between Julie Bankert and Chris Gray is automatically updated by Active Directory.</span></span>

<span data-ttu-id="5866b-112">**Para criar um relatório de Active Directory**</span><span class="sxs-lookup"><span data-stu-id="5866b-112">**To create an Active Directory report**</span></span>

1.  <span data-ttu-id="5866b-113">Abra Visual Basic versão 6,0 e, quando solicitado, insira o tipo de projeto, selecione **projeto de dados**.</span><span class="sxs-lookup"><span data-stu-id="5866b-113">Open Visual Basic version 6.0, and when prompted for the project type, select **Data Project**.</span></span>
2.  <span data-ttu-id="5866b-114">Em **projeto de dados**, clique duas vezes em **Data Environment1**.</span><span class="sxs-lookup"><span data-stu-id="5866b-114">On **Data Project**, double-click **Data Environment1**.</span></span>
3.  <span data-ttu-id="5866b-115">Na janela **ambiente de dados** , clique com o botão direito do mouse no objeto de conexão **(Connection1)** e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="5866b-115">On the **Data Environment** window, right-click the connection object **(Connection1)** and select **Properties**.</span></span>
4.  <span data-ttu-id="5866b-116">Selecione **provedor de OLE DB para serviços de diretório da Microsoft** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="5866b-116">Select **OLE DB Provider for Microsoft Directory Services**, and click **Next**.</span></span>
5.  <span data-ttu-id="5866b-117">Selecione **usar segurança integrada do Windows NT** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="5866b-117">Select **Use Windows NT Integrated security**, and click **OK**.</span></span> <span data-ttu-id="5866b-118">Isso cria um objeto de conexão.</span><span class="sxs-lookup"><span data-stu-id="5866b-118">This creates a connection object.</span></span>
6.  <span data-ttu-id="5866b-119">Clique com o botão direito do mouse na janela **ambiente de dados** novamente para selecionar **Adicionar comando**.</span><span class="sxs-lookup"><span data-stu-id="5866b-119">Right-click the **Data Environment** window again to select **Add Command**.</span></span> <span data-ttu-id="5866b-120">Clique com o botão direito do mouse no objeto **Command1** e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="5866b-120">Right-click the **Command1** object and select **Properties**.</span></span> <span data-ttu-id="5866b-121">A caixa de diálogo **Command1 Properties** a seguir será exibida.</span><span class="sxs-lookup"><span data-stu-id="5866b-121">The following **Command1 Properties** dialog box will appear.</span></span>

    ![caixa de diálogo Propriedades do Command1](images/adadsi3.png)

7.  <span data-ttu-id="5866b-123">Clique no botão de opção **instrução SQL** e digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5866b-123">Click the **SQL Statement** option button and type the following:</span></span>

    <span data-ttu-id="5866b-124">Selecione o nome, telephoneNumber de ' LDAP://DC = Fabrikam, DC = com ' em que objectCategory = ' Person ' e objectClass = ' user '</span><span class="sxs-lookup"><span data-stu-id="5866b-124">SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'</span></span>

    <span data-ttu-id="5866b-125">O objeto de **comando** é criado.</span><span class="sxs-lookup"><span data-stu-id="5866b-125">The **Command** object is created.</span></span> <span data-ttu-id="5866b-126">Adicione o objeto de **comando** ao relatório.</span><span class="sxs-lookup"><span data-stu-id="5866b-126">Add the **Command** object to the report.</span></span>

8.  <span data-ttu-id="5866b-127">Clique duas vezes em **Data Report1** na janela do **projeto** .</span><span class="sxs-lookup"><span data-stu-id="5866b-127">Double-click **Data Report1** from the **Project** window.</span></span>
9.  <span data-ttu-id="5866b-128">Arraste o objeto **Command1** da janela **DataEnvironment1** para a seção **detalhes** na janela **relatório de dados** .</span><span class="sxs-lookup"><span data-stu-id="5866b-128">Drag the **Command1** object from the **DataEnvironment1** window to the **Detail** section in the **Data Report** window.</span></span>
10. <span data-ttu-id="5866b-129">Em **Propriedades de DataReport1**, para **DataSource**, selecione **DataEnvironment1** no menu suspenso e selecione **Command1** no campo **DataMember** .</span><span class="sxs-lookup"><span data-stu-id="5866b-129">On **DataReport1 Properties**, for **DataSource**, select **DataEnvironment1** from the pull-down menu, and select **Command1** in the **DataMember** field.</span></span>
11. <span data-ttu-id="5866b-130">Na janela do projeto, clique com o botão direito do mouse em **projeto de dados** e selecione **Propriedades do dataproject**.</span><span class="sxs-lookup"><span data-stu-id="5866b-130">On the project window, right-click **Data Project**, and select **DataProject Properties**.</span></span>
12. <span data-ttu-id="5866b-131">Na janela de diálogo **dataproject – Project Properties** , em **Startup object**, selecione **DataReport1** no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="5866b-131">On the **DataProject - Project Properties** dialog window, under **Startup Object**, select **DataReport1** from the pull-down menu.</span></span> <span data-ttu-id="5866b-132">Clique em **OK** para salvar.</span><span class="sxs-lookup"><span data-stu-id="5866b-132">Click **OK** to save.</span></span>
13. <span data-ttu-id="5866b-133">Compilar.</span><span class="sxs-lookup"><span data-stu-id="5866b-133">Compile.</span></span> <span data-ttu-id="5866b-134">A caixa de diálogo **DataReport1** a seguir será exibida.</span><span class="sxs-lookup"><span data-stu-id="5866b-134">The following **DataReport1** dialog box will appear.</span></span>

    ![caixa de diálogo datareport1](images/adadsi4.png)

## <a name="related-topics"></a><span data-ttu-id="5866b-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5866b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5866b-137">Unindo dados heterogêneos</span><span class="sxs-lookup"><span data-stu-id="5866b-137">Joining Heterogeneous Data</span></span>](joining-heterogeneous-data.md)
</dt> </dl>

 

 




