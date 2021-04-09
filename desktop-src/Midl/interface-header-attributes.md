---
title: Atributos de cabeçalho de interface
description: Incorpore esses atributos no cabeçalho da interface para transmitir informações sobre a interface inteira.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- MIDL, atributos, cabeçalho de interface IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e5fc25a0e441b092749872a1b4d4735d483cae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005324"
---
# <a name="interface-header-attributes"></a><span data-ttu-id="d165e-104">Atributos de cabeçalho de interface</span><span class="sxs-lookup"><span data-stu-id="d165e-104">Interface Header Attributes</span></span>

<span data-ttu-id="d165e-105">Incorpore esses atributos no cabeçalho da interface para transmitir informações sobre a interface inteira.</span><span class="sxs-lookup"><span data-stu-id="d165e-105">Incorporate these attributes in the interface header to convey information about the entire interface.</span></span>



| <span data-ttu-id="d165e-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="d165e-106">Attribute</span></span>                                   | <span data-ttu-id="d165e-107">Uso</span><span class="sxs-lookup"><span data-stu-id="d165e-107">Usage</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d165e-108">**\_UUID assíncrono**</span><span class="sxs-lookup"><span data-stu-id="d165e-108">**async\_uuid**</span></span>](async-uuid.md)           | <span data-ttu-id="d165e-109">Direciona o compilador MIDL para definir as versões síncrona e assíncrona de uma interface COM.</span><span class="sxs-lookup"><span data-stu-id="d165e-109">Directs the MIDL compiler to define both synchronous and asynchronous versions of a COM interface.</span></span>                                                                                                                                               |
| [<span data-ttu-id="d165e-110">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="d165e-110">**uuid**</span></span>](uuid.md)                        | <span data-ttu-id="d165e-111">Designa um valor de 128 bits que distingue uma interface específica de todas as outras.</span><span class="sxs-lookup"><span data-stu-id="d165e-111">Designates a 128-bit value that distinguishes a particular interface from all others.</span></span> <span data-ttu-id="d165e-112">O valor real pode representar um GUID, um CLSID ou um IID.</span><span class="sxs-lookup"><span data-stu-id="d165e-112">The actual value may represent a GUID, a CLSID, or an IID.</span></span>                                                                                                 |
| [<span data-ttu-id="d165e-113">**local**</span><span class="sxs-lookup"><span data-stu-id="d165e-113">**local**</span></span>](local.md)                      | <span data-ttu-id="d165e-114">Direciona o compilador MIDL para gerar somente arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d165e-114">Directs the MIDL compiler to generate header files only.</span></span> <span data-ttu-id="d165e-115">Uma interface deve ter um [**UUID**](uuid.md) ou um atributo [**local**](local.md) .</span><span class="sxs-lookup"><span data-stu-id="d165e-115">An interface must have either a [**uuid**](uuid.md) or a [**local**](local.md) attribute.</span></span>                                                                                             |
| [<span data-ttu-id="d165e-116">**\_União MS**</span><span class="sxs-lookup"><span data-stu-id="d165e-116">**ms\_union**</span></span>](-ms-union.md)              | <span data-ttu-id="d165e-117">Controla o alinhamento de NDR de uniões não encapsuladas.</span><span class="sxs-lookup"><span data-stu-id="d165e-117">Controls the NDR alignment of nonencapsulated unions.</span></span> <span data-ttu-id="d165e-118">Use para compatibilidade com versões anteriores com interfaces criadas no MIDL 1,0 ou 2,0.</span><span class="sxs-lookup"><span data-stu-id="d165e-118">Use for backward compatibility with interfaces built on MIDL 1.0 or 2.0.</span></span>                                                                                                                   |
| [<span data-ttu-id="d165e-119">**objeto**</span><span class="sxs-lookup"><span data-stu-id="d165e-119">**object**</span></span>](object.md)                    | <span data-ttu-id="d165e-120">Identifica a interface como uma interface COM e direciona o compilador MIDL para gerar código de proxy/stub em vez de stubs de cliente e de servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="d165e-120">Identifies the interface as a COM interface and directs the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span>                                                                                                    |
| [<span data-ttu-id="d165e-121">**Versão**</span><span class="sxs-lookup"><span data-stu-id="d165e-121">**version**</span></span>](version.md)                  | <span data-ttu-id="d165e-122">Identifica uma versão específica de uma interface em casos em que existem várias versões da interface.</span><span class="sxs-lookup"><span data-stu-id="d165e-122">Identifies a particular version of an interface in cases where multiple versions of the interface exist.</span></span> <span data-ttu-id="d165e-123">Como as interfaces COM são imutáveis, você não pode usar o atributo [**version**](version.md) em uma interface de [**objeto**](object.md) .</span><span class="sxs-lookup"><span data-stu-id="d165e-123">Because COM interfaces are immutable, you cannot use the [**version**](version.md) attribute on an [**object**](object.md) interface.</span></span> |
| [<span data-ttu-id="d165e-124">**padrão de ponteiro \_**</span><span class="sxs-lookup"><span data-stu-id="d165e-124">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="d165e-125">Especifica o tipo de ponteiro padrão para todos os ponteiros, exceto aqueles incluídos nas listas de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d165e-125">Specifies the default pointer type for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="d165e-126">O tipo padrão pode ser [**Unique**](unique.md), [**ref**](ref.md)ou [**PTR**](ptr.md).</span><span class="sxs-lookup"><span data-stu-id="d165e-126">The default type can be [**unique**](unique.md), [**ref**](ref.md), or [**ptr**](ptr.md).</span></span>                                                   |
| [<span data-ttu-id="d165e-127">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="d165e-127">**endpoint**</span></span>](endpoint.md)                | <span data-ttu-id="d165e-128">Especifica um ponto de extremidade estático (bem conhecido) no qual um aplicativo de servidor escutará chamadas de procedimento remotas.</span><span class="sxs-lookup"><span data-stu-id="d165e-128">Specifies a static (well-known) endpoint on which a server application will listen for remote procedure calls.</span></span>                                                                                                                                   |



 

<span data-ttu-id="d165e-129">Consulte [atributos de biblioteca de tipos](type-library-attributes.md) para atributos de interface, como [**Dual**](dual.md) e [**oleautomation**](oleautomation.md), que são específicos para interfaces definidas ou referenciadas dentro de uma instrução de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d165e-129">See [Type Library Attributes](type-library-attributes.md) for interface attributes, such as [**dual**](dual.md) and [**oleautomation**](oleautomation.md), that are specific to interfaces defined or referenced inside a library statement.</span></span>

 

 




