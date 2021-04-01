---
title: Obtendo uma ID de link
description: A partir do Windows Server 2003, não é mais necessário solicitar uma LinkId da Microsoft; Há um processo para gerar automaticamente um LinkID.
ms.assetid: e3bf2936-40b1-46b5-8ee9-ab208bb388f6
ms.tgt_platform: multiple
keywords:
- Obtendo uma ID de link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6893baab780d7fb481de0af77a607e988c3f87a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084443"
---
# <a name="obtaining-a-link-id"></a><span data-ttu-id="e7083-104">Obtendo uma ID de link</span><span class="sxs-lookup"><span data-stu-id="e7083-104">Obtaining a Link ID</span></span>

<span data-ttu-id="e7083-105">A partir do Windows Server 2003, não é mais necessário solicitar uma [**LinkId**](/windows/desktop/ADSchema/a-linkid) da Microsoft; Há um processo para gerar automaticamente um **LinkId**.</span><span class="sxs-lookup"><span data-stu-id="e7083-105">Starting with Windows Server 2003, it is no longer necessary to request a [**linkID**](/windows/desktop/ADSchema/a-linkid) from Microsoft; there is a process for automatically generating a **linkID**.</span></span> <span data-ttu-id="e7083-106">O sistema irá gerar automaticamente uma ID de link para um novo atributo vinculado quando o atributo **LinkId** do atributo for definido como 1.2.840.113556.1.2.50.</span><span class="sxs-lookup"><span data-stu-id="e7083-106">The system will automatically generate a link ID for a new linked attribute when the attribute's **linkID** attribute is set to 1.2.840.113556.1.2.50.</span></span> <span data-ttu-id="e7083-107">Um link regressivo para esse link de encaminhamento é criado definindo o **LinkId** para o [**AttributeID**](/windows/desktop/ADSchema/a-attributeid) ou o [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) do link de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="e7083-107">A back link for this forward link is created by setting the **linkID** to the [**attributeID**](/windows/desktop/ADSchema/a-attributeid) or [**ldapDisplayName**](/windows/desktop/ADSchema/a-ldapdisplayname) of the forward link.</span></span> <span data-ttu-id="e7083-108">O cache de esquema deve ser recarregado após a criação do link de encaminhamento e antes da criação do link voltar.</span><span class="sxs-lookup"><span data-stu-id="e7083-108">The schema cache must be reloaded after creating the forward link and before creating the back link.</span></span> <span data-ttu-id="e7083-109">Caso contrário, o **AttributeID** ou **ldapDisplayName** do link de encaminhamento não será encontrado quando o link voltar for criado.</span><span class="sxs-lookup"><span data-stu-id="e7083-109">Otherwise, the forward link's **attributeId** or **ldapDisplayName** will not be found when the back link is created.</span></span> <span data-ttu-id="e7083-110">O cache de esquema é recarregado sob demanda, alguns minutos depois que uma alteração de esquema é feita ou quando o DC é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e7083-110">The schema cache is reloaded on demand, a few minutes after a schema change is made, or when the DC is restarted.</span></span> <span data-ttu-id="e7083-111">Crie todos os links de encaminhamento, recarregue o cache de esquema e, em seguida, crie todos os links de volta.</span><span class="sxs-lookup"><span data-stu-id="e7083-111">Create all forward links, reload the schema cache and then create all back links.</span></span>

<span data-ttu-id="e7083-112">Por exemplo, quando você criou os novos atributos **myForwardLinkAttr** e **myBackLinkAttr**, e deseja vinculá-los:</span><span class="sxs-lookup"><span data-stu-id="e7083-112">For example, when you have created the new attributes **myForwardLinkAttr** and **myBackLinkAttr**, and wish to link them:</span></span>

> [!Note]  
> <span data-ttu-id="e7083-113">Os OIDs neste exemplo são forçado.</span><span class="sxs-lookup"><span data-stu-id="e7083-113">The OIDs in this example are contrived.</span></span> <span data-ttu-id="e7083-114">Consulte [obtendo um identificador de objeto da Microsoft](obtaining-an-object-identifier-from-microsoft.md) para obter instruções sobre como obter OIDs para novos atributos.</span><span class="sxs-lookup"><span data-stu-id="e7083-114">See [Obtaining an Object Identifier from Microsoft](obtaining-an-object-identifier-from-microsoft.md) for instructions on obtaining OIDs for new attributes.</span></span>

 

1.  <span data-ttu-id="e7083-115">Defina esses atributos no atributo que deve ser o link de encaminhamento:</span><span class="sxs-lookup"><span data-stu-id="e7083-115">Set these attributes on the attribute that is to be the forward link:</span></span>
    ```C++
    ldapDisplayName: myForwardLinkAttr
    OID: 1.2.840.113556.6.1234
    LinkID: 1.2.840.113556.1.2.50
    ```

    

2.  <span data-ttu-id="e7083-116">Recarregue o esquema.</span><span class="sxs-lookup"><span data-stu-id="e7083-116">Reload the Schema.</span></span>
3.  <span data-ttu-id="e7083-117">Defina esses atributos no atributo que será o link voltar:</span><span class="sxs-lookup"><span data-stu-id="e7083-117">Set these attributes on the attribute that is to be the back link:</span></span>
    ```C++
    ldapDisplayName: myBackLinkAttr
    OID: 1.2.840.113556.6.1235
    LinkID: 1.2.840.113556.6.1234 or myForwardLinkAttr
    ```

    

## <a name="related-topics"></a><span data-ttu-id="e7083-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7083-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7083-119">Atributos vinculados</span><span class="sxs-lookup"><span data-stu-id="e7083-119">Linked Attributes</span></span>](linked-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7083-120">Como estender o esquema</span><span class="sxs-lookup"><span data-stu-id="e7083-120">How to Extend the Schema</span></span>](how-to-extend-the-schema.md)
</dt> </dl>

 

 