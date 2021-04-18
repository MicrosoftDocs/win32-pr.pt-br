---
description: A propriedade de resumo contagem de caracteres só é usada em transformações.
ms.assetid: d26d24a5-558e-4333-ae39-ffba1bbc5247
title: Propriedade de resumo contagem de caracteres
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afc99c065721f0f0b94691a12e00204305940efd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756905"
---
# <a name="character-count-summary-property"></a><span data-ttu-id="5838e-103">Propriedade de resumo contagem de caracteres</span><span class="sxs-lookup"><span data-stu-id="5838e-103">Character Count Summary property</span></span>

<span data-ttu-id="5838e-104">A propriedade de **Resumo contagem de caracteres** só é usada em transformações.</span><span class="sxs-lookup"><span data-stu-id="5838e-104">The **Character Count Summary** property is only used in transforms.</span></span> <span data-ttu-id="5838e-105">Essa parte do fluxo de informações de resumo é dividida em palavras de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5838e-105">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="5838e-106">A palavra superior contém os [*sinalizadores de validação de transformação*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5838e-106">The upper word contains the [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="5838e-107">A palavra inferior contém os [*sinalizadores de condição de erro de transformação*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5838e-107">The lower word contains the [*transform error condition flags*](t-gly.md).</span></span>

<span data-ttu-id="5838e-108">Essa propriedade deve ser nula em um pacote de instalação ou em um pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="5838e-108">This property should be Null in an installation package or patch package.</span></span>

## <a name="requirements"></a><span data-ttu-id="5838e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5838e-109">Requirements</span></span>



| <span data-ttu-id="5838e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5838e-110">Requirement</span></span> | <span data-ttu-id="5838e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5838e-111">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5838e-112">Versão</span><span class="sxs-lookup"><span data-stu-id="5838e-112">Version</span></span><br/> | <span data-ttu-id="5838e-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5838e-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5838e-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5838e-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5838e-115">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5838e-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5838e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="5838e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5838e-117">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="5838e-117">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




