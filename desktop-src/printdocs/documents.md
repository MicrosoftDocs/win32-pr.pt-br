---
description: Esta seção descreve as tecnologias de documento com suporte do Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: Documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625c2f04a43db9433fe125b52a4bbc08e37fb4f4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119981"
---
# <a name="xps-documents"></a><span data-ttu-id="c45d5-103">Documentos XPS</span><span class="sxs-lookup"><span data-stu-id="c45d5-103">XPS Documents</span></span>

<span data-ttu-id="c45d5-104">Esta seção descreve as tecnologias de documento com suporte do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c45d5-104">This section describes the document technologies that are supported by Microsoft Windows.</span></span>

-   [<span data-ttu-id="c45d5-105">Escolhendo uma tecnologia de documento</span><span class="sxs-lookup"><span data-stu-id="c45d5-105">Choosing a Document Technology</span></span>](#choosing-a-document-technology)
-   [<span data-ttu-id="c45d5-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c45d5-106">In This Section</span></span>](#in-this-section)
-   [<span data-ttu-id="c45d5-107">Ferramentas de documento XPS</span><span class="sxs-lookup"><span data-stu-id="c45d5-107">XPS Document Tools</span></span>](#xps-document-tools)
-   [<span data-ttu-id="c45d5-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c45d5-108">Related topics</span></span>](#related-topics)


## <a name="choosing-a-document-technology"></a><span data-ttu-id="c45d5-109">Escolhendo uma tecnologia de documento</span><span class="sxs-lookup"><span data-stu-id="c45d5-109">Choosing a Document Technology</span></span>

<span data-ttu-id="c45d5-110">A Microsoft fornece várias tecnologias de documentos diferentes para dar suporte a uma variedade de aplicativos de documentos:</span><span class="sxs-lookup"><span data-stu-id="c45d5-110">Microsoft provides several different document technologies to support a variety of document applications:</span></span>

-   <span data-ttu-id="c45d5-111">**XPS e OpenXPS**</span><span class="sxs-lookup"><span data-stu-id="c45d5-111">**XPS and OpenXPS**</span></span>

    <span data-ttu-id="c45d5-112">XPS e OpenXPS têm suporte no Windows 8 e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="c45d5-112">XPS and OpenXPS are supported in Windows 8 and later versions of Windows.</span></span> <span data-ttu-id="c45d5-113">Consulte o diagrama anterior para determinar o cenário de uso correto para XPS e OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="c45d5-113">See the preceding diagram to determine the correct usage scenario for XPS and OpenXPS.</span></span> <span data-ttu-id="c45d5-114">Para obter mais informações sobre essas tecnologias de documento, consulte [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span><span class="sxs-lookup"><span data-stu-id="c45d5-114">For more information about these document technologies, see [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).</span></span>

    <span data-ttu-id="c45d5-115">No caso do uso do OpenXPS com o Windows 8 e o Windows Server 2012, o suporte é fornecido apenas por meio da [API de documento XPS](documents-xps.md)</span><span class="sxs-lookup"><span data-stu-id="c45d5-115">In the case of using OpenXPS with Windows 8 and Windows Server 2012, support is only provided via the [XPS Document API](documents-xps.md)</span></span>

    <span data-ttu-id="c45d5-116">Se você precisar converter entre o Microsoft XPS (MSXPS) e o OpenXPS, a Microsoft forneceu uma ferramenta (XPSConverter.exe) que permite converter documentos formatados em MSXPS no formato OpenXPS e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="c45d5-116">If you need to convert between Microsoft XPS (MSXPS) and OpenXPS, then Microsoft has provided a tool (XPSConverter.exe) that allows you to convert MSXPS-formatted documents to the OpenXPS format and vice versa.</span></span> <span data-ttu-id="c45d5-117">A ferramenta faz parte do WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="c45d5-117">The tool is part of the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="c45d5-118">Para baixar o WDK, consulte [como obter o WDK](/windows-hardware/drivers/download-the-wdk).</span><span class="sxs-lookup"><span data-stu-id="c45d5-118">To download the WDK, see [How to get the WDK](/windows-hardware/drivers/download-the-wdk).</span></span>

    <span data-ttu-id="c45d5-119">Para obter mais informações sobre o OpenXPS e o Windows 8, consulte [suporte do OpenXPS no Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span><span class="sxs-lookup"><span data-stu-id="c45d5-119">And for more information about OpenXPS and Windows 8, see [OpenXPS Support in Windows](/windows-hardware/drivers/print/driver-support-for-openxps).</span></span>

-   <span data-ttu-id="c45d5-120">**API de documento XPS**</span><span class="sxs-lookup"><span data-stu-id="c45d5-120">**XPS Document API**</span></span>

    <span data-ttu-id="c45d5-121">A API do documento XPS é uma API nativa do Windows que dá suporte ao OM XPS.</span><span class="sxs-lookup"><span data-stu-id="c45d5-121">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="c45d5-122">A API de documento XPS foi introduzida no Windows 7 e pode ser usada em programas de modo de usuário e drivers de impressora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="c45d5-122">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span>

    <span data-ttu-id="c45d5-123">Para obter mais informações, consulte a API de documento XPS e a [API de assinatura digital XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="c45d5-123">For more information, see the XPS Document API, and [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

    <span data-ttu-id="c45d5-124">\*A API de documento XPS também tem suporte no Windows Vista com Service Pack 2 (SP2) com a atualização de plataforma para Windows Vista e Windows Server 2008 com SP2 usando a atualização de plataforma para o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c45d5-124">\*The XPS Document API is also supported in Windows Vista with Service Pack 2 (SP2) with the Platform Update for Windows Vista and Windows Server 2008 with SP2 using the Platform Update for Windows Server 2008.</span></span> <span data-ttu-id="c45d5-125">Para obter mais informações sobre a atualização de plataforma para Windows Vista ou a atualização de plataforma para o Windows Server 2008, consulte [atualização de plataforma para Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span><span class="sxs-lookup"><span data-stu-id="c45d5-125">For more information about the Platform Update for Windows Vista or the Platform Update for Windows Server 2008, see [Platform Update for Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal)</span></span>

-   <span data-ttu-id="c45d5-126">**.NET Framework**</span><span class="sxs-lookup"><span data-stu-id="c45d5-126">**.NET Framework**</span></span>

    <span data-ttu-id="c45d5-127">.NET Framework fornece suporte a documentos XPS para programas de código gerenciado do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="c45d5-127">.NET Framework provides XPS document support to user-mode, managed-code programs.</span></span>

    <span data-ttu-id="c45d5-128">O .NET Framework 3,0 tem suporte no Windows XP com Service Pack 2 (SP2) e em versões posteriores de sistemas operacionais cliente Windows e no Windows Server 2003 com Service Pack 2 (SP2) e versões posteriores dos sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c45d5-128">.NET Framework 3.0 is supported on Windows XP with Service Pack 2 (SP2) and later versions of Windows client operating systems, and on Windows Server 2003 with Service Pack 2 (SP2) and later versions of Windows server operating systems.</span></span>

    <span data-ttu-id="c45d5-129">O .NET Framework 3,5 tem suporte em versões do Windows XP de sistemas operacionais cliente do Windows e no Windows Server 2003 e versões posteriores dos sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c45d5-129">.NET Framework 3.5 is supported on Windows XP versions of Windows client operating systems, and on Windows Server 2003 and later versions of Windows server operating systems.</span></span>

    > [!Note]  
    > <span data-ttu-id="c45d5-130">Recomendamos o uso de .NET Framework para criar documentos XPS somente em aplicativos cliente, não em aplicativos de servidor, a menos que o aplicativo saia periodicamente, como seria se fosse um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="c45d5-130">We recommend the use of .NET Framework for creating XPS documents in client applications only, not in server applications unless the application exits periodically, as it would if it were a client application.</span></span>

     

    <span data-ttu-id="c45d5-131">Para obter mais informações sobre o suporte a documentos no .NET Framework, consulte [Windows Presentation Foundation documentos](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c45d5-131">For more information about document support in .NET Framework, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="c45d5-132">Para trabalhar com documentos XPS em um programa, use a API de documento XPS nativo ou a .NET Framework; Não há suporte para o uso simultâneo de ambos no mesmo programa.</span><span class="sxs-lookup"><span data-stu-id="c45d5-132">To work with XPS documents in a program, use either the native XPS Document API or the .NET Framework; simultaneous use of both in the same program is not supported.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="c45d5-133">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c45d5-133">In This Section</span></span>

<span data-ttu-id="c45d5-134">Esta seção descreve as tecnologias de documento nativas do Windows com suporte no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c45d5-134">This section describes the native Windows document technologies that are supported by Microsoft Windows.</span></span>



| <span data-ttu-id="c45d5-135">Tecnologia de documentos</span><span class="sxs-lookup"><span data-stu-id="c45d5-135">Document technology</span></span>                                                                   | <span data-ttu-id="c45d5-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="c45d5-136">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c45d5-137">API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="c45d5-137">XPS Document API</span></span>](documents-xps.md)<br/>                   | <span data-ttu-id="c45d5-138">Fornece um formato confiável para o documento eletrônico.</span><span class="sxs-lookup"><span data-stu-id="c45d5-138">Provides a trustworthy format for electronic paper.</span></span><br/> <span data-ttu-id="c45d5-139">A API de documento XPS descrita nesta seção fornece aos programas e drivers de impressão XPSDrv acesso ao conteúdo e aos metadados de um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="c45d5-139">The XPS Document API that is described in this section gives programs and XPSDrv print drivers access to the content and metadata of an XPS document.</span></span><br/> |
| [<span data-ttu-id="c45d5-140">API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="c45d5-140">XPS Digital Signature API</span></span>](xps-digital-signatures.md)<br/> | <span data-ttu-id="c45d5-141">Habilita a assinatura de documentos, a verificação da identidade do signatário e a indicação de se um documento XPS foi alterado desde que foi assinado.</span><span class="sxs-lookup"><span data-stu-id="c45d5-141">Enables document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/>                                                                          |
| [<span data-ttu-id="c45d5-142">Glossário de documentos XPS</span><span class="sxs-lookup"><span data-stu-id="c45d5-142">XPS Documents Glossary</span></span>](xpsapi-glossary.md)<br/>           | <span data-ttu-id="c45d5-143">Definições de termos usados pela [API de documento XPS](documents-xps.md) e pela [API de assinatura digital XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="c45d5-143">Definitions of terms used by the [XPS Document API](documents-xps.md) and the [XPS Digital Signature API](xps-digital-signatures.md).</span></span><br/>                                                                              |



 

## <a name="xps-document-tools"></a><span data-ttu-id="c45d5-144">Ferramentas de documento XPS</span><span class="sxs-lookup"><span data-stu-id="c45d5-144">XPS Document Tools</span></span>

<span data-ttu-id="c45d5-145">As ferramentas a seguir estão disponíveis para ajudá-lo a testar e solucionar problemas de arquivos de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="c45d5-145">The following tools are available to assist you with testing and troubleshooting of XPS document files.</span></span>

-   <span data-ttu-id="c45d5-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="c45d5-146">[IsXPS](/previous-versions/aa348104(v=vs.110))</span></span>

    <span data-ttu-id="c45d5-147">Testa a conformidade de um arquivo com o XML Paper Specification (XPS) e a especificação do OPC (Open Packaging Conventions).</span><span class="sxs-lookup"><span data-stu-id="c45d5-147">Tests a file's conformity to the XML Paper Specification (XPS) and the Open Packaging Conventions (OPC) Specification.</span></span>

-   [<span data-ttu-id="c45d5-148">XpsAnalyzer</span><span class="sxs-lookup"><span data-stu-id="c45d5-148">XpsAnalyzer</span></span>](/windows-hardware/drivers/devtest/xpsanalyzer)

    <span data-ttu-id="c45d5-149">Uma ferramenta de prompt de comando que analisa arquivos de documento XPS para compatibilidade com a especificação XPS 1,0.</span><span class="sxs-lookup"><span data-stu-id="c45d5-149">A command-prompt tool that analyzes XPS document files for compatibility with the XPS 1.0 specification.</span></span>

-   <span data-ttu-id="c45d5-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c45d5-150">[PTConform](/previous-versions/dd327476(v=msdn.10))</span></span>

    <span data-ttu-id="c45d5-151">Uma ferramenta que verifica a validade de documentos PrintTicket e PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c45d5-151">A tool that checks the validity of PrintTicket and PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c45d5-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c45d5-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c45d5-153">API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="c45d5-153">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[<span data-ttu-id="c45d5-154">Empacotamento</span><span class="sxs-lookup"><span data-stu-id="c45d5-154">Packaging</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="c45d5-155">Impressão</span><span class="sxs-lookup"><span data-stu-id="c45d5-155">Printing</span></span>](./printdocs-printing.md)
</dt> <dt>
  
<span data-ttu-id="c45d5-156">[Imprimir programa de exemplo](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span><span class="sxs-lookup"><span data-stu-id="c45d5-156">[Print Sample Program](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))</span></span>
</dt> </dl>

 

