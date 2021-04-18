---
title: Controls. currentPositionTimecode
description: A propriedade currentPositionTimecode especifica ou recupera a posição atual no item de mídia atual usando um formato de código de tempo. Essa propriedade atualmente dá suporte ao código de tempo SMPTE.
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- Controls. currentPositionTimecode Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e2a4ddeb0849a829ff7a16fd80ff4891cfe56c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796434"
---
# <a name="controlscurrentpositiontimecode"></a><span data-ttu-id="4de88-105">Controls. currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="4de88-105">Controls.currentPositionTimecode</span></span>

<span data-ttu-id="4de88-106">A propriedade **currentPositionTimecode** especifica ou recupera a posição atual no item de mídia atual usando um formato de código de tempo.</span><span class="sxs-lookup"><span data-stu-id="4de88-106">The **currentPositionTimecode** property specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="4de88-107">Essa propriedade atualmente dá suporte ao código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4de88-107">This property currently supports SMPTE time code.</span></span>

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a><span data-ttu-id="4de88-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="4de88-108">Possible Values</span></span>

<span data-ttu-id="4de88-109">Esta propriedade é uma **cadeia de caracteres** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4de88-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4de88-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4de88-110">Remarks</span></span>

<span data-ttu-id="4de88-111">O código de tempo SMPTE fornece uma maneira padrão de identificar um quadro de vídeo individual, que é útil para sincronizar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="4de88-111">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="4de88-112">Se um arquivo de mídia digital der suporte a código de hora SMPTE, o Windows Media Player poderá recuperar as informações de posição do código de tempo atual ou buscar um quadro de vídeo identificado por uma **cadeia de caracteres** de código de tempo específica.</span><span class="sxs-lookup"><span data-stu-id="4de88-112">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code **String**.</span></span>

<span data-ttu-id="4de88-113">O código de tempo SMPTE identifica um determinado quadro pelo número de horas, minutos, segundos e quadros que o separam de um quadro de referência específico o quadro designado como tempo zero.</span><span class="sxs-lookup"><span data-stu-id="4de88-113">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="4de88-114">Geralmente, o quadro de tempo zero é o início do arquivo e um determinado valor de código de tempo SMPTE representa o tempo decorrido desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="4de88-114">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="4de88-115">A cadeia de **caracteres** de código de tempo está no intervalo de formato \[  \] *hh*:*mm*:*SS*.*FF* em que \[ *Range* \] representa o intervalo, *hh* representa horas, *mm* representa minutos, *SS* representa segundos e *FF* representa quadros.</span><span class="sxs-lookup"><span data-stu-id="4de88-115">The time code **String** is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, *hh* represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="4de88-116">Ao especificar um valor usando **currentPositionTimecode**, você deve incluir todos os oito dígitos usando zeros como espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="4de88-116">When specifying a value using **currentPositionTimecode**, you must include all eight digits using zeros as placeholders.</span></span>

<span data-ttu-id="4de88-117">O \[  \] especificador de intervalo corresponde ao membro **wRange** da estrutura de dados de extensão do código de WMT do formato de mídia do Windows. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4de88-117">The \[*range*\] specifier corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="4de88-118">Para obter mais informações sobre intervalos de código de tempo, consulte o SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4de88-118">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="4de88-119">Só há suporte para a especificação e recuperação de **currentPositionTimecode** para arquivos que contêm informações de código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4de88-119">Specifying and retrieving **currentPositionTimecode** is only supported for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="4de88-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4de88-120">Examples</span></span>

<span data-ttu-id="4de88-121">O exemplo de código a seguir especifica **currentPositionTimecode** como 1 hora, zero minutos, 30 segundos e 5 quadros.</span><span class="sxs-lookup"><span data-stu-id="4de88-121">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="4de88-122">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4de88-122">The **Player** object was created with ID = "Player".</span></span>


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a><span data-ttu-id="4de88-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4de88-123">Requirements</span></span>



| <span data-ttu-id="4de88-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4de88-124">Requirement</span></span> | <span data-ttu-id="4de88-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4de88-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4de88-126">Versão</span><span class="sxs-lookup"><span data-stu-id="4de88-126">Version</span></span><br/> | <span data-ttu-id="4de88-127">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="4de88-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="4de88-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4de88-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="4de88-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de88-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de88-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4de88-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de88-131">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="4de88-131">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





