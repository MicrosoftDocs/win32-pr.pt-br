---
description: O método DVDAdm. SaveParentalLevel salva um novo nível de pai padrão no registro.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Método SaveParentalLevel (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768591"
---
# <a name="saveparentallevel-method"></a><span data-ttu-id="1028c-103">Método SaveParentalLevel</span><span class="sxs-lookup"><span data-stu-id="1028c-103">SaveParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="1028c-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1028c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1028c-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1028c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1028c-106">O método **DVDAdm. SaveParentalLevel** salva um novo nível de pai padrão no registro.</span><span class="sxs-lookup"><span data-stu-id="1028c-106">The **DVDAdm.SaveParentalLevel** method saves a new default parental level to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="1028c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1028c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1028c-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="1028c-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="1028c-109">Especifica o nível pai como valor de número inteiro de 1 a 8.</span><span class="sxs-lookup"><span data-stu-id="1028c-109">Specifies the parental level as anInteger value from 1 through 8.</span></span>

</dd> <dt>

<span data-ttu-id="1028c-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="1028c-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="1028c-111">Especifica o nome de usuário como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1028c-111">Specifies the user name as a String.</span></span> <span data-ttu-id="1028c-112">(Ignorado no momento.)</span><span class="sxs-lookup"><span data-stu-id="1028c-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="1028c-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="1028c-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="1028c-114">Especifica a senha como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1028c-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1028c-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1028c-115">Return Value</span></span>

<span data-ttu-id="1028c-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1028c-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1028c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1028c-117">Remarks</span></span>

<span data-ttu-id="1028c-118">Esse método permite que um usuário que conhece a senha atual salve uma nova configuração de nível pai no registro.</span><span class="sxs-lookup"><span data-stu-id="1028c-118">This method enables a user who knows the current password to save a new parental level setting to the registry.</span></span> <span data-ttu-id="1028c-119">Assim como acontece com todos os métodos de **MSDVDAdm**, esse método não afeta o nível atual no Player; Ele altera apenas a configuração do registro, de modo que, na próxima vez que o objeto MSWebDVD for iniciado, ele será aberto com o novo nível.</span><span class="sxs-lookup"><span data-stu-id="1028c-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is started, it will open with the new level.</span></span> <span data-ttu-id="1028c-120">Especifique-1 para desabilitar o gerenciamento de pais.</span><span class="sxs-lookup"><span data-stu-id="1028c-120">Specify -1 to disable parental management.</span></span> <span data-ttu-id="1028c-121">Para alterar o nível de pai no Player, chame [**SelectParentalLevel**](selectparentallevel-method.md), que não altera a configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="1028c-121">To change the parental level in the player, call [**SelectParentalLevel**](selectparentallevel-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="1028c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1028c-122">Requirements</span></span>



| <span data-ttu-id="1028c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1028c-123">Requirement</span></span> | <span data-ttu-id="1028c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1028c-124">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1028c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1028c-125">Header</span></span><br/> | <dl> <span data-ttu-id="1028c-126"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="1028c-126"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1028c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1028c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1028c-128">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="1028c-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




