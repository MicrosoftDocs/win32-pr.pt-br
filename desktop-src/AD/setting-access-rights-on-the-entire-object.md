---
title: Configurando direitos de acesso em todo o objeto
description: Determinadas permissões podem ser definidas somente para um objeto inteiro, como excluir e listar conteúdo. Permissões específicas de operação, como a permissão de leitura, também podem ser definidas para o objeto inteiro para que se apliquem a um objeto inteiro.
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- Configurando direitos de acesso no AD do objeto inteiro
- AD de objetos, configurando direitos de acesso em
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453901"
---
# <a name="setting-access-rights-on-the-entire-object"></a><span data-ttu-id="ea276-106">Configurando direitos de acesso em todo o objeto</span><span class="sxs-lookup"><span data-stu-id="ea276-106">Setting Access Rights on the Entire Object</span></span>

<span data-ttu-id="ea276-107">Determinadas permissões podem ser definidas somente para um objeto inteiro, como excluir e listar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ea276-107">Certain permissions can be set only for an entire object, such as Delete and List Contents.</span></span> <span data-ttu-id="ea276-108">Permissões específicas de operação, como a permissão de leitura, também podem ser definidas para o objeto inteiro para que se apliquem a um objeto inteiro.</span><span class="sxs-lookup"><span data-stu-id="ea276-108">Operation-specific permissions, such as the Read permission, can also be set for entire object so that they apply to an entire object.</span></span>

<span data-ttu-id="ea276-109">O procedimento a seguir pode ser usado para definir permissões para um objeto inteiro.</span><span class="sxs-lookup"><span data-stu-id="ea276-109">The following procedure can be used to set permissions for an entire object.</span></span>

<span data-ttu-id="ea276-110">**Para definir permissões para um objeto inteiro**</span><span class="sxs-lookup"><span data-stu-id="ea276-110">**To set permissions for an entire object**</span></span>

1.  <span data-ttu-id="ea276-111">Defina [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ permitido** ou **ADS \_ AceType \_ acesso \_ negado**.</span><span class="sxs-lookup"><span data-stu-id="ea276-111">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED** or **ADS\_ACETYPE\_ACCESS\_DENIED**.</span></span>
2.  <span data-ttu-id="ea276-112">Defina [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) e **IADsAccessControlEntry. InheritedObjectType** como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ea276-112">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) and **IADsAccessControlEntry.InheritedObjectType** to **NULL**.</span></span>

<span data-ttu-id="ea276-113">Para obter mais informações sobre como criar uma ACE, consulte [definindo direitos de acesso em um objeto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="ea276-113">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="ea276-114">Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="ea276-114">For more information and a code example that can be used to set an ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 