---
description: A propriedade PATCHNEWPACKAGECODE atualiza a propriedade Resumo do número de revisão de uma imagem administrativa durante a aplicação de patch.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Propriedade PATCHNEWPACKAGECODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756897"
---
# <a name="patchnewpackagecode-property"></a><span data-ttu-id="0b59e-103">Propriedade PATCHNEWPACKAGECODE</span><span class="sxs-lookup"><span data-stu-id="0b59e-103">PATCHNEWPACKAGECODE property</span></span>

<span data-ttu-id="0b59e-104">A propriedade **PATCHNEWPACKAGECODE** atualiza a propriedade [**Resumo do número de revisão**](revision-number-summary.md) de uma imagem administrativa durante a aplicação de patch.</span><span class="sxs-lookup"><span data-stu-id="0b59e-104">The **PATCHNEWPACKAGECODE** property updates the [**Revision Number Summary**](revision-number-summary.md) property of an administrative image during patching.</span></span> <span data-ttu-id="0b59e-105">Essa propriedade só é definida por uma transformação em um arquivo. msp.</span><span class="sxs-lookup"><span data-stu-id="0b59e-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="0b59e-106">O arquivo. msp deve incluir uma transformação que adiciona essa propriedade à [tabela de propriedades](property-table.md) e define seu valor.</span><span class="sxs-lookup"><span data-stu-id="0b59e-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="0b59e-107">Em seguida, o instalador grava o valor de **PATCHNEWPACKAGECODE** na propriedade **Summary do número de revisão** .</span><span class="sxs-lookup"><span data-stu-id="0b59e-107">The installer then writes the value of **PATCHNEWPACKAGECODE** to the **Revision Number Summary** property.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b59e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b59e-108">Remarks</span></span>

<span data-ttu-id="0b59e-109">As propriedades **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)e [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) são usadas para atualizar as informações de resumo quando um patch é instalado em uma imagem administrativa.</span><span class="sxs-lookup"><span data-stu-id="0b59e-109">The **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md), and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b59e-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b59e-110">Requirements</span></span>



| <span data-ttu-id="0b59e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b59e-111">Requirement</span></span> | <span data-ttu-id="0b59e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0b59e-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b59e-113">Versão</span><span class="sxs-lookup"><span data-stu-id="0b59e-113">Version</span></span><br/> | <span data-ttu-id="0b59e-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b59e-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0b59e-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0b59e-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0b59e-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b59e-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="0b59e-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0b59e-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b59e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b59e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b59e-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b59e-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




