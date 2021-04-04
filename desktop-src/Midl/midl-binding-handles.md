---
title: Identificadores de associação de MIDL
description: Identificadores de associação são objetos de dados que representam a associação entre o cliente e o servidor.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- tipos de dados MIDL, identificadores de associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007380"
---
# <a name="midl-binding-handles"></a><span data-ttu-id="8e82a-104">Identificadores de associação de MIDL</span><span class="sxs-lookup"><span data-stu-id="8e82a-104">MIDL Binding Handles</span></span>

<span data-ttu-id="8e82a-105">Identificadores de associação são objetos de dados que representam a associação entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="8e82a-105">Binding handles are data objects that represent the binding between the client and the server.</span></span>

<span data-ttu-id="8e82a-106">MIDL dá suporte ao manipulador de tipo base [**\_ t**](handle-t.md).</span><span class="sxs-lookup"><span data-stu-id="8e82a-106">MIDL supports the base type [**handle\_t**](handle-t.md).</span></span> <span data-ttu-id="8e82a-107">Os identificadores desse tipo são conhecidos como "identificadores primitivos".</span><span class="sxs-lookup"><span data-stu-id="8e82a-107">Handles of this type are known as "primitive handles."</span></span>

<span data-ttu-id="8e82a-108">Você pode definir seus próprios tipos de identificador usando o atributo **\[ Handle \]** .</span><span class="sxs-lookup"><span data-stu-id="8e82a-108">You can define your own handle types using the **\[handle\]** attribute.</span></span> <span data-ttu-id="8e82a-109">Os identificadores definidos dessa forma são conhecidos como identificadores "definidos pelo usuário" ou "personalizados" ou "genéricos".</span><span class="sxs-lookup"><span data-stu-id="8e82a-109">Handles defined in this way are known as "user-defined" or "customized" or "generic" handles.</span></span>

<span data-ttu-id="8e82a-110">Você também pode definir um identificador que mantém informações de estado usando o atributo de **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="8e82a-110">You can also define a handle that maintains state information using the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span> <span data-ttu-id="8e82a-111">Os identificadores definidos dessa maneira são conhecidos como identificadores de "contexto".</span><span class="sxs-lookup"><span data-stu-id="8e82a-111">Handles defined in this way are known as "context" handles.</span></span>

<span data-ttu-id="8e82a-112">Se nenhuma informação de estado for necessária e você não optar por chamar as bibliotecas de tempo de execução RPC para gerenciar o identificador, você poderá solicitar que as bibliotecas de tempo de execução forneçam associação automática.</span><span class="sxs-lookup"><span data-stu-id="8e82a-112">If no state information is needed and you do not choose to call the RPC run-time libraries to manage the handle, you can request that the run-time libraries provide automatic binding.</span></span> <span data-ttu-id="8e82a-113">Isso é feito usando o **\[** [**\_ identificador automático**](auto-handle.md)de palavra-chave ACF **\]** .</span><span class="sxs-lookup"><span data-stu-id="8e82a-113">This is done by using the ACF keyword **\[**[**auto\_handle**](auto-handle.md)**\]**.</span></span>

<span data-ttu-id="8e82a-114">Você pode especificar uma variável global como o identificador de associação usando o **\[** [**\_ identificador implícito**](implicit-handle.md)da palavra-chave ACF **\]** .</span><span class="sxs-lookup"><span data-stu-id="8e82a-114">You can specify a global variable as the binding handle by using the ACF keyword **\[**[**implicit\_handle**](implicit-handle.md)**\]**.</span></span> <span data-ttu-id="8e82a-115">A palavra-chave de **\[ \_ identificador \] explícita** é usada para declarar que cada função remota tem um identificador explicitamente especificado.</span><span class="sxs-lookup"><span data-stu-id="8e82a-115">The **\[explicit\_handle\]** keyword is used to state that each remote function has an explicitly specified handle.</span></span>

<span data-ttu-id="8e82a-116">Para obter mais informações, consulte [Binding e Handles](/windows/desktop/Rpc/binding-and-handles).</span><span class="sxs-lookup"><span data-stu-id="8e82a-116">For more information, see [Binding and Handles](/windows/desktop/Rpc/binding-and-handles).</span></span>

 

 