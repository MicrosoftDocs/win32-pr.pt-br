---
title: Tipos de usuário desconhecidos
description: Tipos de usuário desconhecidos
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294540"
---
# <a name="unknown-user-types"></a><span data-ttu-id="83171-103">Tipos de usuário desconhecidos</span><span class="sxs-lookup"><span data-stu-id="83171-103">Unknown User Types</span></span>

<span data-ttu-id="83171-104">Você pode facilitar a localização do produto adicionando a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="83171-104">You can ease product localization by adding the following registry key:</span></span>

<span data-ttu-id="83171-105">**HKEY \_ \_Computadores locais \\ software \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *UserType*</span><span class="sxs-lookup"><span data-stu-id="83171-105">**HKEY\_LOCAL\_MACHINES\\SOFTWARE\\Microsoft\\OLE2**\\**UnknownUserType** = *usertype*</span></span>

<span data-ttu-id="83171-106">Essa chave permite que o Functions retorne uma cadeia de caracteres especificada, em vez de um valor padrão de "Unknown", permitindo que os localizadores especifiquem um tipo de usuário de um idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="83171-106">This key allows functions to return a specified string rather than a default value of "Unknown", enabling localizers to specify a user type of a different language.</span></span>

<span data-ttu-id="83171-107">A implementação do manipulador padrão COM de [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examina o registro chamando [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="83171-107">The COM default handler's implementation of [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examines the registry by calling [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span> <span data-ttu-id="83171-108">Se a classe do objeto não for encontrada no registro, o tipo de usuário da instância [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) do objeto será retornado.</span><span class="sxs-lookup"><span data-stu-id="83171-108">If the object's class is not found in the registry, the user type from the object's [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) instance is returned.</span></span> <span data-ttu-id="83171-109">Se a classe não for encontrada na instância **IStorage** do objeto, a cadeia de caracteres "Unknown" será retornada.</span><span class="sxs-lookup"><span data-stu-id="83171-109">If the class is not found in the object's **IStorage** instance, the string "Unknown" is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83171-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83171-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83171-111">Registrando aplicativos COM</span><span class="sxs-lookup"><span data-stu-id="83171-111">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 