---
title: Chave de ProgID
description: Um ProgID (identificador programático) é uma entrada de registro que pode ser associada a um CLSID. Assim como o CLSID, o ProgID identifica uma classe, mas com menos precisão porque não é garantido que seja globalmente exclusivo.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008734"
---
# <a name="progid-key"></a><span data-ttu-id="938b4-104">Chave de ProgID</span><span class="sxs-lookup"><span data-stu-id="938b4-104">ProgID Key</span></span>

<span data-ttu-id="938b4-105">Um ProgID (identificador programático) é uma entrada de registro que pode ser associada a um CLSID.</span><span class="sxs-lookup"><span data-stu-id="938b4-105">A programmatic identifier (ProgID) is a registry entry that can be associated with a CLSID.</span></span> <span data-ttu-id="938b4-106">Assim como o CLSID, o ProgID identifica uma classe, mas com menos precisão porque não é garantido que seja globalmente exclusivo.</span><span class="sxs-lookup"><span data-stu-id="938b4-106">Like the CLSID, the ProgID identifies a class but with less precision because it is not guaranteed to be globally unique.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="938b4-107">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="938b4-107">Registry Entry</span></span>

<span data-ttu-id="938b4-108">**HKEY \_ \_Classes de \\ software \\ de computador local** \\ *{* ProgID *}*</span><span class="sxs-lookup"><span data-stu-id="938b4-108">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**\\ *{* ProgID *}*</span></span>



| <span data-ttu-id="938b4-109">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="938b4-109">Registry key</span></span>                            | <span data-ttu-id="938b4-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="938b4-110">Description</span></span>                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="938b4-111">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="938b4-111">**CLSID**</span></span>](clsid.md)                  | <span data-ttu-id="938b4-112">Associa um ProgID a um CLSID.</span><span class="sxs-lookup"><span data-stu-id="938b4-112">Associates a ProgID with a CLSID.</span></span>                                  |
| [<span data-ttu-id="938b4-113">**Insertable**</span><span class="sxs-lookup"><span data-stu-id="938b4-113">**Insertable**</span></span>](insertable-progid.md) | <span data-ttu-id="938b4-114">Indica que essa classe é insertável em contêineres OLE 2.</span><span class="sxs-lookup"><span data-stu-id="938b4-114">Indicates that this class is insertable in OLE 2 containers.</span></span>       |
| [<span data-ttu-id="938b4-115">**Protocolo**</span><span class="sxs-lookup"><span data-stu-id="938b4-115">**Protocol**</span></span>](protocol.md)            | <span data-ttu-id="938b4-116">Indica que esta classe OLE 2 é insertável em contêineres de OLE 1.</span><span class="sxs-lookup"><span data-stu-id="938b4-116">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span> |
| [<span data-ttu-id="938b4-117">**Shell**</span><span class="sxs-lookup"><span data-stu-id="938b4-117">**Shell**</span></span>](shell.md)                  | <span data-ttu-id="938b4-118">Fornece informações de impressão do shell do Windows 3,1 e **abertura de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="938b4-118">Provides Windows 3.1 shell printing and **File Open** information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="938b4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="938b4-119">Remarks</span></span>

<span data-ttu-id="938b4-120">Você pode usar uma ProgID em situações de programação em que não é possível usar um CLSID.</span><span class="sxs-lookup"><span data-stu-id="938b4-120">You can use a ProgID in programming situations where it is not possible to use a CLSID.</span></span> <span data-ttu-id="938b4-121">ProgIDs não devem aparecer na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="938b4-121">ProgIDs should not appear in the user interface.</span></span> <span data-ttu-id="938b4-122">Não há garantia de que os ProgIDs sejam exclusivos, portanto, eles podem ser usados apenas onde as colisões de nomes são gerenciáveis.</span><span class="sxs-lookup"><span data-stu-id="938b4-122">ProgIDs are not guaranteed to be unique, so they can be used only where name collisions are manageable.</span></span>

<span data-ttu-id="938b4-123">O formato de um ProgID é <*programa*>. <*componente*>. <*versão*>, separados por pontos e sem espaços, como em Word.Document. 6.</span><span class="sxs-lookup"><span data-stu-id="938b4-123">The format of a ProgID is <*Program*>.<*Component*>.<*Version*>, separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="938b4-124">O ProgID deve estar em conformidade com os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="938b4-124">The ProgID must comply with the following requirements:</span></span>

-   <span data-ttu-id="938b4-125">Ter no máximo 39 caracteres.</span><span class="sxs-lookup"><span data-stu-id="938b4-125">Have no more than 39 characters.</span></span>
-   <span data-ttu-id="938b4-126">Não conter nenhuma Pontuação (incluindo sublinhados), exceto um ou mais pontos.</span><span class="sxs-lookup"><span data-stu-id="938b4-126">Contain no punctuation (including underscores) except one or more periods.</span></span>
-   <span data-ttu-id="938b4-127">Não começar com um dígito.</span><span class="sxs-lookup"><span data-stu-id="938b4-127">Not start with a digit.</span></span>
-   <span data-ttu-id="938b4-128">Seja diferente do nome de classe de qualquer aplicativo OLE 1, incluindo a versão de OLE 1 do mesmo aplicativo, se houver um.</span><span class="sxs-lookup"><span data-stu-id="938b4-128">Be different from the class name of any OLE 1 application, including the OLE 1 version of the same application, if there is one.</span></span>

<span data-ttu-id="938b4-129">Como o ProgID não deve aparecer na interface do usuário, você pode obter um nome de exibição chamando [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span><span class="sxs-lookup"><span data-stu-id="938b4-129">Because the ProgID should not appear in the user interface, you can obtain a displayable name by calling [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span></span> <span data-ttu-id="938b4-130">Além disso, consulte [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="938b4-130">Also, see [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span>

<span data-ttu-id="938b4-131">A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.</span><span class="sxs-lookup"><span data-stu-id="938b4-131">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="938b4-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="938b4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="938b4-133">**IOleObject:: GetUserType**</span><span class="sxs-lookup"><span data-stu-id="938b4-133">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[<span data-ttu-id="938b4-134">**OleRegGetUserType**</span><span class="sxs-lookup"><span data-stu-id="938b4-134">**OleRegGetUserType**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




