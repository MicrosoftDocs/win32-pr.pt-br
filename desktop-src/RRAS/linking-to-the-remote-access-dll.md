---
title: Vinculando à DLL de acesso remoto
description: Se um aplicativo for vinculado estaticamente à DLL RASAPI32, o aplicativo não será carregado se o serviço de acesso remoto não estiver instalado.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823897"
---
# <a name="linking-to-the-remote-access-dll"></a><span data-ttu-id="f6c4f-103">Vinculando à DLL de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="f6c4f-103">Linking to the Remote Access DLL</span></span>

<span data-ttu-id="f6c4f-104">Se um aplicativo for vinculado estaticamente à DLL RASAPI32, o aplicativo não será carregado se o serviço de acesso remoto não estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="f6c4f-104">If an application links statically to the RASAPI32 DLL, the application will fail to load if Remote Access Service is not installed.</span></span> <span data-ttu-id="f6c4f-105">Um aplicativo RAS pode ser carregado quando o RAS não é instalado usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar a dll e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter ponteiros para as funções RAS.</span><span class="sxs-lookup"><span data-stu-id="f6c4f-105">A RAS application can load when RAS is not installed by using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to load the DLL, and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain pointers to the RAS functions.</span></span>

<span data-ttu-id="f6c4f-106">As funções RAS estão localizadas em RASAPI32.DLL.</span><span class="sxs-lookup"><span data-stu-id="f6c4f-106">The RAS functions are located in RASAPI32.DLL.</span></span> <span data-ttu-id="f6c4f-107">A biblioteca de importação para essas funções é RASAPI32. LIB.</span><span class="sxs-lookup"><span data-stu-id="f6c4f-107">The import library for these functions is RASAPI32.LIB.</span></span> <span data-ttu-id="f6c4f-108">Para usar as funções RAS, seus programas devem incluir os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="f6c4f-108">To use the RAS functions, your programs must include the following files:</span></span>



| <span data-ttu-id="f6c4f-109">Arquivo</span><span class="sxs-lookup"><span data-stu-id="f6c4f-109">File</span></span>       | <span data-ttu-id="f6c4f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6c4f-110">Description</span></span>                                                                 |
|------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="f6c4f-111">Services. T</span><span class="sxs-lookup"><span data-stu-id="f6c4f-111">RAS.H</span></span>      | <span data-ttu-id="f6c4f-112">Contém os protótipos de função RAS, constantes e definições de estrutura.</span><span class="sxs-lookup"><span data-stu-id="f6c4f-112">Contains the RAS function prototypes, constants, and structure definitions.</span></span> |
| <span data-ttu-id="f6c4f-113">RASERROR. T</span><span class="sxs-lookup"><span data-stu-id="f6c4f-113">RASERROR.H</span></span> | <span data-ttu-id="f6c4f-114">Contém os códigos de erro de RAS.</span><span class="sxs-lookup"><span data-stu-id="f6c4f-114">Contains the RAS error codes.</span></span>                                               |



 

 

 