---
title: Integrando extensões de esquema com a interface do usuário
description: As ferramentas de administração do Active Directory Domain Services usam uma arquitetura comum para conectar a interface do usuário administrativo ao esquema de diretório.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105749125"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a><span data-ttu-id="ff5c0-103">Integrando extensões de esquema com a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="ff5c0-103">Integrating Schema Extensions with the User Interface</span></span>

<span data-ttu-id="ff5c0-104">As ferramentas de administração do Active Directory Domain Services usam uma arquitetura comum para conectar a interface do usuário administrativo ao esquema de diretório.</span><span class="sxs-lookup"><span data-stu-id="ff5c0-104">The administration tools of Active Directory Domain Services use a common architecture for connecting the administrative user interface to the directory schema.</span></span> <span data-ttu-id="ff5c0-105">O ponto central dessa arquitetura é a classe de objeto **displaySpecifier** .</span><span class="sxs-lookup"><span data-stu-id="ff5c0-105">The centerpiece of this architecture is the **displaySpecifier** object class.</span></span> <span data-ttu-id="ff5c0-106">Os especificadores de exibição e seu uso são descritos em detalhes na [extensão da interface do usuário para objetos de diretório](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ff5c0-106">Display specifiers and their usage are described in detail in [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

<span data-ttu-id="ff5c0-107">Ao criar uma nova classe por meio da subclasse de uma classe existente, você pode aproveitar a interface do usuário existente para a superclasse copiando o especificador de exibição da superclasse.</span><span class="sxs-lookup"><span data-stu-id="ff5c0-107">When you create a new class by subclassing an existing class, you can leverage the existing UI for the superclass by copying the superclass' display specifier.</span></span> <span data-ttu-id="ff5c0-108">Uma maneira fácil de copiar o especificador de exibição para uma classe é exportá-lo para um arquivo LDIF usando LDIFDE, editar o nome e CN distintos e, em seguida, importar o arquivo LDIF modificado.</span><span class="sxs-lookup"><span data-stu-id="ff5c0-108">An easy way to copy the display specifier for a class is to export it into an LDIF file using LDIFDE, edit the Distinguished name and CN, then import the modified LDIF file.</span></span> <span data-ttu-id="ff5c0-109">Se a subclasse tiver atributos adicionais, será necessário fornecer páginas de propriedades adicionais para dar suporte à edição.</span><span class="sxs-lookup"><span data-stu-id="ff5c0-109">If the subclass has additional attributes, you will need to provide additional property pages to support editing.</span></span> <span data-ttu-id="ff5c0-110">Se a subclasse tiver propriedades adicionais necessárias, você precisará fornecer páginas de extensão da caixa de diálogo de criação, pois a interface do usuário fornecida pela superclasse não tem como criar esses novos atributos.</span><span class="sxs-lookup"><span data-stu-id="ff5c0-110">If the subclass has additional must-have properties, you will need to provide Creation Dialog extension pages since the UI provided by the superclass has no way to create these new attributes.</span></span>

 

 




