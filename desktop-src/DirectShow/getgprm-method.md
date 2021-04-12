---
description: O método GetGPRM recupera o registro de parâmetro geral especificado.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Método GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500615"
---
# <a name="getgprm-method"></a><span data-ttu-id="d1e4c-103">Método GetGPRM</span><span class="sxs-lookup"><span data-stu-id="d1e4c-103">GetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="d1e4c-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d1e4c-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d1e4c-106">O `GetGPRM` método recupera o registro de parâmetro geral especificado.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-106">The `GetGPRM` method retrieves the specified general parameter register.</span></span>

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="d1e4c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1e4c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e4c-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="d1e4c-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="d1e4c-109">Especifica o registro a ser recuperado como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-109">Specifies the register to retrieve as an Integer.</span></span> <span data-ttu-id="d1e4c-110">O valor deve variar de 0 a 15.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-110">The value must range from 0 through 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e4c-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d1e4c-111">Return Value</span></span>

<span data-ttu-id="d1e4c-112">Retorna um valor inteiro que representa o registro especificado.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-112">Returns an integer value representing the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1e4c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1e4c-113">Remarks</span></span>

<span data-ttu-id="d1e4c-114">Esse método não é necessário para qualquer funcionalidade de navegação ou reprodução de DVD usando o objeto **MSWebDVD** .</span><span class="sxs-lookup"><span data-stu-id="d1e4c-114">This method is not required for any DVD navigation or playback functionality using the **MSWebDVD** object.</span></span> <span data-ttu-id="d1e4c-115">Ele é fornecido para aqueles com uma compreensão completa da especificação de DVD que desejam implementar recursos avançados.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-115">It is provided for those with a thorough understanding of the DVD specification who want to implement advanced features.</span></span> <span data-ttu-id="d1e4c-116">GPRMs pode ser usado para armazenar quaisquer valores, para que possam ser configurados e lidos livremente.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-116">GPRMs can be used to hold any values, so they can be freely set and read.</span></span> <span data-ttu-id="d1e4c-117">Mas como GPRMs também são usadas para armazenar comandos de disco, alterar seus valores usando [**SetGPRM**](setgprm-method.md) pode resultar em um comportamento imprevisível.</span><span class="sxs-lookup"><span data-stu-id="d1e4c-117">But since GPRMs are used to store disc commands as well, changing their values using [**SetGPRM**](setgprm-method.md) can result in unpredictable behavior.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1e4c-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1e4c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e4c-119">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="d1e4c-119">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



