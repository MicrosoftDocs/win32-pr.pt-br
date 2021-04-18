---
description: O instalador define a última propriedade de resumo salva por Summary com um valor que depende de se esse é um pacote de instalação, uma transformação ou um pacote de patch. Em um pacote de instalação, o instalador define essa propriedade como o valor da propriedade LogonUser durante uma instalação administrativa. Os desenvolvedores de ferramentas de edição de banco de dados podem usar essa propriedade durante o processo de desenvolvimento para acompanhar a última pessoa para modificar o banco de dados de instalação. Essa propriedade deve ser definida como NULL em um banco de dados de envio final. O instalador nunca usa essa propriedade e um usuário nunca precisa modificá-la. Em uma transformação, essa propriedade Summary contém a plataforma e as IDs de idioma que um banco de dados deve ter depois de ter sido transformado. A propriedade especifica para qual o resumo do modelo deve ser definido no novo banco de dados. Em um pacote de patch, essa propriedade de Resumo contém uma lista delimitada por ponto-e-vírgula dos nomes de subarmazenamento de transformação na ordem em que são aplicadas por esse patch.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Última gravação por propriedade de resumo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778566"
---
# <a name="last-saved-by-summary-property"></a><span data-ttu-id="15287-107">Última gravação por propriedade de resumo</span><span class="sxs-lookup"><span data-stu-id="15287-107">Last Saved By Summary property</span></span>

<span data-ttu-id="15287-108">O instalador define a **última propriedade de resumo salva por Summary** com um valor que depende de se esse é um pacote de instalação, uma transformação ou um pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="15287-108">The installer sets the **Last Saved by Summary** Property to a value that depends on whether this is an installation package, transform, or patch package.</span></span>

<span data-ttu-id="15287-109">Em um pacote de instalação, o instalador define essa propriedade como o valor da propriedade [**LogonUser**](logonuser.md) durante uma [instalação administrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="15287-109">In an installation package, the installer sets this property to the value of the [**LogonUser**](logonuser.md) property during an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="15287-110">Os desenvolvedores de ferramentas de edição de banco de dados podem usar essa propriedade durante o processo de desenvolvimento para acompanhar a última pessoa para modificar o banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="15287-110">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="15287-111">Essa propriedade deve ser definida como NULL em um banco de dados de envio final.</span><span class="sxs-lookup"><span data-stu-id="15287-111">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="15287-112">O instalador nunca usa essa propriedade e um usuário nunca precisa modificá-la.</span><span class="sxs-lookup"><span data-stu-id="15287-112">The installer never uses this property and a user never needs to modify it.</span></span>

<span data-ttu-id="15287-113">Em uma transformação, essa propriedade Summary contém a plataforma e as IDs de idioma que um banco de dados deve ter depois de ter sido transformado.</span><span class="sxs-lookup"><span data-stu-id="15287-113">In a transform, this summary property contains the platform and language ID(s) that a database should have after it has been transformed.</span></span> <span data-ttu-id="15287-114">A propriedade especifica para qual o [**Resumo do modelo**](template-summary.md) deve ser definido no novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="15287-114">The property specifies to what the [**Template Summary**](template-summary.md) should be set in the new database.</span></span>

<span data-ttu-id="15287-115">Em um pacote de patch, essa propriedade de Resumo contém uma lista delimitada por ponto-e-vírgula dos nomes de subarmazenamento de transformação na ordem em que são aplicadas por esse patch.</span><span class="sxs-lookup"><span data-stu-id="15287-115">In a patch package, this summary property contains a semicolon-delimited list of transform substorage names in the order they are applied by this patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="15287-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15287-116">Requirements</span></span>



| <span data-ttu-id="15287-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="15287-117">Requirement</span></span> | <span data-ttu-id="15287-118">Valor</span><span class="sxs-lookup"><span data-stu-id="15287-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15287-119">Versão</span><span class="sxs-lookup"><span data-stu-id="15287-119">Version</span></span><br/> | <span data-ttu-id="15287-120">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="15287-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="15287-121">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15287-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="15287-122">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="15287-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15287-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="15287-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15287-124">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="15287-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




