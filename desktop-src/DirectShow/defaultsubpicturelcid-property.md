---
description: A propriedade DVDAdm. DefaultSubpictureLCID define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de subimagem.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propriedade DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500733"
---
# <a name="defaultsubpicturelcid-property"></a><span data-ttu-id="54fca-103">Propriedade DefaultSubpictureLCID</span><span class="sxs-lookup"><span data-stu-id="54fca-103">DefaultSubpictureLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="54fca-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="54fca-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="54fca-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="54fca-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="54fca-106">A `DVDAdm.DefaultSubpictureLCID` propriedade define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de subimagem.</span><span class="sxs-lookup"><span data-stu-id="54fca-106">The `DVDAdm.DefaultSubpictureLCID` property sets or retrieves the registry setting for the user-specified default LCID for the subpicture stream.</span></span>

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a><span data-ttu-id="54fca-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="54fca-107">Return Value</span></span>

<span data-ttu-id="54fca-108">Retorna um valor inteiro que representa o LCID da subimagem padrão especificado pelo usuário como armazenado nas configurações do registro para o aplicativo de DVD.</span><span class="sxs-lookup"><span data-stu-id="54fca-108">Returns an Integer value representing the user-specified default subpicture LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="54fca-109">Esse valor não é necessariamente o mesmo que o fluxo de subimagem padrão como criado no DVD.</span><span class="sxs-lookup"><span data-stu-id="54fca-109">This value is not necessarily the same as the default subpicture stream as authored on the DVD.</span></span> <span data-ttu-id="54fca-110">Para obter o intervalo de LCIDs válidos, consulte a documentação do Win32 no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="54fca-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="54fca-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="54fca-111">Remarks</span></span>

<span data-ttu-id="54fca-112">Esta propriedade é de leitura/gravação sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="54fca-112">This property is read/write with no default value.</span></span> <span data-ttu-id="54fca-113">Se nenhum LCID de subimagem padrão for especificado, o objeto MSDVDAdm reproduzirá o fluxo de subimagem marcado como o fluxo padrão no disco.</span><span class="sxs-lookup"><span data-stu-id="54fca-113">If no default subpicture LCID is specified, the MSDVDAdm object will play the subpicture stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="54fca-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="54fca-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54fca-115">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="54fca-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



