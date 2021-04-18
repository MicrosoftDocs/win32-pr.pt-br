---
description: MFTrace é uma ferramenta para gerar logs de rastreamento para aplicativos Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750180"
---
# <a name="mftrace"></a><span data-ttu-id="d4d6f-103">MFTrace</span><span class="sxs-lookup"><span data-stu-id="d4d6f-103">MFTrace</span></span>

<span data-ttu-id="d4d6f-104">MFTrace é uma ferramenta para gerar logs de rastreamento para aplicativos Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d4d6f-104">MFTrace is a tool for generating trace logs for Media Foundation applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4d6f-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d4d6f-105">In this section</span></span>

-   [<span data-ttu-id="d4d6f-106">Usando MFTrace</span><span class="sxs-lookup"><span data-stu-id="d4d6f-106">Using MFTrace</span></span>](using-mftrace.md)
-   [<span data-ttu-id="d4d6f-107">Palavras-chave MFTrace</span><span class="sxs-lookup"><span data-stu-id="d4d6f-107">MFTrace Keywords</span></span>](mftrace-keywords.md)
-   [<span data-ttu-id="d4d6f-108">Arquivo de configuração MFTrace</span><span class="sxs-lookup"><span data-stu-id="d4d6f-108">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)

## <a name="requirements"></a><span data-ttu-id="d4d6f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4d6f-109">Requirements</span></span>



| <span data-ttu-id="d4d6f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4d6f-110">Requirement</span></span> | <span data-ttu-id="d4d6f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d4d6f-111">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d6f-112">Versão mínima do SDK</span><span class="sxs-lookup"><span data-stu-id="d4d6f-112">Minimum SDK version</span></span>      | <span data-ttu-id="d4d6f-113">SDK (Software Development Kit) do Microsoft Windows para Windows 7 e .NET Framework 4,0</span><span class="sxs-lookup"><span data-stu-id="d4d6f-113">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span> |
| <span data-ttu-id="d4d6f-114">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="d4d6f-114">Minimum operating system</span></span> | <span data-ttu-id="d4d6f-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4d6f-115">Windows Vista</span></span>                                                                         |



 

<span data-ttu-id="d4d6f-116">O MFTrace requer as seguintes DLLs, que também são fornecidas no SDK.</span><span class="sxs-lookup"><span data-stu-id="d4d6f-116">MFTrace requires the following DLLs, which are also provided in the SDK.</span></span>

-   <span data-ttu-id="d4d6f-117">detoured.dll</span><span class="sxs-lookup"><span data-stu-id="d4d6f-117">detoured.dll</span></span>
-   <span data-ttu-id="d4d6f-118">mfdetours.dll</span><span class="sxs-lookup"><span data-stu-id="d4d6f-118">mfdetours.dll</span></span>

<span data-ttu-id="d4d6f-119">O SDK fornece as versões de 32 bits e 64 bits do MFTrace.</span><span class="sxs-lookup"><span data-stu-id="d4d6f-119">The SDK provides both 32-bit and 64-bit versions of MFTrace.</span></span> <span data-ttu-id="d4d6f-120">MFTrace não dá suporte a WOW64; para rastrear um processo de 32 bits em execução no Windows de 64 bits, use a versão de 32 bits do MFTrace.</span><span class="sxs-lookup"><span data-stu-id="d4d6f-120">MFTrace does not support WOW64; to trace a 32-bit process running on 64-bit Windows, use the 32-bit version of MFTrace.</span></span>

<span data-ttu-id="d4d6f-121">SDK-raiz em sistemas de 32 bits: \Program Programas\windows Kits\10 SDK-root no sistema de 64 bits: \Program Files (x86) \Windows Kits\10 você encontrará mftrace no <SDK-root> \Bin \<sdk-version> \<architecture>\mftrace.exe</span><span class="sxs-lookup"><span data-stu-id="d4d6f-121">sdk-root on 32 bit systems: \Program Files\Windows Kits\10 sdk-root on 64 bit system: \Program Files (x86)\Windows Kits\10 You will find mftrace at <sdk-root>\bin\<sdk-version>\<architecture>\mftrace.exe</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4d6f-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4d6f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4d6f-123">Ferramentas de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4d6f-123">Media Foundation Tools</span></span>](media-foundation-tools.md)
</dt> </dl>

 

 



