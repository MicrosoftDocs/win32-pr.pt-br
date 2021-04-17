---
description: O método DVDAdm. ChangePassword salva uma nova senha de aplicativo no registro.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: Método ChangePassword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456452"
---
# <a name="changepassword-method"></a><span data-ttu-id="d2680-103">Método ChangePassword</span><span class="sxs-lookup"><span data-stu-id="d2680-103">ChangePassword Method</span></span>

> [!Note]  
> <span data-ttu-id="d2680-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d2680-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d2680-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="d2680-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d2680-106">O `DVDAdm.ChangePassword` método salva uma nova senha de aplicativo no registro.</span><span class="sxs-lookup"><span data-stu-id="d2680-106">The `DVDAdm.ChangePassword` method saves a new application password in the registry.</span></span>

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a><span data-ttu-id="d2680-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2680-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2680-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="d2680-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="d2680-109">Especifica o nome de logon do usuário atual como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2680-109">Specifies the current user's logon name as a String.</span></span> <span data-ttu-id="d2680-110">O objeto MSDVDAdm ignora esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d2680-110">The MSDVDAdm object ignores this parameter.</span></span> <span data-ttu-id="d2680-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="d2680-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d2680-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Gota*</span><span class="sxs-lookup"><span data-stu-id="d2680-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*sOld*</span></span>
</dt> <dd>

<span data-ttu-id="d2680-113">Especifica a senha antiga do usuário como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2680-113">Specifies the user's old password as a String.</span></span>

</dd> <dt>

<span data-ttu-id="d2680-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span><span class="sxs-lookup"><span data-stu-id="d2680-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span></span>
</dt> <dd>

<span data-ttu-id="d2680-115">Especifica a nova senha do usuário como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2680-115">Specifies the user's new password as a String.</span></span> <span data-ttu-id="d2680-116">Não pode ser uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="d2680-116">Cannot be an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2680-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d2680-117">Return Value</span></span>

<span data-ttu-id="d2680-118">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d2680-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2680-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2680-119">Remarks</span></span>

<span data-ttu-id="d2680-120">Atualmente, o parâmetro *sUserName* é ignorado neste e em todos os métodos relacionados.</span><span class="sxs-lookup"><span data-stu-id="d2680-120">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span> <span data-ttu-id="d2680-121">Isso significa que quem sabe que a senha pode definir o nível de pais.</span><span class="sxs-lookup"><span data-stu-id="d2680-121">This means that whoever knows the password can set the parental level.</span></span> <span data-ttu-id="d2680-122">Há apenas uma senha e um nível de pai para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d2680-122">There is only one password and one parental level for the application.</span></span> <span data-ttu-id="d2680-123">Não há suporte para nomes de logon de usuário individuais ou para o gerenciamento de várias senhas.</span><span class="sxs-lookup"><span data-stu-id="d2680-123">There is no support for individual user logon names or multiple password management.</span></span> <span data-ttu-id="d2680-124">Para impor os níveis de gerenciamento dos pais, os pais devem definir a senha e, em seguida, definir o nível pai apropriado para membros mais jovens do grupo de parentes.</span><span class="sxs-lookup"><span data-stu-id="d2680-124">To enforce parental management levels, parents should set the password and then set the parental level appropriate for younger members of the group of relatives.</span></span> <span data-ttu-id="d2680-125">Quando os pais desejam exibir um disco com conteúdo classificado como adulto, eles podem alterar o nível e, em seguida, alterá-lo novamente quando terminarem de ser exibidos.</span><span class="sxs-lookup"><span data-stu-id="d2680-125">When parents want to view a disc with adult-rated content, they can change the level, and then change it back when they are done viewing.</span></span> <span data-ttu-id="d2680-126">Desde que os filhos não saibam a senha, eles só podem ver o conteúdo no nível definido ou abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="d2680-126">As long as the children do not know the password, they can only watch content at or below the level set for them.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2680-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2680-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2680-128">**ConfirmPassword**</span><span class="sxs-lookup"><span data-stu-id="d2680-128">**ConfirmPassword**</span></span>](confirmpassword-method.md)
</dt> <dt>

[<span data-ttu-id="d2680-129">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="d2680-129">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



