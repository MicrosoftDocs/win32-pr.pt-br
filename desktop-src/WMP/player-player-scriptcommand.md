---
title: Evento Player. ScriptCommand
description: O evento ScriptCommand ocorre quando um comando ou uma URL sincronizada é recebida. | Evento Player. ScriptCommand
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Evento ScriptCommand do Windows Media Player
- Evento ScriptCommand Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento ScriptCommand
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784547"
---
# <a name="playerscriptcommand-event"></a><span data-ttu-id="01eff-107">Evento Player. ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="01eff-107">Player.ScriptCommand event</span></span>

<span data-ttu-id="01eff-108">O evento **ScriptCommand** ocorre quando um comando ou uma URL sincronizada é recebida.</span><span class="sxs-lookup"><span data-stu-id="01eff-108">The **ScriptCommand** event occurs when a synchronized command or URL is received.</span></span>

## <a name="syntax"></a><span data-ttu-id="01eff-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01eff-109">Syntax</span></span>


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="01eff-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01eff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01eff-111">*scType*</span><span class="sxs-lookup"><span data-stu-id="01eff-111">*scType*</span></span> 
</dt> <dd>

<span data-ttu-id="01eff-112">Cadeia de caracteres que especifica o tipo de comando de script.</span><span class="sxs-lookup"><span data-stu-id="01eff-112">String specifying the type of script command.</span></span>

</dd> <dt>

<span data-ttu-id="01eff-113">*Param*</span><span class="sxs-lookup"><span data-stu-id="01eff-113">*Param*</span></span> 
</dt> <dd>

<span data-ttu-id="01eff-114">**Cadeia de caracteres** que especifica o comando de script.</span><span class="sxs-lookup"><span data-stu-id="01eff-114">**String** specifying the script command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01eff-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01eff-115">Return value</span></span>

<span data-ttu-id="01eff-116">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="01eff-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01eff-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="01eff-117">Remarks</span></span>

<span data-ttu-id="01eff-118">Os comandos podem ser inseridos entre os sons e as imagens de um arquivo ou fluxo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="01eff-118">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="01eff-119">Os comandos são um par de cadeias de caracteres Unicode associadas a um horário designado no fluxo.</span><span class="sxs-lookup"><span data-stu-id="01eff-119">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="01eff-120">Quando o fluxo atinge o tempo associado ao comando, o controle do Windows Media Player envia um evento **ScriptCommand** com dois parâmetros.</span><span class="sxs-lookup"><span data-stu-id="01eff-120">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="01eff-121">Um parâmetro especifica o tipo de comando que está sendo enviado e o outro parâmetro especifica o comando.</span><span class="sxs-lookup"><span data-stu-id="01eff-121">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="01eff-122">O tipo de parâmetro é usado para determinar como o parâmetro de comando é processado.</span><span class="sxs-lookup"><span data-stu-id="01eff-122">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="01eff-123">Qualquer tipo de comando pode ser inserido em um arquivo ou fluxo para ser manipulado pelo evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="01eff-123">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="01eff-124">A tabela a seguir lista os tipos de comando de script que são processados automaticamente pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="01eff-124">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="01eff-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="01eff-125">Type</span></span>                   | <span data-ttu-id="01eff-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="01eff-126">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01eff-127">CAPTION</span><span class="sxs-lookup"><span data-stu-id="01eff-127">CAPTION</span></span>                | <span data-ttu-id="01eff-128">O controle exibe o texto associado na DIV especificada por *ClosedCaption*. **captioningID**.</span><span class="sxs-lookup"><span data-stu-id="01eff-128">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="01eff-129">CIRCUNSTÂNCIA</span><span class="sxs-lookup"><span data-stu-id="01eff-129">EVENT</span></span>                  | <span data-ttu-id="01eff-130">Informa o controle para executar instruções definidas para o evento especificado.</span><span class="sxs-lookup"><span data-stu-id="01eff-130">Tells the control to execute instructions defined for the specified event.</span></span>                                                                                          |
| <span data-ttu-id="01eff-131">NOME do arquivo</span><span class="sxs-lookup"><span data-stu-id="01eff-131">FILENAME</span></span>               | <span data-ttu-id="01eff-132">O controle redefine sua propriedade **URL** , tenta abrir o arquivo especificado e começa a reproduzir o novo fluxo imediatamente.</span><span class="sxs-lookup"><span data-stu-id="01eff-132">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="01eff-133">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="01eff-133">OPENEVENT</span></span>              | <span data-ttu-id="01eff-134">Armazena em buffer o comando de tipo de evento associado para execução oportuna do script de evento.</span><span class="sxs-lookup"><span data-stu-id="01eff-134">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="01eff-135">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="01eff-135">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="01eff-136">O parâmetro *param* contém o texto Lyric sincronizado.</span><span class="sxs-lookup"><span data-stu-id="01eff-136">The *Param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="01eff-137">O Windows Media Player exibe o texto Lyric na área de legenda codificada do recurso que agora está em **execução** .</span><span class="sxs-lookup"><span data-stu-id="01eff-137">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="01eff-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="01eff-138">TEXT</span></span>                   | <span data-ttu-id="01eff-139">O controle exibe o texto associado na DIV especificada por *ClosedCaption*. **captioningID**.</span><span class="sxs-lookup"><span data-stu-id="01eff-139">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="01eff-140">URL</span><span class="sxs-lookup"><span data-stu-id="01eff-140">URL</span></span>                    | <span data-ttu-id="01eff-141">O controle abrirá automaticamente a URL especificada usando o navegador de Internet padrão se as *configurações*. a propriedade **invokeURLs** está definida como true.</span><span class="sxs-lookup"><span data-stu-id="01eff-141">The control automatically opens the URL specified using the default Internet browser if the *Settings*.**invokeURLs** property is set to true.</span></span>                      |



 

