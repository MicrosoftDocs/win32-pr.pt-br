---
description: A propriedade AnglesAvailable recupera o número de ângulos disponíveis no momento.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Propriedade AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105749645"
---
# <a name="anglesavailable-property"></a><span data-ttu-id="28b07-103">Propriedade AnglesAvailable</span><span class="sxs-lookup"><span data-stu-id="28b07-103">AnglesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="28b07-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="28b07-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="28b07-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="28b07-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="28b07-106">A `AnglesAvailable` propriedade recupera o número de ângulos disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="28b07-106">The `AnglesAvailable` property retrieves the number of angles currently available.</span></span>

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a><span data-ttu-id="28b07-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="28b07-107">Return Value</span></span>

<span data-ttu-id="28b07-108">Retorna um valor inteiro de 1 a 9 que representa o número de ângulos disponíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="28b07-108">Returns an integer value from 1 through 9 representing the number of angles currently available.</span></span> <span data-ttu-id="28b07-109">If</span><span class="sxs-lookup"><span data-stu-id="28b07-109">If</span></span>


```
iAngles
```



<span data-ttu-id="28b07-110">= 1, não há nenhum bloco de ângulo no local atual.</span><span class="sxs-lookup"><span data-stu-id="28b07-110">= 1, there is no angle block at the current location.</span></span>

## <a name="remarks"></a><span data-ttu-id="28b07-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="28b07-111">Remarks</span></span>

<span data-ttu-id="28b07-112">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="28b07-112">This property is read-only with no default value.</span></span> <span data-ttu-id="28b07-113">Um *bloco de ângulo* é um segmento de vídeo que foi capturado de mais de um ângulo de câmera.</span><span class="sxs-lookup"><span data-stu-id="28b07-113">An *angle block* is a video segment that was shot from more than one camera angle.</span></span> <span data-ttu-id="28b07-114">Pode haver até nove ângulos em um bloco de ângulo, numerados de 1 a 9.</span><span class="sxs-lookup"><span data-stu-id="28b07-114">There can be up to nine angles in an angle block, numbered from 1 through 9.</span></span> <span data-ttu-id="28b07-115">Quando o navegador de DVD entra primeiro em um bloco de ângulo, ele envia ao aplicativo uma \_ notificação de evento de ângulos de DVD EC \_ \_ disponíveis com o número de ângulos em *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="28b07-115">When the DVD Navigator first enters an angle block, it sends your application an EC\_DVD\_ANGLES\_AVAILABLE event notification with the number of angles in *lParam1*.</span></span> <span data-ttu-id="28b07-116">Um disco pode ser criado para mostrar automaticamente um menu para os ângulos disponíveis quando ele entra em um bloco de ângulo, mas geralmente um aplicativo deve determinar o número de ângulos disponíveis e oferecer ao usuário uma maneira de selecionar um.</span><span class="sxs-lookup"><span data-stu-id="28b07-116">A disc can be authored to automatically show a menu for available angles when it enters an angle block, but generally an application must determine the number of angles available and offer the user a way to select one.</span></span>

## <a name="see-also"></a><span data-ttu-id="28b07-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="28b07-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28b07-118">**CurrentAngle**</span><span class="sxs-lookup"><span data-stu-id="28b07-118">**CurrentAngle**</span></span>](currentangle-property.md)
</dt> </dl>

 

 



