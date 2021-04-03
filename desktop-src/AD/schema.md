---
title: Esquema (AD DS)
description: Active Directory esquema é implementado como um conjunto de instâncias de classe de objeto armazenadas no diretório.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory de esquema de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "103639030"
---
# <a name="schema-ad-ds"></a><span data-ttu-id="ce290-104">Esquema (AD DS)</span><span class="sxs-lookup"><span data-stu-id="ce290-104">Schema (AD DS)</span></span>

<span data-ttu-id="ce290-105">Active Directory esquema é implementado como um conjunto de instâncias de classe de objeto armazenadas no diretório.</span><span class="sxs-lookup"><span data-stu-id="ce290-105">Active Directory schema is implemented as a set of object class instances stored in the directory.</span></span> <span data-ttu-id="ce290-106">Isso é muito diferente de muitos diretórios que têm um esquema, mas os armazenam como um arquivo de texto lido na inicialização.</span><span class="sxs-lookup"><span data-stu-id="ce290-106">This is very different than many directories that have a schema but store it as a text file read at startup.</span></span> <span data-ttu-id="ce290-107">O armazenamento do esquema no diretório tem muitas vantagens.</span><span class="sxs-lookup"><span data-stu-id="ce290-107">Storing the schema in the directory has many advantages.</span></span> <span data-ttu-id="ce290-108">Por exemplo, os aplicativos de usuário podem lê-lo para descobrir quais objetos e propriedades estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ce290-108">For example, user applications can read it to discover what objects and properties are available.</span></span>

<span data-ttu-id="ce290-109">Active Directory esquema pode ser atualizado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="ce290-109">Active Directory schema can be updated dynamically.</span></span> <span data-ttu-id="ce290-110">Ou seja, um aplicativo pode estender o esquema com novos atributos e classes e usar as extensões imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ce290-110">That is, an application can extend the schema with new attributes and classes and use the extensions immediately.</span></span> <span data-ttu-id="ce290-111">As atualizações de esquema são realizadas criando ou modificando os objetos de esquema armazenados no diretório.</span><span class="sxs-lookup"><span data-stu-id="ce290-111">Schema updates are accomplished by creating or modifying the schema objects stored in the directory.</span></span> <span data-ttu-id="ce290-112">Como todos os objetos em Active Directory, ACLs (listas de controle de acesso) protegem objetos de esquema, para que os usuários autorizados só possam alterar o esquema.</span><span class="sxs-lookup"><span data-stu-id="ce290-112">Like every object in Active Directory, access-control lists (ACLs) protect schema objects, so authorized users only may alter the schema.</span></span>

<span data-ttu-id="ce290-113">Para obter mais informações, consulte [Active Directory esquema](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="ce290-113">For more information, see [Active Directory Schema](active-directory-schema.md).</span></span>

 

 




