---
description: Você pode armazenar qualquer tipo de dados específicos do aplicativo com uma superfície. Por exemplo, uma superfície que representa um mapa em um jogo pode conter informações sobre o terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Dados de superfície privada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105761706"
---
# <a name="private-surface-data-direct3d-9"></a><span data-ttu-id="5997e-104">Dados de superfície privada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5997e-104">Private Surface Data (Direct3D 9)</span></span>

<span data-ttu-id="5997e-105">Você pode armazenar qualquer tipo de dados específicos do aplicativo com uma superfície.</span><span class="sxs-lookup"><span data-stu-id="5997e-105">You can store any kind of application-specific data with a surface.</span></span> <span data-ttu-id="5997e-106">Por exemplo, uma superfície que representa um mapa em um jogo pode conter informações sobre o terreno.</span><span class="sxs-lookup"><span data-stu-id="5997e-106">For example, a surface representing a map in a game might contain information about terrain.</span></span>

<span data-ttu-id="5997e-107">Uma superfície pode ter mais de um buffer de dados privado.</span><span class="sxs-lookup"><span data-stu-id="5997e-107">A surface can have more than one private data buffer.</span></span> <span data-ttu-id="5997e-108">Cada buffer é identificado por um GUID que você fornece ao anexar os dados à superfície.</span><span class="sxs-lookup"><span data-stu-id="5997e-108">Each buffer is identified by a GUID that you supply when attaching the data to the surface.</span></span>

<span data-ttu-id="5997e-109">Para armazenar dados de superfície privada, use SetPrivateData, passando um ponteiro para o buffer de origem, o tamanho dos dados e um GUID definido pelo aplicativo para os dados.</span><span class="sxs-lookup"><span data-stu-id="5997e-109">To store private surface data, use SetPrivateData, passing a pointer to the source buffer, the size of the data, and an application-defined GUID for the data.</span></span> <span data-ttu-id="5997e-110">Opcionalmente, os dados de origem podem existir na forma de um objeto COM; Nesse caso, você passa um ponteiro para o ponteiro de interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do objeto e define o sinalizador D3DSPD \_ IUNKNOWNPOINTER.</span><span class="sxs-lookup"><span data-stu-id="5997e-110">Optionally, the source data can exist in the form of a COM object; in this case, you pass a pointer to the object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface pointer and you set the D3DSPD\_IUNKNOWNPOINTER flag.</span></span>

<span data-ttu-id="5997e-111">SetPrivateData aloca um buffer interno para os dados e copia-o.</span><span class="sxs-lookup"><span data-stu-id="5997e-111">SetPrivateData allocates an internal buffer for the data and copies it.</span></span> <span data-ttu-id="5997e-112">Em seguida, você pode liberar com segurança o objeto ou o buffer de origem.</span><span class="sxs-lookup"><span data-stu-id="5997e-112">You can then safely free the source buffer or object.</span></span> <span data-ttu-id="5997e-113">O buffer interno ou a referência de interface é liberada quando FreePrivateData é chamado.</span><span class="sxs-lookup"><span data-stu-id="5997e-113">The internal buffer or interface reference is released when FreePrivateData is called.</span></span> <span data-ttu-id="5997e-114">Isso ocorre automaticamente quando a superfície é liberada.</span><span class="sxs-lookup"><span data-stu-id="5997e-114">This happens automatically when the surface is freed.</span></span>

<span data-ttu-id="5997e-115">Para recuperar dados privados para uma superfície, você deve alocar um buffer do tamanho correto e, em seguida, chamar o método GetPrivateData, passando o GUID que foi atribuído aos dados.</span><span class="sxs-lookup"><span data-stu-id="5997e-115">To retrieve private data for a surface, you must allocate a buffer of the correct size and then call the GetPrivateData method, passing the GUID that was assigned to the data.</span></span> <span data-ttu-id="5997e-116">Você é responsável por liberar qualquer memória dinâmica usada para esse buffer.</span><span class="sxs-lookup"><span data-stu-id="5997e-116">You are responsible for freeing any dynamic memory you use for this buffer.</span></span> <span data-ttu-id="5997e-117">Se os dados forem um objeto COM, esse método recuperará o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5997e-117">If the data is a COM object, this method retrieves the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="5997e-118">Se você não souber o tamanho de um buffer a ser alocado, primeiro chame GetPrivateData com zero em pSizeOfData.</span><span class="sxs-lookup"><span data-stu-id="5997e-118">If you don't know how big a buffer to allocate, first call GetPrivateData with zero in pSizeOfData.</span></span> <span data-ttu-id="5997e-119">Se o método falhar com D3DERR \_ MOREDATA, ele retornará o número necessário de bytes para o buffer.</span><span class="sxs-lookup"><span data-stu-id="5997e-119">If the method fails with D3DERR\_MOREDATA, it returns the necessary number of bytes for the buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5997e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5997e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5997e-121">Superfícies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="5997e-121">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 
