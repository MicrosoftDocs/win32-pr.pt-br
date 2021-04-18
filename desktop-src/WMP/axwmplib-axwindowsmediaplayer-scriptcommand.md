---
title: Evento ScriptCommand do objeto AxWindowsMediaPlayer
description: O evento ScriptCommand ocorre quando um comando ou uma URL sincronizada é recebida. | Evento ScriptCommand do objeto AxWindowsMediaPlayer
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- Evento ScriptCommand do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760465"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f9e25-105">Evento ScriptCommand do objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="f9e25-105">ScriptCommand Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f9e25-106">O evento ScriptCommand ocorre quando um comando ou uma URL sincronizada é recebida.</span><span class="sxs-lookup"><span data-stu-id="f9e25-106">The ScriptCommand event occurs when a synchronized command or URL is received.</span></span>

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a><span data-ttu-id="f9e25-107">Dados de evento</span><span class="sxs-lookup"><span data-stu-id="f9e25-107">Event Data</span></span>

<span data-ttu-id="f9e25-108">O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="f9e25-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEventHandler**.</span></span> <span data-ttu-id="f9e25-109">Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ ScriptCommandEvent**, que contém as propriedades a seguir relacionadas a esse evento.</span><span class="sxs-lookup"><span data-stu-id="f9e25-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="f9e25-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f9e25-110">Property</span></span> | <span data-ttu-id="f9e25-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9e25-111">Description</span></span>                                                   |
|----------|---------------------------------------------------------------|
| <span data-ttu-id="f9e25-112">scType</span><span class="sxs-lookup"><span data-stu-id="f9e25-112">scType</span></span>   | <span data-ttu-id="f9e25-113">System. StringSpecifies o tipo de comando de script.</span><span class="sxs-lookup"><span data-stu-id="f9e25-113">System.StringSpecifies the type of script command.</span></span><br/> |
| <span data-ttu-id="f9e25-114">param</span><span class="sxs-lookup"><span data-stu-id="f9e25-114">param</span></span>    | <span data-ttu-id="f9e25-115">System. StringSpecifies o comando de script.</span><span class="sxs-lookup"><span data-stu-id="f9e25-115">System.StringSpecifies the script command.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="f9e25-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9e25-116">Remarks</span></span>

<span data-ttu-id="f9e25-117">Os comandos podem ser inseridos entre os sons e as imagens de um arquivo ou fluxo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f9e25-117">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="f9e25-118">Os comandos são um par de cadeias de caracteres Unicode associadas a um horário designado no fluxo.</span><span class="sxs-lookup"><span data-stu-id="f9e25-118">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="f9e25-119">Quando o fluxo atinge o tempo associado ao comando, o controle do Windows Media Player envia um evento **ScriptCommand** com dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f9e25-119">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="f9e25-120">Um parâmetro especifica o tipo de comando que está sendo enviado e o outro parâmetro especifica o comando.</span><span class="sxs-lookup"><span data-stu-id="f9e25-120">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="f9e25-121">O tipo de parâmetro é usado para determinar como o parâmetro de comando é processado.</span><span class="sxs-lookup"><span data-stu-id="f9e25-121">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="f9e25-122">Qualquer tipo de comando pode ser inserido em um arquivo ou fluxo para ser manipulado pelo evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f9e25-122">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="f9e25-123">A tabela a seguir lista os tipos de comando de script que são processados automaticamente pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f9e25-123">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="f9e25-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9e25-124">Type</span></span>                   | <span data-ttu-id="f9e25-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9e25-125">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e25-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="f9e25-126">CAPTION</span></span>                | <span data-ttu-id="f9e25-127">O controle exibe o texto associado no elemento HTML especificado por IWMPClosedCaption. **captioningId**.</span><span class="sxs-lookup"><span data-stu-id="f9e25-127">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="f9e25-128">CIRCUNSTÂNCIA</span><span class="sxs-lookup"><span data-stu-id="f9e25-128">EVENT</span></span>                  | <span data-ttu-id="f9e25-129">O controle executa instruções definidas para o evento especificado.</span><span class="sxs-lookup"><span data-stu-id="f9e25-129">The control executes instructions defined for the specified event.</span></span>                                                                                                  |
| <span data-ttu-id="f9e25-130">NOME do arquivo</span><span class="sxs-lookup"><span data-stu-id="f9e25-130">FILENAME</span></span>               | <span data-ttu-id="f9e25-131">O controle redefine sua propriedade **URL** , tenta abrir o arquivo especificado e começa a reproduzir o novo fluxo imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f9e25-131">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="f9e25-132">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="f9e25-132">OPENEVENT</span></span>              | <span data-ttu-id="f9e25-133">Armazena em buffer o comando de tipo de evento associado para execução oportuna do script de evento.</span><span class="sxs-lookup"><span data-stu-id="f9e25-133">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="f9e25-134">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="f9e25-134">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="f9e25-135">O parâmetro *param* contém o texto Lyric sincronizado.</span><span class="sxs-lookup"><span data-stu-id="f9e25-135">The *param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="f9e25-136">O Windows Media Player exibe o texto Lyric na área de legenda codificada do recurso que agora está em **execução** .</span><span class="sxs-lookup"><span data-stu-id="f9e25-136">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="f9e25-137">TEXT</span><span class="sxs-lookup"><span data-stu-id="f9e25-137">TEXT</span></span>                   | <span data-ttu-id="f9e25-138">O controle exibe o texto associado no elemento HTML especificado por IWMPClosedCaption. **captioningId**.</span><span class="sxs-lookup"><span data-stu-id="f9e25-138">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="f9e25-139">URL</span><span class="sxs-lookup"><span data-stu-id="f9e25-139">URL</span></span>                    | <span data-ttu-id="f9e25-140">O controle abrirá automaticamente a URL especificada usando o navegador de Internet padrão se o IWMPSettings. a propriedade **invokeURLs** está definida como true.</span><span class="sxs-lookup"><span data-stu-id="f9e25-140">The control automatically opens the URL specified using the default Internet browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span>                    |



 

