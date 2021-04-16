---
description: A propriedade DefaultUIFont define o estilo de fonte padrão usado para controles. Para especificar o padrão, defina DefaultUIFont como um dos estilos predefinidos na tabela TextStyle na tabela de propriedades.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: Propriedade DefaultUIFont
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750008"
---
# <a name="defaultuifont-property"></a><span data-ttu-id="ea787-104">Propriedade DefaultUIFont</span><span class="sxs-lookup"><span data-stu-id="ea787-104">DefaultUIFont property</span></span>

<span data-ttu-id="ea787-105">A propriedade **DefaultUIFont** define o estilo de fonte padrão usado para controles.</span><span class="sxs-lookup"><span data-stu-id="ea787-105">The **DefaultUIFont** property sets the default font style used for controls.</span></span> <span data-ttu-id="ea787-106">Para especificar o padrão, defina **DefaultUIFont** como um dos estilos predefinidos na [tabela TextStyle](textstyle-table.md) na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="ea787-106">To specify the default, set **DefaultUIFont** to one of the predefined styles in the [TextStyle table](textstyle-table.md) in the [Property table](property-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea787-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea787-107">Remarks</span></span>

<span data-ttu-id="ea787-108">A propriedade **DefaultUIFont** de cada pacote de instalação com uma interface do usuário deve ser definida na [tabela de propriedades](property-table.md) para um dos estilos predefinidos listados na [tabela TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="ea787-108">The **DefaultUIFont** property of every installation package with a UI should be set in the [Property table](property-table.md) to one of the predefined styles listed in the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="ea787-109">Se essa propriedade não for especificada, o instalador usará a fonte do sistema.</span><span class="sxs-lookup"><span data-stu-id="ea787-109">If this property is not specified, the installer uses the System font.</span></span> <span data-ttu-id="ea787-110">Isso pode fazer com que o instalador exiba incorretamente cadeias de caracteres de texto quando a página de código do pacote for diferente da página de código padrão da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ea787-110">This can cause the installer to improperly display text strings when the package's code page is different from the user's default UI code page.</span></span>

<span data-ttu-id="ea787-111">O texto e o estilo de fonte de um controle podem ser definidos conforme descrito em [adicionando controles e texto](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="ea787-111">The text and font style of a control can be set as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="ea787-112">Se a cadeia de caracteres listada na coluna texto da [tabela de controle](control-table.md) ou da [tabela BBControl](bbcontrol-table.md) não especificar o estilo da fonte, o controle usará o valor da propriedade **DefaultUIFont** como o estilo da fonte.</span><span class="sxs-lookup"><span data-stu-id="ea787-112">If the character string listed in the Text column of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) does not specify the font style, the control uses the value of the **DefaultUIFont** property as the font style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea787-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea787-113">Requirements</span></span>



| <span data-ttu-id="ea787-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea787-114">Requirement</span></span> | <span data-ttu-id="ea787-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ea787-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea787-116">Versão</span><span class="sxs-lookup"><span data-stu-id="ea787-116">Version</span></span><br/> | <span data-ttu-id="ea787-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ea787-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ea787-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ea787-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ea787-119">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ea787-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ea787-120">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ea787-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ea787-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea787-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea787-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea787-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




