---
title: Como estender o esquema
description: Quando as classes e/ou atributos existentes não se ajustarem ao tipo de dados que você deseja armazenar, talvez você queira estender o esquema.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- AD Schema, como estender
- Active Directory, usando, esquema
- Active Directory, usando, esquema, estendendo o esquema, como estender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640398"
---
# <a name="how-to-extend-the-schema"></a><span data-ttu-id="0f12a-106">Como estender o esquema</span><span class="sxs-lookup"><span data-stu-id="0f12a-106">How to Extend the Schema</span></span>

<span data-ttu-id="0f12a-107">Quando as classes e/ou atributos existentes não se ajustarem ao tipo de dados que você deseja armazenar, talvez você queira estender o esquema.</span><span class="sxs-lookup"><span data-stu-id="0f12a-107">When the existing classes and/or attributes do not fit with the type of data that you want to store, you might want to extend the schema.</span></span> <span data-ttu-id="0f12a-108">Para obter mais informações sobre como decidir quando estender o esquema, consulte [estendendo o esquema](extending-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="0f12a-108">For more information on deciding when to extend the schema, see [Extending the Schema](extending-the-schema.md).</span></span> <span data-ttu-id="0f12a-109">Quando você tiver decidido que a extensão do esquema é necessária, use o procedimento a seguir para estender o esquema.</span><span class="sxs-lookup"><span data-stu-id="0f12a-109">When you have decided that schema extension is required, use the following procedure to extend the schema.</span></span>

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a><span data-ttu-id="0f12a-110">Verifique Active Directory funcionalidade antes de aplicar as extensões de esquema</span><span class="sxs-lookup"><span data-stu-id="0f12a-110">Verify Active Directory functionality before you apply any schema extensions</span></span>

<span data-ttu-id="0f12a-111">Verifique Active Directory funcionalidade antes de atualizar o esquema para ajudar a garantir que a extensão do esquema continue sem erros.</span><span class="sxs-lookup"><span data-stu-id="0f12a-111">Verify Active Directory functionality before you update the schema to help ensure that the schema extension proceeds without error.</span></span> <span data-ttu-id="0f12a-112">No mínimo, verifique se todos os controladores de domínio da floresta estão online e executando a replicação de entrada.</span><span class="sxs-lookup"><span data-stu-id="0f12a-112">At a minimum, ensure that all domain controllers for the forest are online and performing inbound replication.</span></span>

<span data-ttu-id="0f12a-113">**Para verificar Active Directory funcionalidade antes de aplicar a extensão do esquema**</span><span class="sxs-lookup"><span data-stu-id="0f12a-113">**To verify Active Directory functionality before you apply the schema extension**</span></span>

1.  <span data-ttu-id="0f12a-114">Faça logon em uma estação de trabalho administrativa que tenha a ferramenta de suporte do Windows Repadmin.exe instalada.</span><span class="sxs-lookup"><span data-stu-id="0f12a-114">Log on to an administrative workstation that has the Windows Support Tool Repadmin.exe installed.</span></span>
    > [!Note]  
    > <span data-ttu-id="0f12a-115">As ferramentas de suporte estão localizadas na mídia de instalação do sistema operacional na \\ pasta ferramentas de suporte.</span><span class="sxs-lookup"><span data-stu-id="0f12a-115">The Support Tools are located on the operating system installation media in the Support\\Tools folder.</span></span>

     

2.  <span data-ttu-id="0f12a-116">Abra um prompt de comando e, em seguida, altere os diretórios para a pasta na qual as ferramentas de suporte do Windows estão instaladas.</span><span class="sxs-lookup"><span data-stu-id="0f12a-116">Open a command prompt, and then change directories to the folder in which the Windows Support Tools are installed.</span></span>
3.  <span data-ttu-id="0f12a-117">Em um prompt de comando, digite o seguinte e pressione ENTER:</span><span class="sxs-lookup"><span data-stu-id="0f12a-117">At a command prompt, type the following, and then press ENTER:</span></span>

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    <span data-ttu-id="0f12a-118">Todos os controladores de domínio devem mostrar 0 na coluna falha e os maiores deltas (que indicam o número de alterações feitas no banco de dados de Active Directory desde a última replicação bem-sucedida) devem ser menores ou aproximadamente iguais à frequência de replicação do link de site usado pelo controlador de domínio para replicação.</span><span class="sxs-lookup"><span data-stu-id="0f12a-118">All domain controllers should show 0 in the Fails column, and the largest deltas (which indicate the number of changes that have been made to the Active Directory database since the last successful replication) should be less than or roughly equal to the replication frequency of the site link that is used by the domain controller for replication.</span></span> <span data-ttu-id="0f12a-119">A frequência de replicação padrão é 180 minutos.</span><span class="sxs-lookup"><span data-stu-id="0f12a-119">The default replication frequency is 180 minutes.</span></span>

    <span data-ttu-id="0f12a-120">Para obter mais informações sobre as etapas adicionais que você pode executar para verificar Active Directory funcionalidade antes de aplicar a extensão do esquema, consulte o [artigo 325379 na base de dados de conhecimento Microsoft](https://support.microsoft.com/kb/325379/en-us).</span><span class="sxs-lookup"><span data-stu-id="0f12a-120">For more information about additional steps that you can take to verify Active Directory functionality before you apply the schema extension, see [article 325379 in the Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span></span>

<span data-ttu-id="0f12a-121">**Para estender o esquema**</span><span class="sxs-lookup"><span data-stu-id="0f12a-121">**To Extend the Schema**</span></span>

1.  <span data-ttu-id="0f12a-122">Determine o método de extensão.</span><span class="sxs-lookup"><span data-stu-id="0f12a-122">Determine the method of extension.</span></span> <span data-ttu-id="0f12a-123">Depois de criar cuidadosamente as alterações de esquema, a próxima etapa é decidir qual método usar para estender o esquema.</span><span class="sxs-lookup"><span data-stu-id="0f12a-123">Once you have carefully designed your schema changes, the next step is to decide which method to use to extend the schema.</span></span> <span data-ttu-id="0f12a-124">É possível usar um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="0f12a-124">You can use one of the following methods:</span></span>
    -   <span data-ttu-id="0f12a-125">Manualmente, usando arquivos de importação.</span><span class="sxs-lookup"><span data-stu-id="0f12a-125">Manually, using import files.</span></span> <span data-ttu-id="0f12a-126">Consulte a documentação [usando a ferramenta Ldifde](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="0f12a-126">See the documentation [Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span></span>
        > [!Note]  
        > <span data-ttu-id="0f12a-127">Não use o LDIFDE para importar \* arquivos. ldf do Windows SCH.</span><span class="sxs-lookup"><span data-stu-id="0f12a-127">Do not use LDIFDE to import Windows Sch\*.ldf files.</span></span> <span data-ttu-id="0f12a-128">Esses arquivos são necessários para estender o esquema de Active Directory a fim de instalar controladores de domínio que executam uma versão mais recente do Windows Server do que a versão em execução no mestre de esquema atual.</span><span class="sxs-lookup"><span data-stu-id="0f12a-128">Those files are required to extend the Active Directory schema in order to install domain controllers that run a newer version of Windows Server than the version that is running on the current schema master.</span></span> <span data-ttu-id="0f12a-129">Quando você precisar estender o esquema para instalar um novo controlador de domínio, use Adprep.exe.</span><span class="sxs-lookup"><span data-stu-id="0f12a-129">When you need to extend the schema in order to install a new domain controller, use Adprep.exe.</span></span>

         

    -   <span data-ttu-id="0f12a-130">Programaticamente, usando um programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="0f12a-130">Programmatically, using an installation program.</span></span> <span data-ttu-id="0f12a-131">Para obter mais informações, consulte [extensão programática](programmatic-extension.md)</span><span class="sxs-lookup"><span data-stu-id="0f12a-131">For more information, see [Programmatic Extension](programmatic-extension.md)</span></span>
2.  <span data-ttu-id="0f12a-132">Habilitar alterações de esquema.</span><span class="sxs-lookup"><span data-stu-id="0f12a-132">Enable Schema Changes.</span></span> <span data-ttu-id="0f12a-133">Para obter mais informações, consulte [pré-requisitos para instalar uma extensão de esquema](prerequisites-for-installing-a-schema-extension.md) e [habilitar alterações de esquema no mestre de esquema](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="0f12a-133">For more information, see [Prerequisites for Installing a Schema Extension](prerequisites-for-installing-a-schema-extension.md) and [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
3.  <span data-ttu-id="0f12a-134">Obtenha um OID (identificador de objeto) para seus novos atributos e/ou classes, conforme descrito em [obtendo um identificador de objeto](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="0f12a-134">Obtain an Object Identifier (OID) for your new attributes and/or classes, as described in [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
4.  <span data-ttu-id="0f12a-135">Crie novos atributos e classes.</span><span class="sxs-lookup"><span data-stu-id="0f12a-135">Create new attributes and classes.</span></span>
5.  <span data-ttu-id="0f12a-136">Use especificadores de exibição para integrar novos atributos e classes com a interface do usuário, se necessário.</span><span class="sxs-lookup"><span data-stu-id="0f12a-136">Use display specifiers to integrate new attributes and classes with the user interface, if necessary.</span></span>
6.  <span data-ttu-id="0f12a-137">Atualize o cache de esquema conforme descrito em [atualizando o cache de esquema](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="0f12a-137">Update the schema cache as described in [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
7.  <span data-ttu-id="0f12a-138">Verifique a extensão do esquema usando LDP.exe.</span><span class="sxs-lookup"><span data-stu-id="0f12a-138">Verify the schema extension using LDP.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f12a-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f12a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f12a-140">Obtendo um identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="0f12a-140">Obtaining an Object Identifier</span></span>](obtaining-an-object-identifier.md)
</dt> <dt>

[<span data-ttu-id="0f12a-141">As novas ferramentas de linha de comando para Active Directory no Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f12a-141">The new command-line tools for Active Directory in Windows Server 2003</span></span>](https://support.microsoft.com/kb/298882)
</dt> <dt>

<span data-ttu-id="0f12a-142">[Usando a ferramenta LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span><span class="sxs-lookup"><span data-stu-id="0f12a-142">[Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span></span>
</dt> <dt>

<span data-ttu-id="0f12a-143">[Estendendo o esquema de Active Directory](/previous-versions/ms806972(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="0f12a-143">[Extending the Active Directory Schema](/previous-versions/ms806972(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="0f12a-144">Restrições na extensão do esquema</span><span class="sxs-lookup"><span data-stu-id="0f12a-144">Restrictions on Schema Extension</span></span>](restrictions-on-schema-extension.md)
</dt> </dl>

 

 