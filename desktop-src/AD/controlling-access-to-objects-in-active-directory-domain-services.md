---
title: Controlando o acesso a objetos no Active Directory Domain Services
description: Cada objeto de serviço de diretório Active Directory é protegido pela segurança do Windows 2000.
ms.assetid: 0821069d-76bd-49cb-a617-8446d26e61d9
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, usando, segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cac744ef63fa95c45d5af535f5155378d479fdb
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/04/2019
ms.locfileid: "104006964"
---
# <a name="controlling-object-access-in-active-directory-domain-services"></a><span data-ttu-id="3ba25-104">Controlando o acesso a objetos no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="3ba25-104">Controlling object access in Active Directory Domain Services</span></span>

<span data-ttu-id="3ba25-105">Cada objeto de serviço de diretório Active Directory é protegido pela segurança do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3ba25-105">Each Active Directory directory service object is protected by Windows 2000 security.</span></span> <span data-ttu-id="3ba25-106">Essa proteção de segurança controla as operações que cada entidade de segurança pode executar no diretório.</span><span class="sxs-lookup"><span data-stu-id="3ba25-106">This security protection controls the operations that each security principal can perform in the directory.</span></span> <span data-ttu-id="3ba25-107">As seções a seguir descrevem como um aplicativo habilitado para diretório pode usar os recursos de controle de acesso no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3ba25-107">The following sections describe how a directory-enabled application can use the access control features in Active Directory.</span></span>

-   [<span data-ttu-id="3ba25-108">Como o controle de acesso funciona no Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="3ba25-108">How Access Control Works in Active Directory Domain Services</span></span>](how-access-control-works-in-active-directory-domain-services.md)
-   [<span data-ttu-id="3ba25-109">Como o controle de acesso afeta as operações de leitura, a operação de gravação, a criação e a exclusão de objetos.</span><span class="sxs-lookup"><span data-stu-id="3ba25-109">How access control affects read operations, write operation, object creation and deletion.</span></span>](how-security-affects-operations-in-active-directory-domain-services.md)
-   [<span data-ttu-id="3ba25-110">Usando as interfaces IADs e IDirectoryObject para trabalhar com um descritor de segurança de um objeto</span><span class="sxs-lookup"><span data-stu-id="3ba25-110">Using the IADs and IDirectoryObject interfaces to work with an object's security descriptor</span></span>](apis-for-working-with-security-descriptors.md)
-   [<span data-ttu-id="3ba25-111">Modificando as permissões de acesso em um objeto</span><span class="sxs-lookup"><span data-stu-id="3ba25-111">Modifying the access permissions on an object</span></span>](setting-access-rights-on-an-object.md)
-   [<span data-ttu-id="3ba25-112">Como os descritores de segurança são definidos em novos objetos de diretório</span><span class="sxs-lookup"><span data-stu-id="3ba25-112">How security descriptors are set on new directory objects</span></span>](how-security-descriptors-are-set-on-new-directory-objects.md)
-   [<span data-ttu-id="3ba25-113">Criando um descritor de segurança para um novo objeto de diretório</span><span class="sxs-lookup"><span data-stu-id="3ba25-113">Creating a Security Descriptor for a New Directory Object</span></span>](creating-a-security-descriptor-for-a-new-directory-object.md)
-   [<span data-ttu-id="3ba25-114">Usando a herança de permissões de acesso para habilitar o acesso administrativo a uma subárvore inteira do diretório</span><span class="sxs-lookup"><span data-stu-id="3ba25-114">Using inheritance of access permissions to enable administrative access to an entire subtree of the directory</span></span>](inheritance-and-delegation-of-administration.md)
-   [<span data-ttu-id="3ba25-115">Criando, modificando e lendo o descritor de segurança padrão para uma classe de objeto</span><span class="sxs-lookup"><span data-stu-id="3ba25-115">Creating, modifying, and reading the default security descriptor for an object class</span></span>](default-security-descriptor.md)
-   [<span data-ttu-id="3ba25-116">Criação, configuração e verificação de direitos de acesso de controle para operações que vão além daquelas cobertas pelos direitos predefinidos</span><span class="sxs-lookup"><span data-stu-id="3ba25-116">Creating, setting, and checking control access rights for operations that go beyond those covered by the predefined rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="3ba25-117">Usando DsAddSidHistory</span><span class="sxs-lookup"><span data-stu-id="3ba25-117">Using DsAddSidHistory</span></span>](using-dsaddsidhistory.md)
-   [<span data-ttu-id="3ba25-118">Controlando a visibilidade do objeto</span><span class="sxs-lookup"><span data-stu-id="3ba25-118">Controlling Object Visibility</span></span>](controlling-object-visibility.md)
-   [<span data-ttu-id="3ba25-119">DACLs nulas e DACLs vazias</span><span class="sxs-lookup"><span data-stu-id="3ba25-119">Null DACLs and Empty DACLs</span></span>](null-dacls-and-empty-dacls.md)

 

 




