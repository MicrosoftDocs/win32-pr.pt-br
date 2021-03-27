---
title: Interfaces de versão comuns
description: Esta seção contém informações sobre as interfaces de versão comuns.
ms.assetid: d228c3c2-e2ff-4723-aec1-5c3ce82c321d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f535650fa24593cc4b663c1a2b01a1a2d53a9b3b
ms.sourcegitcommit: 8f833c83be1accc119cc57e67b608ffe1e0159b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/07/2020
ms.locfileid: "103642945"
---
# <a name="common-version-interfaces"></a><span data-ttu-id="61cdb-103">Interfaces de versão comuns</span><span class="sxs-lookup"><span data-stu-id="61cdb-103">Common version interfaces</span></span>

<span data-ttu-id="61cdb-104">Esta seção contém informações sobre as interfaces de versão comuns.</span><span class="sxs-lookup"><span data-stu-id="61cdb-104">This section contains information about the common version interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61cdb-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="61cdb-105">In this section</span></span>

| <span data-ttu-id="61cdb-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="61cdb-106">Topic</span></span> | <span data-ttu-id="61cdb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="61cdb-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="61cdb-108">**ID3D10Blob**</span><span class="sxs-lookup"><span data-stu-id="61cdb-108">**ID3D10Blob**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3d10blob) | <span data-ttu-id="61cdb-109">Essa interface é usada para retornar dados de comprimento arbitrário.</span><span class="sxs-lookup"><span data-stu-id="61cdb-109">This interface is used to return arbitrary-length data.</span></span> |
| <span data-ttu-id="61cdb-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="61cdb-110">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span> | <span data-ttu-id="61cdb-111">Essa interface é usada para retornar dados de comprimento arbitrário.</span><span class="sxs-lookup"><span data-stu-id="61cdb-111">This interface is used to return data of arbitrary length.</span></span> |
| [<span data-ttu-id="61cdb-112">**ID3DDestructionNotifier**</span><span class="sxs-lookup"><span data-stu-id="61cdb-112">**ID3DDestructionNotifier**</span></span>](/windows/win32/api/d3dcommon/nn-d3dcommon-id3ddestructionotifier) | <span data-ttu-id="61cdb-113">Usado para se registrar para retornos de chamada quando um objeto nano 3D direto for destruído.</span><span class="sxs-lookup"><span data-stu-id="61cdb-113">Used to register for callbacks when a Direct 3D nano-COM object is destroyed.</span></span> |
| [<span data-ttu-id="61cdb-114">**ID3DInclude**</span><span class="sxs-lookup"><span data-stu-id="61cdb-114">**ID3DInclude**</span></span>](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) | <span data-ttu-id="61cdb-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) é uma interface de inclusão que o usuário implementa para permitir que um aplicativo chame métodos substituíveis pelo usuário para abrir e fechar arquivos de inclusão de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="61cdb-115">[**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) is an include interface that the user implements to allow an application to call user-overridable methods for opening and closing shader \#include files.</span></span> |
| [<span data-ttu-id="61cdb-116">**ID3DUserDefinedAnnotation**</span><span class="sxs-lookup"><span data-stu-id="61cdb-116">**ID3DUserDefinedAnnotation**</span></span>](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) | <span data-ttu-id="61cdb-117">A interface [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) permite que um aplicativo Descreva seções conceituais e marcadores dentro do fluxo de código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61cdb-117">The [**ID3DUserDefinedAnnotation**](/windows/desktop/api/D3D11_1/nn-d3d11_1-id3duserdefinedannotation) interface enables an application to describe conceptual sections and markers within the application's code flow.</span></span> <span data-ttu-id="61cdb-118">Uma ferramenta habilitada adequadamente, como o Microsoft Visual Studio Ultimate 2012, pode exibir essas seções e marcadores visualmente ao longo da linha de tempo do Microsoft Direct3D da ferramenta, enquanto a ferramenta desbugs o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61cdb-118">An appropriately enabled tool, such as Microsoft Visual Studio Ultimate 2012, can display these sections and markers visually along the tool's Microsoft Direct3D time line, while the tool debugs the application.</span></span> <span data-ttu-id="61cdb-119">Essas observações visuais permitem que os usuários de tal ferramenta naveguem para partes da linha de tempo que são de interesse ou para entender qual conjunto de chamadas Direct3D são produzidos por determinadas seções do código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61cdb-119">These visual notes allow users of such a tool to navigate to parts of the time line that are of interest, or to understand what set of Direct3D calls are produced by certain sections of the application's code.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="61cdb-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61cdb-120">Related topics</span></span>

[<span data-ttu-id="61cdb-121">Referência de versão comum</span><span class="sxs-lookup"><span data-stu-id="61cdb-121">Common version reference</span></span>](d3d11-graphics-reference-d3d11-common.md)
