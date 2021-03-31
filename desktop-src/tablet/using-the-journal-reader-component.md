---
description: O componente leitor de notas do diário do Microsoft Windows fornece acesso de leitura programático a arquivos no formato de diário.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Usando o componente de leitor de diário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920878"
---
# <a name="using-the-journal-reader-component"></a><span data-ttu-id="b004a-103">Usando o componente de leitor de diário</span><span class="sxs-lookup"><span data-stu-id="b004a-103">Using the Journal Reader Component</span></span>

<span data-ttu-id="b004a-104">O componente leitor de notas do diário do Microsoft Windows fornece acesso de leitura programático a arquivos no formato de diário.</span><span class="sxs-lookup"><span data-stu-id="b004a-104">The Microsoft Windows Journal Note Reader component provides programmatic read access to files in the Journal format.</span></span>

## <a name="component-overview"></a><span data-ttu-id="b004a-105">Visão geral do componente</span><span class="sxs-lookup"><span data-stu-id="b004a-105">Component Overview</span></span>

<span data-ttu-id="b004a-106">Os arquivos de diário têm a extensão de arquivo. jnt.</span><span class="sxs-lookup"><span data-stu-id="b004a-106">Journal files have the .jnt file extension.</span></span> <span data-ttu-id="b004a-107">Esse componente simples usa um fluxo que contém um arquivo. jnt e retorna um fluxo que contém o conteúdo do arquivo em formato XML.</span><span class="sxs-lookup"><span data-stu-id="b004a-107">This simple component takes a stream containing a .jnt file and returns a stream containing the file's content in XML format.</span></span> <span data-ttu-id="b004a-108">O XML retornado pelo componente está de acordo com o esquema de leitor de nota do diário.</span><span class="sxs-lookup"><span data-stu-id="b004a-108">The XML returned by the component conforms to the Journal Note Reader schema.</span></span> <span data-ttu-id="b004a-109">Esse esquema está documentado na [referência de esquema do leitor de diário](journal-reader-schema-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b004a-109">This schema is documented in [Journal Reader Schema Reference](journal-reader-schema-reference.md).</span></span>

<span data-ttu-id="b004a-110">O componente não fornece a capacidade de gravar arquivos. jnt.</span><span class="sxs-lookup"><span data-stu-id="b004a-110">The component does not provide the ability to write out .jnt files.</span></span>

<span data-ttu-id="b004a-111">O componente está disponível em versões não gerenciadas e gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="b004a-111">The component is available in unmanaged and managed versions.</span></span> <span data-ttu-id="b004a-112">O componente não gerenciado está disponível no journal.dll biblioteca de vínculo dinâmico (DLL).</span><span class="sxs-lookup"><span data-stu-id="b004a-112">The unmanaged component is available in the journal.dll dynamic link library (DLL).</span></span> <span data-ttu-id="b004a-113">A versão gerenciada está no assembly Microsoft.Ink.Journal.dll (para redistribuição para o Windows XP Tablet PC Edition ou Windows Vista) ou Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="b004a-113">The managed version is either in the Microsoft.Ink.Journal.dll assembly (for redistribution to Windows XP Tablet PC Edition or Windows Vista), or Microsoft.Ink.dll.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="b004a-114">A partir do Windows 10, versão 1607, o journal.dll não está incluído no sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="b004a-114">Beginning with Windows 10, version 1607, journal.dll is not included in the Windows operating system.</span></span> <span data-ttu-id="b004a-115">Essa biblioteca deve ser considerada preterida ou obsoleta e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="b004a-115">That library should be considered deprecated or obsolete and should not be used.</span></span>

 

### <a name="assembly-changes-of-note"></a><span data-ttu-id="b004a-116">Alterações de assembly de observação</span><span class="sxs-lookup"><span data-stu-id="b004a-116">Assembly Changes of Note</span></span>

