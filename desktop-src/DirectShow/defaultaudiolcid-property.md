---
description: A propriedade DVDAdm. DefaultAudioLCID define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de áudio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Propriedade DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105780638"
---
# <a name="defaultaudiolcid-property"></a><span data-ttu-id="599e7-103">Propriedade DefaultAudioLCID</span><span class="sxs-lookup"><span data-stu-id="599e7-103">DefaultAudioLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="599e7-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="599e7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="599e7-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="599e7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="599e7-106">A `DVDAdm.DefaultAudioLCID` propriedade define ou recupera a configuração do registro para o LCID padrão especificado pelo usuário para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="599e7-106">The `DVDAdm.DefaultAudioLCID` property sets or retrieves the registry setting for the user-specified default LCID for the audio stream.</span></span>

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a><span data-ttu-id="599e7-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="599e7-107">Return Value</span></span>

<span data-ttu-id="599e7-108">Retorna um valor inteiro que representa o LCID de áudio padrão especificado pelo usuário como armazenado nas configurações do registro para o aplicativo de DVD.</span><span class="sxs-lookup"><span data-stu-id="599e7-108">Returns an Integer value representing the user-specified default audio LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="599e7-109">Esse valor não é necessariamente o mesmo que o fluxo de áudio padrão, como criado no DVD.</span><span class="sxs-lookup"><span data-stu-id="599e7-109">This value is not necessarily the same as the default audio stream as authored on the DVD.</span></span>

## <a name="remarks"></a><span data-ttu-id="599e7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="599e7-110">Remarks</span></span>

<span data-ttu-id="599e7-111">Esta propriedade é de leitura/gravação sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="599e7-111">This property is read/write with no default value.</span></span> <span data-ttu-id="599e7-112">Se nenhum LCID de áudio padrão for especificado, o objeto MSDVDAdm reproduzirá o fluxo de áudio marcado como o fluxo padrão no disco.</span><span class="sxs-lookup"><span data-stu-id="599e7-112">If no default audio LCID is specified, the MSDVDAdm object will play the audio stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="599e7-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="599e7-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599e7-114">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="599e7-114">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



