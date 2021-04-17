---
description: O Microsoft XPS Document Writer (MXDW) é um driver de impressão para arquivo que permite que um aplicativo do Windows Crie arquivos de documento XPS (XML Paper Specification) em versões do Windows a partir do Windows XP com Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Gravador de documento XPS da Microsoft (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760989"
---
# <a name="microsoft-xps-document-writer-mxdw"></a><span data-ttu-id="688e0-103">Gravador de documento XPS da Microsoft (MXDW)</span><span class="sxs-lookup"><span data-stu-id="688e0-103">Microsoft XPS Document Writer (MXDW)</span></span>

<span data-ttu-id="688e0-104">O Microsoft XPS Document Writer (MXDW) é um driver de impressão para arquivo que permite que um aplicativo do Windows Crie arquivos de documento XPS (XML Paper Specification) em versões do Windows a partir do Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="688e0-104">The Microsoft XPS Document Writer (MXDW) is a print-to-file driver that enables a Windows application to create XML Paper Specification (XPS) document files on versions of Windows starting with Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="688e0-105">Usar o MXDW possibilita que um aplicativo do Windows salve seu conteúdo como um documento XPS sem alterar qualquer código do programa do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="688e0-105">Using the MXDW makes it possible for a Windows application to save its content as an XPS document without changing any of the application's program code.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="688e0-106">Quando usar</span><span class="sxs-lookup"><span data-stu-id="688e0-106">When to Use</span></span>

<span data-ttu-id="688e0-107">Como usuário, você deve selecionar o MXDW quando quiser criar um documento XPS a partir de um aplicativo do Windows que não tem a opção de salvar seu conteúdo como um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="688e0-107">As a user, you would select the MXDW when you want to create an XPS document from a Windows application that does not have the option to save its content as an XPS document.</span></span>

<span data-ttu-id="688e0-108">Como desenvolvedor de aplicativos, você recomendaria o MXDW a usuários que desejam criar documentos XPS quando seu aplicativo não oferecer a opção de salvar como um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="688e0-108">As an application developer, you would recommend the MXDW to users who want to create XPS documents when your application does not offer the option to save as an XPS document.</span></span> <span data-ttu-id="688e0-109">Para obter mais informações sobre a especificação de papel XML e documentos XPS, consulte [especificação de documento XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) e a [especificação XPS e downloads de licenças](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="688e0-109">For more information on the XML Paper Specification and XPS documents, see [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) and [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

<span data-ttu-id="688e0-110">O MXDW é instalado automaticamente no Windows Vista e em versões posteriores do Windows e pode ser baixado e instalado no Windows XP com SP2 e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="688e0-110">The MXDW is installed automatically on Windows Vista and later versions of Windows and can be downloaded and installed on Windows XP with SP2 and Windows Server 2003.</span></span>

## <a name="installation"></a><span data-ttu-id="688e0-111">Instalação</span><span class="sxs-lookup"><span data-stu-id="688e0-111">Installation</span></span>

<span data-ttu-id="688e0-112">No Windows Vista e versões posteriores do Windows, o MXDW é instalado automaticamente quando o sistema operacional é instalado.</span><span class="sxs-lookup"><span data-stu-id="688e0-112">On Windows Vista and later versions of Windows, the MXDW is installed automatically when the operating system is installed.</span></span>

<span data-ttu-id="688e0-113">**Windows XP com SP2 e Windows Server 2003**: Baixe e instale o .net Framework 3,0 ou o pacote XPS Essential do [centro de download da Microsoft](https://www.microsoft.com/downloads/en/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="688e0-113">**Windows XP with SP2 and Windows Server 2003**: Download and install either .Net Framework 3.0 or the XPS Essential Pack from the [Microsoft Download Center](https://www.microsoft.com/downloads/en/default.aspx).</span></span>

## <a name="how-to-use"></a><span data-ttu-id="688e0-114">Como usar</span><span class="sxs-lookup"><span data-stu-id="688e0-114">How to Use</span></span>

<span data-ttu-id="688e0-115">Quando instalado, o MXDW aparece como uma fila de impressão disponível na caixa de diálogo Imprimir apresentada por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="688e0-115">When installed, the MXDW appears as an available print queue in the Print dialog box presented by an application.</span></span> <span data-ttu-id="688e0-116">Quando o MXDW é selecionado como a impressora, é solicitado que o nome do arquivo seja criado como o documento XPS que captura a saída de impressão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="688e0-116">When the MXDW is selected as the printer, the user is prompted for the file name to create as the XPS Document that captures the print output of the application.</span></span>

<span data-ttu-id="688e0-117">A imagem a seguir mostra o MXDW que está sendo selecionado como a impressora na caixa de diálogo impressão comum do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="688e0-117">The following image shows the MXDW being selected as the printer in the Windows Vista common print dialog box.</span></span>

![uma imagem da caixa de diálogo de impressão que mostra a seleção do Microsoft XPS Document Writer (MXDW)](images/choosingmxdwinvista.gif)

<span data-ttu-id="688e0-119">Os desenvolvedores de aplicativos podem personalizar a saída de MXDW usando as [definições de configuração do MXDW](mxdw-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="688e0-119">Application developers can customize the output of MXDW using the [MXDW configuration settings](mxdw-configuration-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="688e0-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="688e0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="688e0-121">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="688e0-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="688e0-122">Downloads de licença e de especificação XPS</span><span class="sxs-lookup"><span data-stu-id="688e0-122">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

<span data-ttu-id="688e0-123">[Ferramenta de conformidade do isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="688e0-123">[isXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="688e0-124">Definições de configuração do MXDW</span><span class="sxs-lookup"><span data-stu-id="688e0-124">MXDW configuration settings</span></span>](mxdw-configuration-settings.md)
</dt> </dl>

 

 
