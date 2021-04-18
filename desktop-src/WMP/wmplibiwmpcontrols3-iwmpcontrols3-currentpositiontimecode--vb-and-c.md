---
title: Propriedade IWMPControls3 currentPositionTimecode
description: A propriedade currentPositionTimecode Obtém ou define a posição atual no item de mídia atual usando um formato de código de tempo. Essa propriedade atualmente dá suporte ao código de tempo SMPTE.
ms.assetid: 035b812c-e976-4b4e-b4e5-820653257732
keywords:
- Propriedade currentPositionTimecode Windows Media Player
- Propriedade currentPositionTimecode Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, Propriedade currentPositionTimecode
topic_type:
- apiref
api_name:
- IWMPControls3.currentPositionTimecode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7660e6dc2690c310cf06f64e38190dc1cb3f24ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747687"
---
# <a name="iwmpcontrols3currentpositiontimecode-property"></a><span data-ttu-id="ab088-107">Propriedade IWMPControls3:: currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="ab088-107">IWMPControls3::currentPositionTimecode property</span></span>

<span data-ttu-id="ab088-108">A propriedade **currentPositionTimecode** Obtém ou define a posição atual no item de mídia atual usando um formato de código de tempo.</span><span class="sxs-lookup"><span data-stu-id="ab088-108">The **currentPositionTimecode** property gets or sets the current position in the current media item using a time code format.</span></span> <span data-ttu-id="ab088-109">Essa propriedade atualmente dá suporte ao código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="ab088-109">This property currently supports SMPTE time code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab088-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab088-110">Syntax</span></span>


```CSharp
public System.String currentPositionTimecode {get; set;}
```


```VB

Public Property currentPositionTimecode As System.String
```





## <a name="property-value"></a><span data-ttu-id="ab088-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ab088-111">Property value</span></span>

<span data-ttu-id="ab088-112">Um **System. String** que é o código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="ab088-112">A **System.String** that is the SMPTE time code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab088-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab088-113">Remarks</span></span>

<span data-ttu-id="ab088-114">O código de tempo SMPTE fornece uma maneira padrão de identificar um quadro de vídeo individual, que é útil para sincronizar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="ab088-114">SMPTE time code provides a standard way of identifying an individual video frame, which is useful for synchronizing playback.</span></span> <span data-ttu-id="ab088-115">Se um arquivo de mídia digital oferecer suporte a código de hora SMPTE, o Windows Media Player poderá recuperar as informações de posição de código da hora atual ou buscar um quadro de vídeo identificado por um código de tempo específico.</span><span class="sxs-lookup"><span data-stu-id="ab088-115">If a digital media file supports SMPTE time code, Windows Media Player can retrieve the current time code position information or seek to a video frame identified by a particular time code.</span></span>

<span data-ttu-id="ab088-116">O código de tempo SMPTE identifica um determinado quadro pelo número de horas, minutos, segundos e quadros que o separam de um quadro de referência específico o quadro designado como tempo zero.</span><span class="sxs-lookup"><span data-stu-id="ab088-116">SMPTE time code identifies a particular frame by the number of hours, minutes, seconds, and frames that separate it from a particular reference frame the frame designated as time zero.</span></span> <span data-ttu-id="ab088-117">Geralmente, o quadro de tempo zero é o início do arquivo e um determinado valor de código de tempo SMPTE representa o tempo decorrido desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ab088-117">Usually the time zero frame is the start of the file and a particular SMPTE time code value represents the elapsed time since the start of the file.</span></span>

<span data-ttu-id="ab088-118">O código de tempo está no intervalo de formato \[  \] *hh*:*mm*:*SS*.*FF* em que \[ *Range* \] representa o intervalo, hh representa horas, *mm* representa minutos, *SS* representa segundos e *FF* representa quadros.</span><span class="sxs-lookup"><span data-stu-id="ab088-118">The time code is in the format \[*range*\]*hh*:*mm*:*ss*.*ff* where \[*range*\] represents the range, hh represents hours, *mm* represents minutes, *ss* represents seconds, and *ff* represents frames.</span></span> <span data-ttu-id="ab088-119">Ao definir um valor para **currentPositionTimecode**, você deve incluir todos os oito dígitos, usando zeros como espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="ab088-119">When setting a value for **currentPositionTimecode**, you must include all eight digits, using zeros as placeholders.</span></span>

<span data-ttu-id="ab088-120">\[*intervalo* \] de corresponde ao membro **wRange** da estrutura de **dados de extensão do \_ código \_ \_ de WMT** do formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="ab088-120">\[*range*\] corresponds to the **wRange** member of the Windows Media Format **WMT\_TIMECODE\_EXTENSION\_DATA** structure.</span></span> <span data-ttu-id="ab088-121">Para obter mais informações sobre intervalos de código de tempo, consulte o SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ab088-121">For more information about time code ranges, see the Windows Media Format SDK.</span></span>

<span data-ttu-id="ab088-122">Só há suporte para a configuração e obtenção de **currentPositionTimecode** para arquivos que contêm informações de código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="ab088-122">Setting and getting **currentPositionTimecode** is supported only for files that contain SMPTE time code information.</span></span>

## <a name="examples"></a><span data-ttu-id="ab088-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab088-123">Examples</span></span>

<span data-ttu-id="ab088-124">O exemplo de código a seguir especifica **currentPositionTimecode** como 1 hora, zero minutos, 30 segundos e 5 quadros.</span><span class="sxs-lookup"><span data-stu-id="ab088-124">The following code example specifies **currentPositionTimecode** as 1 hour, zero minutes, 30 seconds, and 5 frames.</span></span> <span data-ttu-id="ab088-125">O objeto **AxWMPLib. AxWindowsMediaPlayer** é representado pela variável chamada Player.</span><span class="sxs-lookup"><span data-stu-id="ab088-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
// so that you can use the currentPositionTimecode property.
WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

// Seek to a frame using SMPTE time code.
controls.currentPositionTimecode = "[00000]01:00:30.05";
```


```VB

' Cast the interface returned by player.Ctlcontrols to an IWMPControls3 interface
&#39; so that you can use the currentPositionTimecode property.
Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

&#39; Seek to a frame using SMPTE time code.
Controls.currentPositionTimecode = &quot;[00000]01:00:30.05&quot;
```





## <a name="requirements"></a><span data-ttu-id="ab088-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab088-126">Requirements</span></span>



| <span data-ttu-id="ab088-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab088-127">Requirement</span></span> | <span data-ttu-id="ab088-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ab088-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab088-129">Versão</span><span class="sxs-lookup"><span data-stu-id="ab088-129">Version</span></span><br/>   | <span data-ttu-id="ab088-130">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ab088-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ab088-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab088-131">Namespace</span></span><br/> | <span data-ttu-id="ab088-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ab088-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ab088-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="ab088-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ab088-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ab088-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab088-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab088-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab088-136">**Interface IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ab088-136">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





