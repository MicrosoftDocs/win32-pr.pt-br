---
description: 'A propriedade time é a hora atual em horas, minutos e segundos como uma cadeia de caracteres de texto literal no formato HH: MM: SS usando um relógio de 24 horas.'
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Propriedade Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757376"
---
# <a name="time-property"></a><span data-ttu-id="3edf5-103">Propriedade Time</span><span class="sxs-lookup"><span data-stu-id="3edf5-103">Time property</span></span>

<span data-ttu-id="3edf5-104">A propriedade **time** é a hora atual em horas, minutos e segundos como uma cadeia de caracteres de texto literal no formato hh: mm: SS usando um relógio de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="3edf5-104">The **Time** property is the current time in hours, minutes, and seconds as a string of literal text in the format HH:MM:SS using a 24 hour clock.</span></span> <span data-ttu-id="3edf5-105">Por exemplo, a hora 6:57</span><span class="sxs-lookup"><span data-stu-id="3edf5-105">For example, the time 6:57 p.m.</span></span> <span data-ttu-id="3edf5-106">é representado por "18:57:00".</span><span class="sxs-lookup"><span data-stu-id="3edf5-106">is represented by "18:57:00".</span></span> <span data-ttu-id="3edf5-107">O formato do valor depende da localidade do usuário e é o formato obtido usando a função [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) com a \_ opção time FORCE24HOURFORMAT \| time \_ NOTIMEMARKER.</span><span class="sxs-lookup"><span data-stu-id="3edf5-107">The format of the value depends upon the user's locale, and is the format obtained using [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) function with the TIME\_FORCE24HOURFORMAT \| TIME\_NOTIMEMARKER option.</span></span> <span data-ttu-id="3edf5-108">O valor dessa propriedade é definido pelo Windows Installer e não pelo autor do pacote.</span><span class="sxs-lookup"><span data-stu-id="3edf5-108">The value of this property is set by the Windows Installer and not the package author.</span></span>

## <a name="remarks"></a><span data-ttu-id="3edf5-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3edf5-109">Remarks</span></span>

<span data-ttu-id="3edf5-110">Como essa é uma cadeia de caracteres de texto, ela não pode ser usada em expressões condicionais.</span><span class="sxs-lookup"><span data-stu-id="3edf5-110">Because this is a text string, it cannot be used in conditional expressions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3edf5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3edf5-111">Requirements</span></span>



| <span data-ttu-id="3edf5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3edf5-112">Requirement</span></span> | <span data-ttu-id="3edf5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3edf5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3edf5-114">Versão</span><span class="sxs-lookup"><span data-stu-id="3edf5-114">Version</span></span><br/> | <span data-ttu-id="3edf5-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3edf5-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3edf5-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3edf5-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3edf5-117">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3edf5-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3edf5-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3edf5-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3edf5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="3edf5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3edf5-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3edf5-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 
