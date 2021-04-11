---
description: A propriedade DVDAdm. DefaultMenuLCID define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para menus.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propriedade DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087824"
---
# <a name="defaultmenulcid-property"></a><span data-ttu-id="deeb8-103">Propriedade DefaultMenuLCID</span><span class="sxs-lookup"><span data-stu-id="deeb8-103">DefaultMenuLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="deeb8-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="deeb8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="deeb8-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="deeb8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="deeb8-106">A `DVDAdm.DefaultMenuLCID` propriedade define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para menus.</span><span class="sxs-lookup"><span data-stu-id="deeb8-106">The `DVDAdm.DefaultMenuLCID` property sets or retrieves the registry setting for the user-specified default LCID for menus.</span></span>

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a><span data-ttu-id="deeb8-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="deeb8-107">Return Value</span></span>

<span data-ttu-id="deeb8-108">Retorna um valor inteiro que representa o LCID como armazenado nas configurações do registro para o aplicativo de DVD.</span><span class="sxs-lookup"><span data-stu-id="deeb8-108">Returns an Integer value representing the LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="deeb8-109">Esse valor não é necessariamente o mesmo que o idioma do menu padrão, conforme criado no DVD.</span><span class="sxs-lookup"><span data-stu-id="deeb8-109">This value is not necessarily the same as the default menu language as authored on the DVD.</span></span> <span data-ttu-id="deeb8-110">Para obter o intervalo de LCIDs válidos, consulte a documentação do Win32 no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="deeb8-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="deeb8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="deeb8-111">Remarks</span></span>

<span data-ttu-id="deeb8-112">Esta propriedade é de leitura/gravação sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="deeb8-112">This property is read/write with no default value.</span></span> <span data-ttu-id="deeb8-113">Se nenhum LCID de menu padrão for especificado, o objeto MSDVDAdm usará o idioma marcado como o idioma de menu padrão no disco.</span><span class="sxs-lookup"><span data-stu-id="deeb8-113">If no default menu LCID is specified, the MSDVDAdm object will use the language that is marked as the default menu language on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="deeb8-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="deeb8-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deeb8-115">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="deeb8-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



