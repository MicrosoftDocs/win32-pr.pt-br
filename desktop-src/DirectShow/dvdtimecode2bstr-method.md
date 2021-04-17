---
description: O método DVDTimeCode2bstr recupera uma cadeia de caracteres que indica a hora atual no disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Método DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759557"
---
# <a name="dvdtimecode2bstr-method"></a><span data-ttu-id="c5b82-103">Método DVDTimeCode2bstr</span><span class="sxs-lookup"><span data-stu-id="c5b82-103">DVDTimeCode2bstr Method</span></span>

> [!Note]  
> <span data-ttu-id="c5b82-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c5b82-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c5b82-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c5b82-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c5b82-106">O `DVDTimeCode2bstr` método recupera uma cadeia de caracteres que indica a hora atual no disco.</span><span class="sxs-lookup"><span data-stu-id="c5b82-106">The `DVDTimeCode2bstr` method retrieves a string indicating the current time on the disc.</span></span>

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a><span data-ttu-id="c5b82-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5b82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b82-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span><span class="sxs-lookup"><span data-stu-id="c5b82-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="c5b82-109">Especifica a hora atual no disco em relação ao início do título como um número obtido por meio do evento [**de \_ \_ \_ \_ hora HMSF atual do DVD do EC**](ec-dvd-current-hmsf-time.md) .</span><span class="sxs-lookup"><span data-stu-id="c5b82-109">Specifies the current time on the disc relative to the start of the title as a Number obtained through the [**EC\_DVD\_CURRENT\_HMSF\_TIME**](ec-dvd-current-hmsf-time.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b82-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c5b82-110">Return Value</span></span>

<span data-ttu-id="c5b82-111">Retorna uma cadeia de caracteres de 11 caracteres no formato "hh: mm: SS: FF" que representa as horas, os minutos, os segundos e os quadros que definem a hora atual.</span><span class="sxs-lookup"><span data-stu-id="c5b82-111">Returns an 11-character String in the format "hh:mm:ss:ff" representing the hours, minutes, seconds and frames that define the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5b82-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5b82-112">Remarks</span></span>

<span data-ttu-id="c5b82-113">Este método é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c5b82-113">This method is read only.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5b82-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5b82-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b82-115">Manipulando notificações de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="c5b82-115">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