<span data-ttu-id="f9e25-141">Você pode inserir qualquer outro tipo de comando, desde que forneça código para manipular o comando.</span><span class="sxs-lookup"><span data-stu-id="f9e25-141">You can embed any other type of command as long as you provide code to handle the command.</span></span> <span data-ttu-id="f9e25-142">Embora comandos desconhecidos sejam ignorados pelo controle do Windows Media Player, eles ainda são enviados para o evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f9e25-142">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="f9e25-143">O evento ScriptCommand não será chamado se o arquivo estiver sendo examinado no modo de avanço rápido ou retrocesso.</span><span class="sxs-lookup"><span data-stu-id="f9e25-143">The ScriptCommand event is not called if the file is being scanned in fast forward or rewind mode.</span></span>

<span data-ttu-id="f9e25-144">Os comandos de URL recebidos pelo controle do Windows Media Player serão invocados automaticamente no navegador da Web padrão se o IWMPSettings. a propriedade **invokeURLs** está definida como true.</span><span class="sxs-lookup"><span data-stu-id="f9e25-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="f9e25-145">Você pode usar o IWMPSettings. Propriedade **DefaultFrame** para especificar o quadro de destino no qual a página da Web é exibida.</span><span class="sxs-lookup"><span data-stu-id="f9e25-145">You can use the IWMPSettings.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="f9e25-146">A URL enviada ao Windows Media Player é processada em relação à URL base especificada pelo IWMPSettings. Propriedade **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="f9e25-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the IWMPSettings.**baseURL** property.</span></span> <span data-ttu-id="f9e25-147">A URL base é concatenada com a URL relativa, resultando em uma URL totalmente especificada que é passada como o parâmetro de comando pelo evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f9e25-147">The base URL is concatenated with the relative URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="f9e25-148">O controle do Windows Media Player sempre processa comandos de URL de entrada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f9e25-148">The Windows Media Player control always processes incoming URL commands in the following manner:</span></span>

1.  <span data-ttu-id="f9e25-149">Um comando de tipo de URL é recebido.</span><span class="sxs-lookup"><span data-stu-id="f9e25-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="f9e25-150">IWMPSettings. **baseURL** é usado para criar uma URL completa a partir da URL relativa especificada no comando de script.</span><span class="sxs-lookup"><span data-stu-id="f9e25-150">IWMPSettings.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="f9e25-151">**ScriptCommand** é chamado.</span><span class="sxs-lookup"><span data-stu-id="f9e25-151">**ScriptCommand** is called.</span></span>
4.  <span data-ttu-id="f9e25-152">Após **ScriptCommand** retornar, IWMPSettings. **invokeURLs** está marcada.</span><span class="sxs-lookup"><span data-stu-id="f9e25-152">After **ScriptCommand** returns, IWMPSettings.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="f9e25-153">Se IWMPSettings. **invokeURLs** é true e o comando é um comando de URL, a URL especificada é invocada.</span><span class="sxs-lookup"><span data-stu-id="f9e25-153">If IWMPSettings.**invokeURLs** is true and the command is a URL command, the specified URL is invoked.</span></span> <span data-ttu-id="f9e25-154">Se IWMPSettings. **invokeURLs** é false ou, se o comando não for um comando de URL, o comando será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f9e25-154">If IWMPSettings.**invokeURLs** is false or if the command is not a URL command, the command is ignored.</span></span>

<span data-ttu-id="f9e25-155">Ao criar um arquivo de mídia do Windows, você pode especificar em qual quadro a nova URL será exibida, concatenando dois e comercial e o nome do quadro no campo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f9e25-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="f9e25-156">O exemplo a seguir ilustra os parâmetros típicos de **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="f9e25-156">The following example illustrates typical **ScriptCommand** parameters.</span></span> <span data-ttu-id="f9e25-157">Ele especifica que a URL *mypage* deve ser iniciada no quadro *myframe* .</span><span class="sxs-lookup"><span data-stu-id="f9e25-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



<span data-ttu-id="f9e25-158">O evento ScriptCommand não será chamado se o arquivo estiver sendo examinado (encaminhado ou rebobinado rapidamente).</span><span class="sxs-lookup"><span data-stu-id="f9e25-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or rewound).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e25-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9e25-159">Requirements</span></span>



| <span data-ttu-id="f9e25-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9e25-160">Requirement</span></span> | <span data-ttu-id="f9e25-161">Valor</span><span class="sxs-lookup"><span data-stu-id="f9e25-161">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e25-162">Versão</span><span class="sxs-lookup"><span data-stu-id="f9e25-162">Version</span></span><br/>   | <span data-ttu-id="f9e25-163">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f9e25-163">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f9e25-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9e25-164">Namespace</span></span><br/> | <span data-ttu-id="f9e25-165">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f9e25-165">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f9e25-166">Assembly</span><span class="sxs-lookup"><span data-stu-id="f9e25-166">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f9e25-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f9e25-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9e25-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9e25-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e25-169">**Objeto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9e25-169">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9e25-170">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9e25-170">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9e25-171">**IWMPClosedCaption. captioningId (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9e25-171">**IWMPClosedCaption.captioningId (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9e25-172">**IWMPSettings. baseURL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9e25-172">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9e25-173">**IWMPSettings. DefaultFrame (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9e25-173">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f9e25-174">**IWMPSettings. invokeURLs (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f9e25-174">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