<span data-ttu-id="01eff-142">Você pode inserir qualquer outro tipo de comando, desde que forneça o código recíproco para manipular o comando.</span><span class="sxs-lookup"><span data-stu-id="01eff-142">You can embed any other type of command as long as you provide reciprocal code to handle the command.</span></span> <span data-ttu-id="01eff-143">Embora comandos desconhecidos sejam ignorados pelo controle do Windows Media Player, eles ainda são enviados para o evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="01eff-143">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="01eff-144">Os comandos de URL recebidos pelo controle do Windows Media Player serão invocados automaticamente no navegador da Web padrão se as *configurações*. a propriedade **invokeURLs** está definida como true.</span><span class="sxs-lookup"><span data-stu-id="01eff-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the *Settings*.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="01eff-145">Você pode usar as *configurações*. Propriedade **DefaultFrame** para especificar o quadro de destino no qual a página da Web é exibida.</span><span class="sxs-lookup"><span data-stu-id="01eff-145">You can use the *Settings*.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="01eff-146">A URL enviada ao Windows Media Player é processada em relação à URL base especificada pelas *configurações*. Propriedade **baseURL** .</span><span class="sxs-lookup"><span data-stu-id="01eff-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the *Settings*.**baseURL** property.</span></span> <span data-ttu-id="01eff-147">A URL base é concatenada com a URL relativamente especificada, resultando em uma URL totalmente especificada que é passada como o parâmetro de comando pelo evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="01eff-147">The base URL is concatenated with the relatively specified URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="01eff-148">O controle do Windows Media Player sempre processa os comandos do tipo URL de entrada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="01eff-148">The Windows Media Player control always processes incoming URL-type commands in the following manner:</span></span>

1.  <span data-ttu-id="01eff-149">Um comando de tipo de URL é recebido.</span><span class="sxs-lookup"><span data-stu-id="01eff-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="01eff-150">*Configurações*. **baseURL** é usado para criar uma URL completa a partir da URL relativa especificada no comando de script.</span><span class="sxs-lookup"><span data-stu-id="01eff-150">*Settings*.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="01eff-151">*ScriptCommand* é chamado.</span><span class="sxs-lookup"><span data-stu-id="01eff-151">*ScriptCommand* is called.</span></span>
4.  <span data-ttu-id="01eff-152">Depois que *ScriptCommand* retorna, *as configurações*. **invokeURLs** está marcada.</span><span class="sxs-lookup"><span data-stu-id="01eff-152">After *ScriptCommand* returns, *Settings*.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="01eff-153">Se houver *configurações*. **invokeURLs** é true e o comando é um tipo de URL, a URL especificada é invocada.</span><span class="sxs-lookup"><span data-stu-id="01eff-153">If *Settings*.**invokeURLs** is true and the command is a URL-type, the specified URL is invoked.</span></span> <span data-ttu-id="01eff-154">Se houver *configurações*. **invokeURLs** é false ou, se o comando não for um tipo de URL, o comando será ignorado.</span><span class="sxs-lookup"><span data-stu-id="01eff-154">If *Settings*.**invokeURLs** is false or if the command is not a URL-type, the command is ignored.</span></span>

<span data-ttu-id="01eff-155">Ao criar um arquivo de mídia do Windows, você pode especificar em qual quadro a nova URL será exibida, concatenando dois e comercial e o nome do quadro no campo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="01eff-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="01eff-156">O exemplo a seguir ilustra os parâmetros típicos de *ScriptCommand* .</span><span class="sxs-lookup"><span data-stu-id="01eff-156">The example below illustrates typical *ScriptCommand* parameters.</span></span> <span data-ttu-id="01eff-157">Ele especifica que a URL *mypage* deve ser iniciada no quadro *myframe* .</span><span class="sxs-lookup"><span data-stu-id="01eff-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



<span data-ttu-id="01eff-158">O evento ScriptCommand não será chamado se o arquivo estiver sendo examinado (rápido-encaminhado ou revertido rapidamente).</span><span class="sxs-lookup"><span data-stu-id="01eff-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or fast-reversed).</span></span>

<span data-ttu-id="01eff-159">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="01eff-159">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="01eff-160">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="01eff-160">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="01eff-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01eff-161">Requirements</span></span>



| <span data-ttu-id="01eff-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="01eff-162">Requirement</span></span> | <span data-ttu-id="01eff-163">Valor</span><span class="sxs-lookup"><span data-stu-id="01eff-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01eff-164">Versão</span><span class="sxs-lookup"><span data-stu-id="01eff-164">Version</span></span><br/> | <span data-ttu-id="01eff-165">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="01eff-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="01eff-166">DLL</span><span class="sxs-lookup"><span data-stu-id="01eff-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="01eff-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01eff-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01eff-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="01eff-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01eff-169">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="01eff-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="01eff-170">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="01eff-170">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="01eff-171">**Settings. baseURL**</span><span class="sxs-lookup"><span data-stu-id="01eff-171">**Settings.baseURL**</span></span>](settings-baseurl.md)
</dt> <dt>

[<span data-ttu-id="01eff-172">**Settings. DefaultFrame**</span><span class="sxs-lookup"><span data-stu-id="01eff-172">**Settings.defaultFrame**</span></span>](settings-defaultframe.md)
</dt> <dt>

[<span data-ttu-id="01eff-173">**Settings. invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="01eff-173">**Settings.invokeURLs**</span></span>](settings-invokeurls.md)
</dt> </dl>

 

 





