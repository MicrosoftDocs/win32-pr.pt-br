---
description: A propriedade date é o mês, o dia e o ano atuais como uma cadeia de caracteres de texto literal no formato MM/DD/AAAA.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Propriedade Date
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752856"
---
# <a name="date-property"></a><span data-ttu-id="41c0c-103">Propriedade Date</span><span class="sxs-lookup"><span data-stu-id="41c0c-103">Date property</span></span>

<span data-ttu-id="41c0c-104">A propriedade **Date** é o mês, o dia e o ano atuais como uma cadeia de caracteres de texto literal no formato mm/dd/aaaa.</span><span class="sxs-lookup"><span data-stu-id="41c0c-104">The **Date** property is the current month, day, and year as a string of literal text in the format MM/DD/YYYY.</span></span> <span data-ttu-id="41c0c-105">Por exemplo, a data 22 de junho de 2005 pode ser representada como "06/22/2005".</span><span class="sxs-lookup"><span data-stu-id="41c0c-105">For example, the date June 22, 2005 can represented as "06/22/2005".</span></span> <span data-ttu-id="41c0c-106">O formato do valor depende da localidade do usuário e é o formato obtido usando [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) com a \_ opção Date SHORTDATE.</span><span class="sxs-lookup"><span data-stu-id="41c0c-106">The format of the value depends upon the user's locale, and is the format obtained using [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) with the DATE\_SHORTDATE option.</span></span> <span data-ttu-id="41c0c-107">O valor dessa propriedade é definido pelo Windows Installer e não pelo autor do pacote.</span><span class="sxs-lookup"><span data-stu-id="41c0c-107">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="41c0c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="41c0c-108">Remarks</span></span>

<span data-ttu-id="41c0c-109">Como essa é uma cadeia de caracteres de texto, ela não pode ser usada em expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="41c0c-109">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c0c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c0c-110">Requirements</span></span>



| <span data-ttu-id="41c0c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c0c-111">Requirement</span></span> | <span data-ttu-id="41c0c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="41c0c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c0c-113">Versão</span><span class="sxs-lookup"><span data-stu-id="41c0c-113">Version</span></span><br/> | <span data-ttu-id="41c0c-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41c0c-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="41c0c-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="41c0c-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="41c0c-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="41c0c-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="41c0c-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="41c0c-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41c0c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="41c0c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c0c-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41c0c-119">Properties</span></span>](properties.md)
</dt> </dl>

 

