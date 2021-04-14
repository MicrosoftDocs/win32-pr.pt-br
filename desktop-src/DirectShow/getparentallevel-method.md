---
description: O método DVDAdm. GetParentalLevel recupera o nível pai que foi salvo pela última vez no registro.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Método GetParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370069"
---
# <a name="getparentallevel-method"></a><span data-ttu-id="69ee7-103">Método GetParentalLevel</span><span class="sxs-lookup"><span data-stu-id="69ee7-103">GetParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="69ee7-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="69ee7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="69ee7-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="69ee7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="69ee7-106">O `DVDAdm.GetParentalLevel` método recupera o nível pai que foi salvo pela última vez no registro.</span><span class="sxs-lookup"><span data-stu-id="69ee7-106">The `DVDAdm.GetParentalLevel` method retrieves the parental level that was last saved to the registry.</span></span>

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="69ee7-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="69ee7-107">Return Value</span></span>

<span data-ttu-id="69ee7-108">Retorna um inteiro de 1 a 8 indicando o nível pai padrão.</span><span class="sxs-lookup"><span data-stu-id="69ee7-108">Returns an Integer from 1 through 8 indicating the default parental level.</span></span>

## <a name="remarks"></a><span data-ttu-id="69ee7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="69ee7-109">Remarks</span></span>

<span data-ttu-id="69ee7-110">O nível pai que esse método recupera não é necessariamente o mesmo nível atualmente armazenado no controle MSWebDVD; para obter o nível atualmente armazenado no controle, chame o método [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) .</span><span class="sxs-lookup"><span data-stu-id="69ee7-110">The parental level this method retrieves is not necessarily the same level currently stored in the MSWebDVD control; to get the level currently stored in the control, call the [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) method.</span></span> <span data-ttu-id="69ee7-111">Um valor de-1 indica que o gerenciamento de pais está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="69ee7-111">A value of -1 indicates that parental management is disabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="69ee7-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="69ee7-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ee7-113">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="69ee7-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



