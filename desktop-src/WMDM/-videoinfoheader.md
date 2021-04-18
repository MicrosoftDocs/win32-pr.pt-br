---
title: Estrutura de _VIDEOINFOHEADER
description: A \_ estrutura VIDEOINFOHEADER contém informações sobre um fluxo de vídeo e inclui uma \_ estrutura BITMAPINFOHEADER que define o formato de um quadro individual.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- Estrutura de _VIDEOINFOHEADER Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813400"
---
# <a name="_videoinfoheader-structure"></a><span data-ttu-id="1060b-104">\_Estrutura VIDEOINFOHEADER</span><span class="sxs-lookup"><span data-stu-id="1060b-104">\_VIDEOINFOHEADER structure</span></span>

<span data-ttu-id="1060b-105">A estrutura **\_ VIDEOINFOHEADER** contém informações sobre um fluxo de vídeo e inclui uma estrutura **\_ BITMAPINFOHEADER** que define o formato de um quadro individual.</span><span class="sxs-lookup"><span data-stu-id="1060b-105">The **\_VIDEOINFOHEADER** structure contains information about a video stream and includes a **\_BITMAPINFOHEADER** structure that defines the format of an individual frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="1060b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1060b-106">Syntax</span></span>


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="1060b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1060b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1060b-108">**rcSource**</span><span class="sxs-lookup"><span data-stu-id="1060b-108">**rcSource**</span></span>
</dt> <dd>

<span data-ttu-id="1060b-109">A estrutura **Rect** que especifica a janela de vídeo de origem.</span><span class="sxs-lookup"><span data-stu-id="1060b-109">**RECT** structure that specifies the source video window.</span></span>

</dd> <dt>

<span data-ttu-id="1060b-110">**rcTarget**</span><span class="sxs-lookup"><span data-stu-id="1060b-110">**rcTarget**</span></span>
</dt> <dd>

<span data-ttu-id="1060b-111">A estrutura **Rect** que especifica a janela de vídeo de destino.</span><span class="sxs-lookup"><span data-stu-id="1060b-111">**RECT** structure that specifies the destination video window.</span></span>

</dd> <dt>

<span data-ttu-id="1060b-112">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="1060b-112">**dwBitRate**</span></span>
</dt> <dd>

<span data-ttu-id="1060b-113">Valor **DWORD** que especifica a taxa aproximada de dados do fluxo de vídeo, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1060b-113">**DWORD** value that specifies the video stream's approximate data rate, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="1060b-114">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="1060b-114">**dwBitErrorRate**</span></span>
</dt> <dd>

<span data-ttu-id="1060b-115">Valor **DWORD** que especifica a taxa de erros de dados do fluxo de vídeo, erros de bit por segundo.</span><span class="sxs-lookup"><span data-stu-id="1060b-115">**DWORD** value that specifies the video stream's data error rate, in bit errors per second.</span></span>

</dd> <dt>

<span data-ttu-id="1060b-116">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="1060b-116">**AvgTimePerFrame**</span></span>
</dt> <dd>

<span data-ttu-id="1060b-117">**Referência \_ do** Valor de tempo que especifica o tempo médio de exibição do quadro de vídeo, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="1060b-117">**REFERENCE\_TIME** value that specifies the video frame's average display time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="1060b-118">**bmiHeader**</span><span class="sxs-lookup"><span data-stu-id="1060b-118">**bmiHeader**</span></span>
</dt> <dd>

<span data-ttu-id="1060b-119">Estrutura **\_ BITMAPINFOHEADER** do Win32 que contém informações de cor e dimensão para o bitmap de imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1060b-119">Win32 **\_BITMAPINFOHEADER** structure that contains color and dimension information for the video image bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1060b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1060b-120">Requirements</span></span>



| <span data-ttu-id="1060b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1060b-121">Requirement</span></span> | <span data-ttu-id="1060b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1060b-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1060b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1060b-123">Header</span></span><br/> | <dl> <span data-ttu-id="1060b-124"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1060b-124"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1060b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1060b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1060b-126">**\_BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="1060b-126">**\_BITMAPINFOHEADER**</span></span>](-bitmapinfoheader.md)
</dt> <dt>

[<span data-ttu-id="1060b-127">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="1060b-127">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





