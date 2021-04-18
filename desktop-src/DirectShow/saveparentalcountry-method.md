---
description: O método DVDAdm. SaveParentalCountry salva o novo país/região pai do aplicativo no registro.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Método SaveParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767669"
---
# <a name="saveparentalcountry-method"></a><span data-ttu-id="17f16-103">Método SaveParentalCountry</span><span class="sxs-lookup"><span data-stu-id="17f16-103">SaveParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="17f16-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="17f16-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="17f16-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="17f16-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="17f16-106">O `DVDAdm.SaveParentalCountry` método salva o novo país/região pai do aplicativo no registro.</span><span class="sxs-lookup"><span data-stu-id="17f16-106">The `DVDAdm.SaveParentalCountry` method saves the application's new parental country/region to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="17f16-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17f16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17f16-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="17f16-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="17f16-109">Especifica o país/região pai como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="17f16-109">Specifies the parental country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="17f16-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="17f16-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="17f16-111">Especifica o nome de usuário como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="17f16-111">Specifies the user name as a String.</span></span> <span data-ttu-id="17f16-112">(Ignorado no momento.)</span><span class="sxs-lookup"><span data-stu-id="17f16-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="17f16-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="17f16-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="17f16-114">Especifica a senha como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="17f16-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17f16-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17f16-115">Return value</span></span>

<span data-ttu-id="17f16-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="17f16-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17f16-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="17f16-117">Remarks</span></span>

<span data-ttu-id="17f16-118">Esse método permite que um usuário que conhece a senha atual salve uma nova configuração de país/região pai no registro.</span><span class="sxs-lookup"><span data-stu-id="17f16-118">This method enables a user who knows the current password to save a new parental country/region setting to the registry.</span></span> <span data-ttu-id="17f16-119">Assim como acontece com todos os métodos de **MSDVDAdm**, esse método não afeta o nível atual no Player; Ele altera apenas a configuração do registro, de modo que, na próxima vez que o objeto MSWebDVD for criado, ele será aberto com o novo país/região.</span><span class="sxs-lookup"><span data-stu-id="17f16-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is created, it will open with the new country/region.</span></span> <span data-ttu-id="17f16-120">Para alterar o país/região pai no Player, chame [**SelectParentalCountry**](selectparentalcountry-method.md), que não altera a configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="17f16-120">To change the parental country/region in the player, call [**SelectParentalCountry**](selectparentalcountry-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="17f16-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17f16-121">Requirements</span></span>



| <span data-ttu-id="17f16-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="17f16-122">Requirement</span></span> | <span data-ttu-id="17f16-123">Valor</span><span class="sxs-lookup"><span data-stu-id="17f16-123">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="17f16-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17f16-124">Header</span></span><br/> | <dl> <span data-ttu-id="17f16-125"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="17f16-125"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17f16-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="17f16-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f16-127">**SaveParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="17f16-127">**SaveParentalLevel**</span></span>](saveparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="17f16-128">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="17f16-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




