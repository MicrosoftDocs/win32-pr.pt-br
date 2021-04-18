---
description: Os tópicos nesta seção abordam a funcionalidade básica de fontes internacionais.
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: Gerenciamento de fontes internacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ade599577f97c696d3205e32bfaaca106ddaae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759664"
---
# <a name="international-font-management"></a><span data-ttu-id="aa7db-103">Gerenciamento de fontes internacionais</span><span class="sxs-lookup"><span data-stu-id="aa7db-103">International Font Management</span></span>

<span data-ttu-id="aa7db-104">Os tópicos nesta seção abordam a funcionalidade básica de fontes internacionais.</span><span class="sxs-lookup"><span data-stu-id="aa7db-104">The topics in this section address the basic functionality of International Fonts.</span></span> <span data-ttu-id="aa7db-105">Para obter instruções sobre como usar a tecnologia de fonte internacional em seus aplicativos, consulte [enumeração e seleção de fontes internacionais](using-international-fonts-and-text.md) e [usando MS Shell Dlg e MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).</span><span class="sxs-lookup"><span data-stu-id="aa7db-105">For instructions on using the international font technology in your applications, see [International Font Enumeration and Selection](using-international-fonts-and-text.md) and [Using MS Shell Dlg and MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md).</span></span>

## <a name="font-management-infrastructure"></a><span data-ttu-id="aa7db-106">Infraestrutura de gerenciamento de fontes</span><span class="sxs-lookup"><span data-stu-id="aa7db-106">Font Management Infrastructure</span></span>

<span data-ttu-id="aa7db-107">A partir do Windows 7, a infraestrutura de gerenciamento de fontes dá suporte à ocultação de fontes que não são apropriadas para listas de seleção de fontes de um usuário.</span><span class="sxs-lookup"><span data-stu-id="aa7db-107">Starting with Windows 7, the font management infrastructure supports the hiding of fonts which are not appropriate for a user's font selection lists.</span></span> <span data-ttu-id="aa7db-108">As configurações padrão do sistema optarão por ocultar automaticamente as fontes que não foram projetadas para os idiomas de entrada (teclados) habilitados no sistema do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="aa7db-108">The default system settings will choose to auto-hide fonts which are not designed for the input language(s) (keyboards) enabled on the OS system.</span></span> <span data-ttu-id="aa7db-109">Além disso, os usuários podem optar por ocultar manualmente as fontes no painel de controle fontes.</span><span class="sxs-lookup"><span data-stu-id="aa7db-109">In addition, users can choose to manually hide fonts in the Fonts Control Panel.</span></span> <span data-ttu-id="aa7db-110">Esse recurso significa que os usuários não precisam mais enfrentar listas longas de fontes inadequadas e são especialmente valiosos para usuários internacionais que trabalham em scripts não latinos.</span><span class="sxs-lookup"><span data-stu-id="aa7db-110">This feature means users need no longer be faced with long lists of inappropriate fonts, and is particularly valuable for international users working in non-Latin scripts.</span></span>

<span data-ttu-id="aa7db-111">No Windows 7, não há APIs para consultar diretamente quais fontes estão ocultas ou para definir fontes como ocultas.</span><span class="sxs-lookup"><span data-stu-id="aa7db-111">In Windows 7, there are no APIs for directly querying which fonts are hidden, or for setting fonts to be hidden.</span></span> <span data-ttu-id="aa7db-112">No entanto, isso não significa que você não possa aproveitar esse recurso em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa7db-112">However, this does not mean you cannot take advantage of this feature in your application.</span></span> <span data-ttu-id="aa7db-113">Se você usar a API [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) do Windows (caixa de diálogo de fonte comum) para habilitar a seleção de fontes hoje, você obterá o novo comportamento gratuitamente.</span><span class="sxs-lookup"><span data-stu-id="aa7db-113">If you use the Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) API (Font common dialog) to enable font selection today, you will get the new behavior for free.</span></span> <span data-ttu-id="aa7db-114">A nova faixa de Cenários do Windows (controles de fonte) introduzida no Windows 7 também dá suporte a esse comportamento e fornece outro motivo para "Ribbonar" seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="aa7db-114">The new Windows Scenic Ribbon (Font Controls) introduced in Windows 7 also supports this behavior and provides another reason to "Ribbonize" your applications.</span></span> <span data-ttu-id="aa7db-115">Para obter detalhes sobre como usar os controles de fonte na faixa de opção e **ChooseFont** para exibir fontes ao filtrar as fontes ocultas, consulte a [enumeração e a seleção de fontes internacionais](using-international-fonts-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="aa7db-115">For details of using Font Controls in Ribbon and **ChooseFont** to display fonts while filtering out the hidden fonts, please reference [International Font Enumeration and Selection](using-international-fonts-and-text.md).</span></span>

<span data-ttu-id="aa7db-116">Observe que ocultar fontes afeta apenas a interface do usuário de seleção de fontes.</span><span class="sxs-lookup"><span data-stu-id="aa7db-116">Note that hiding fonts only impacts font selection UI.</span></span> <span data-ttu-id="aa7db-117">Ele não afeta as APIs de desenho.</span><span class="sxs-lookup"><span data-stu-id="aa7db-117">It does not impact drawing APIs.</span></span> <span data-ttu-id="aa7db-118">Quando uma fonte é selecionada em um contexto de dispositivo, não há nenhum efeito no desenho devido à fonte que está sendo ocultada.</span><span class="sxs-lookup"><span data-stu-id="aa7db-118">When a font is selected into a device context, there is no effect on drawing due to the font being hidden.</span></span> <span data-ttu-id="aa7db-119">A função [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) continua enumerando fontes definidas como ocultas.</span><span class="sxs-lookup"><span data-stu-id="aa7db-119">The [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) function continues to enumerate fonts that are set to hidden.</span></span>

## <a name="gdi-font-embedding-and-subsetting"></a><span data-ttu-id="aa7db-120">Incorporação e subconfiguração de fonte GDI</span><span class="sxs-lookup"><span data-stu-id="aa7db-120">GDI Font Embedding and Subsetting</span></span>

<span data-ttu-id="aa7db-121">A tecnologia de fontes internacionais usa a biblioteca de serviços de inserção de fontes para permitir que você agrupe fontes TrueType e OpenType em um documento ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa7db-121">International Fonts technology makes use of the Font Embedding Services Library to allow you to bundle TrueType and OpenType fonts into a document or file.</span></span> <span data-ttu-id="aa7db-122">A inserção de uma fonte em um arquivo garante que a fonte estará presente no computador que está recebendo o arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa7db-122">Embedding a font in a file guarantees that the font will be present on the computer receiving the file.</span></span> <span data-ttu-id="aa7db-123">Para obter mais informações, consulte [referência de inserção de fonte](../gdi/font-embedding-reference.md).</span><span class="sxs-lookup"><span data-stu-id="aa7db-123">For more information, see [Font Embedding Reference](../gdi/font-embedding-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa7db-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa7db-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa7db-125">Seleção e enumeração de fontes internacionais</span><span class="sxs-lookup"><span data-stu-id="aa7db-125">International Font Enumeration and Selection</span></span>](using-international-fonts-and-text.md)
</dt> <dt>

[<span data-ttu-id="aa7db-126">Usando MS Shell Dlg e MS Shell Dlg 2</span><span class="sxs-lookup"><span data-stu-id="aa7db-126">Using MS Shell Dlg and MS Shell Dlg 2</span></span>](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[<span data-ttu-id="aa7db-127">Referência de incorporação de fonte</span><span class="sxs-lookup"><span data-stu-id="aa7db-127">Font Embedding Reference</span></span>](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
