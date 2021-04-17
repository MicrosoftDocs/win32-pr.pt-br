---
title: Monikers de arquivo
description: Monikers de arquivo
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291986"
---
# <a name="file-monikers"></a><span data-ttu-id="217b5-103">Monikers de arquivo</span><span class="sxs-lookup"><span data-stu-id="217b5-103">File Monikers</span></span>

<span data-ttu-id="217b5-104">Os *monikers de arquivo* são a classe de moniker mais simples.</span><span class="sxs-lookup"><span data-stu-id="217b5-104">*File monikers* are the simplest moniker class.</span></span> <span data-ttu-id="217b5-105">Os identificadores de arquivo podem ser usados para identificar qualquer objeto armazenado em seu próprio arquivo.</span><span class="sxs-lookup"><span data-stu-id="217b5-105">File monikers can be used to identify any object that is stored in its own file.</span></span> <span data-ttu-id="217b5-106">Um moniker de arquivo atua como um wrapper para o nome do caminho que o sistema de arquivos nativo atribui ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="217b5-106">A file moniker acts as a wrapper for the path name the native file system assigns to the file.</span></span> <span data-ttu-id="217b5-107">Chamar [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) para esse moniker faria com que esse objeto fosse ativado e, em seguida, retornaria um ponteiro de interface para o objeto.</span><span class="sxs-lookup"><span data-stu-id="217b5-107">Calling [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) for this moniker would cause this object to be activated and then would return an interface pointer to the object.</span></span> <span data-ttu-id="217b5-108">A origem do objeto nomeado pelo moniker deve fornecer uma implementação da interface [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) para dar suporte à associação de um moniker de arquivo.</span><span class="sxs-lookup"><span data-stu-id="217b5-108">The source of the object named by the moniker must provide an implementation of the [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) interface to support binding a file moniker.</span></span> <span data-ttu-id="217b5-109">Os monikers de arquivo podem representar um caminho completo ou relativo.</span><span class="sxs-lookup"><span data-stu-id="217b5-109">File monikers can represent either a complete or a relative path.</span></span>

<span data-ttu-id="217b5-110">Por exemplo, o moniker do arquivo para um objeto de planilha armazenado como o arquivo C: \\ Work \\MySheet.xls conteria informações equivalentes a esse nome de caminho.</span><span class="sxs-lookup"><span data-stu-id="217b5-110">For example, the file moniker for a spreadsheet object stored as the file C:\\Work\\MySheet.xls would contain information equivalent to that path name.</span></span> <span data-ttu-id="217b5-111">No entanto, o moniker não consistiria necessariamente na mesma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="217b5-111">The moniker would not necessarily consist of the same string, however.</span></span> <span data-ttu-id="217b5-112">A cadeia de caracteres é apenas seu *nome displayÂ*, uma representação do conteúdo do moniker que é significativo para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="217b5-112">The string is just its *displayÂ name*, a representation of the moniker's contents that is meaningful to an end user.</span></span> <span data-ttu-id="217b5-113">O nome de exibição, que está disponível por meio do método [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) , é usado somente ao exibir um moniker para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="217b5-113">The display name, which is available through the [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) method, is used only when displaying a moniker to an end user.</span></span> <span data-ttu-id="217b5-114">Esse método obtém o nome de exibição para qualquer uma das classes de moniker.</span><span class="sxs-lookup"><span data-stu-id="217b5-114">This method gets the display name for any of the moniker classes.</span></span> <span data-ttu-id="217b5-115">Internamente, o moniker pode armazenar as mesmas informações em um formato mais eficiente para executar operações de moniker, mas não é significativo para os usuários.</span><span class="sxs-lookup"><span data-stu-id="217b5-115">Internally, the moniker may store the same information in a format that is more efficient for performing moniker operations but isn't meaningful to users.</span></span> <span data-ttu-id="217b5-116">Em seguida, quando esse mesmo objeto é vinculado por meio de uma chamada para o método [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , o objeto seria ativado, provavelmente carregando o arquivo na planilha.</span><span class="sxs-lookup"><span data-stu-id="217b5-116">Then, when this same object is bound through a call to the [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) method, the object would be activated, probably by loading the file into the spreadsheet.</span></span>

<span data-ttu-id="217b5-117">O OLE oferece aos provedores de moniker a função auxiliar [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) que cria um objeto de moniker de arquivo e retorna seu ponteiro para o provedor.</span><span class="sxs-lookup"><span data-stu-id="217b5-117">OLE offers moniker providers the helper function [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) that creates a file moniker object and returns its pointer to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="217b5-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="217b5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="217b5-119">Anti-moniker</span><span class="sxs-lookup"><span data-stu-id="217b5-119">Anti-Monikers</span></span>](anti-monikers.md)
</dt> <dt>

[<span data-ttu-id="217b5-120">Monikers de classe</span><span class="sxs-lookup"><span data-stu-id="217b5-120">Class Monikers</span></span>](class-monikers.md)
</dt> <dt>

[<span data-ttu-id="217b5-121">Monikers compostos</span><span class="sxs-lookup"><span data-stu-id="217b5-121">Composite Monikers</span></span>](composite-monikers.md)
</dt> <dt>

[<span data-ttu-id="217b5-122">Monikers de item</span><span class="sxs-lookup"><span data-stu-id="217b5-122">Item Monikers</span></span>](item-monikers.md)
</dt> <dt>

[<span data-ttu-id="217b5-123">Monikers de ponteiro</span><span class="sxs-lookup"><span data-stu-id="217b5-123">Pointer Monikers</span></span>](pointer-monikers.md)
</dt> </dl>

 

 