<span data-ttu-id="b004a-117">É importante estar ciente de algumas alterações no assembly que contêm o componente de leitor de nota do diário que ocorreu entre a versão lançada em conjunto com a versão 1,7 do kit de desenvolvedores de Tablet e a versão fornecida no sistema operacional Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b004a-117">It is important to be aware of some changes to the assembly containing the Journal Note Reader component that occurred between the version released in conjunction with version 1.7 of the Tablet Developers Kit and the version that ships in the Windows Vista operating system.</span></span>

<span data-ttu-id="b004a-118">A versão 1,7 do componente de leitor, que pode ser redistribuído para o Windows XP ou o Windows Vista, está contida em um assembly chamado Microsoft.Ink.Journal.dll.</span><span class="sxs-lookup"><span data-stu-id="b004a-118">The 1.7 version of the reader component, which can be redistributed to either Windows XP or Windows Vista, is contained in an assembly called Microsoft.Ink.Journal.dll.</span></span> <span data-ttu-id="b004a-119">O componente de leitor é fornecido no Windows Vista, mas foi integrado ao assembly de Microsoft.Ink.dll principal.</span><span class="sxs-lookup"><span data-stu-id="b004a-119">The reader component ships in Windows Vista, but has been integrated into the core Microsoft.Ink.dll assembly.</span></span> <span data-ttu-id="b004a-120">Isso significa que os aplicativos que fazem uso do assembly 1,7 precisam redistribuir esse assembly com a configuração.</span><span class="sxs-lookup"><span data-stu-id="b004a-120">This means that applications that make use of the 1.7 assembly need to redistribute that assembly with their setup.</span></span>

## <a name="using-the-component"></a><span data-ttu-id="b004a-121">Usando o componente</span><span class="sxs-lookup"><span data-stu-id="b004a-121">Using the Component</span></span>

<span data-ttu-id="b004a-122">O componente leitor de nota do diário é útil para extrair os dados de tinta e outras informações sobre o arquivo de um arquivo de diário.</span><span class="sxs-lookup"><span data-stu-id="b004a-122">The Journal Note Reader component is useful for extracting the ink data and other information about the file from a Journal file.</span></span>

### <a name="com"></a><span data-ttu-id="b004a-123">COM</span><span class="sxs-lookup"><span data-stu-id="b004a-123">COM</span></span>

<span data-ttu-id="b004a-124">O componente COM do leitor de anotações do diário está no arquivo Journal.dll, que é instalado e registrado quando você baixa e executa o arquivo de instalação do leitor de notas do diário.</span><span class="sxs-lookup"><span data-stu-id="b004a-124">The Journal Note Reader COM component is in the file Journal.dll, which is installed and registered when you download and run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="b004a-125">O componente COM não oferece suporte à interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b004a-125">The COM component does not support the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

### <a name="managed"></a><span data-ttu-id="b004a-126">Gerenciado</span><span class="sxs-lookup"><span data-stu-id="b004a-126">Managed</span></span>

<span data-ttu-id="b004a-127">O componente gerenciado do leitor de anotações do diário está no assembly Microsoft.Ink.JournalReader.dll.</span><span class="sxs-lookup"><span data-stu-id="b004a-127">The Journal Note Reader managed component is in the Microsoft.Ink.JournalReader.dll assembly.</span></span> <span data-ttu-id="b004a-128">Esse assembly é instalado e registrado no cache de assembly global quando você executa o arquivo de instalação do leitor de notas do diário.</span><span class="sxs-lookup"><span data-stu-id="b004a-128">This assembly is installed and registered in the global assembly cache when you run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="b004a-129">Adicione uma referência ao assembly para usá-lo em seu projeto gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b004a-129">Add a reference to the assembly to use it in your managed project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b004a-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b004a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b004a-131">**Interface IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="b004a-131">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="b004a-132">Referência de esquema do leitor de diário</span><span class="sxs-lookup"><span data-stu-id="b004a-132">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

 
