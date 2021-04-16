---
description: A propriedade Resumo de segurança transmite se o pacote deve ser aberto como somente leitura.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Propriedade de Resumo de segurança
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750218"
---
# <a name="security-summary-property"></a><span data-ttu-id="c691a-103">Propriedade de Resumo de segurança</span><span class="sxs-lookup"><span data-stu-id="c691a-103">Security Summary property</span></span>

<span data-ttu-id="c691a-104">A propriedade **Resumo de segurança** transmite se o pacote deve ser aberto como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c691a-104">The **Security Summary** property conveys whether the package should be opened as read-only.</span></span> <span data-ttu-id="c691a-105">A ferramenta de edição de banco de dados não deve modificar um banco de dados imposto somente leitura e emitir um aviso em tentativas de modificar um banco de dados recomendado somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c691a-105">The database editing tool should not modify a read-only enforced database and should issue a warning at attempts to modify a read-only recommended database.</span></span> <span data-ttu-id="c691a-106">Os seguintes valores dessa propriedade são aplicáveis a Windows Installer arquivos.</span><span class="sxs-lookup"><span data-stu-id="c691a-106">The following values of this property are applicable to Windows Installer files.</span></span>



| <span data-ttu-id="c691a-107">Valor</span><span class="sxs-lookup"><span data-stu-id="c691a-107">Value</span></span> | <span data-ttu-id="c691a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c691a-108">Description</span></span>           |
|-------|-----------------------|
| <span data-ttu-id="c691a-109">0</span><span class="sxs-lookup"><span data-stu-id="c691a-109">0</span></span>     | <span data-ttu-id="c691a-110">Nenhuma restrição</span><span class="sxs-lookup"><span data-stu-id="c691a-110">No restriction</span></span>        |
| <span data-ttu-id="c691a-111">2</span><span class="sxs-lookup"><span data-stu-id="c691a-111">2</span></span>     | <span data-ttu-id="c691a-112">Somente leitura recomendado</span><span class="sxs-lookup"><span data-stu-id="c691a-112">Read-only recommended</span></span> |
| <span data-ttu-id="c691a-113">4</span><span class="sxs-lookup"><span data-stu-id="c691a-113">4</span></span>     | <span data-ttu-id="c691a-114">Imposto somente leitura</span><span class="sxs-lookup"><span data-stu-id="c691a-114">Read-only enforced</span></span>    |



 

<span data-ttu-id="c691a-115">Essa propriedade deve ser definida como somente leitura recomendado (2) para um banco de dados de instalação e para somente leitura (4) para uma transformação ou patch.</span><span class="sxs-lookup"><span data-stu-id="c691a-115">This property should be set to read-only recommended (2) for an installation database and to read-only enforced (4) for a transform or patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="c691a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c691a-116">Requirements</span></span>



| <span data-ttu-id="c691a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c691a-117">Requirement</span></span> | <span data-ttu-id="c691a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c691a-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c691a-119">Versão</span><span class="sxs-lookup"><span data-stu-id="c691a-119">Version</span></span><br/> | <span data-ttu-id="c691a-120">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c691a-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c691a-121">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c691a-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c691a-122">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c691a-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c691a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c691a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c691a-124">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="c691a-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




