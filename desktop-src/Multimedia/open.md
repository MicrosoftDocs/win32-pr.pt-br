---
title: comando abrir (Corecrt \_ Io. h)
description: O comando abrir Inicializa um dispositivo. Todos os dispositivos MCI reconhecem este comando.
ms.assetid: 0bb97c8c-8222-4d4e-b20b-94e9f9095afe
keywords:
- abrir o comando multimídia do Windows
topic_type:
- apiref
api_name:
- open
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8d31f1806a9c12f764c679548564aa053c3041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644632"
---
# <a name="open-command"></a><span data-ttu-id="3c89f-105">Abrir comando</span><span class="sxs-lookup"><span data-stu-id="3c89f-105">open command</span></span>

<span data-ttu-id="3c89f-106">O comando abrir Inicializa um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-106">The open command initializes a device.</span></span> <span data-ttu-id="3c89f-107">Todos os dispositivos MCI reconhecem este comando.</span><span class="sxs-lookup"><span data-stu-id="3c89f-107">All MCI devices recognize this command.</span></span>

<span data-ttu-id="3c89f-108">Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="3c89f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("open %s %s %s"), 
  lpszDevice, 
  lpszOpenFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="3c89f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c89f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c89f-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span><span class="sxs-lookup"><span data-stu-id="3c89f-110"><span id="lpszDevice"></span><span id="lpszdevice"></span><span id="LPSZDEVICE"></span>*lpszDevice*</span></span>
</dt> <dd>

<span data-ttu-id="3c89f-111">Identificador de um dispositivo MCI ou driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-111">Identifier of an MCI device or device driver.</span></span> <span data-ttu-id="3c89f-112">Pode ser um nome de dispositivo (conforme fornecido no registro ou no arquivo de SYSTEM.INI) ou o nome de arquivo do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-112">This can be either a device name (as given in the registry or the SYSTEM.INI file) or the filename of the device driver.</span></span> <span data-ttu-id="3c89f-113">Se você especificar o nome de arquivo do driver de dispositivo, você pode opcionalmente incluir o. Extensão DRV, mas você não deve incluir o caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-113">If you specify the filename of the device driver, you can optionally include the .DRV extension, but you should not include the path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="3c89f-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span><span class="sxs-lookup"><span data-stu-id="3c89f-114"><span id="lpszOpenFlags"></span><span id="lpszopenflags"></span><span id="LPSZOPENFLAGS"></span>*lpszOpenFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3c89f-115">Sinalizador que identifica o que inicializar.</span><span class="sxs-lookup"><span data-stu-id="3c89f-115">Flag that identifies what to initialize.</span></span> <span data-ttu-id="3c89f-116">A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **Open** e os sinalizadores usados por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-116">The following table lists device types that recognize the **open** command and the flags used by each type.</span></span>



| <span data-ttu-id="3c89f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3c89f-117">Value</span></span>        | <span data-ttu-id="3c89f-118">Significado</span><span class="sxs-lookup"><span data-stu-id="3c89f-118">Meaning</span></span>                                                        | <span data-ttu-id="3c89f-119">Significado</span><span class="sxs-lookup"><span data-stu-id="3c89f-119">Meaning</span></span>                                                                         |
|--------------|----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3c89f-120">cdaudio</span><span class="sxs-lookup"><span data-stu-id="3c89f-120">cdaudio</span></span>      | <span data-ttu-id="3c89f-121">*\_ alias de dispositivo* de alias compartilhável</span><span class="sxs-lookup"><span data-stu-id="3c89f-121">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="3c89f-122">Digite *o \_ tipo de dispositivo*</span><span class="sxs-lookup"><span data-stu-id="3c89f-122">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="3c89f-123">digitalvideo</span><span class="sxs-lookup"><span data-stu-id="3c89f-123">digitalvideo</span></span> | <span data-ttu-id="3c89f-124">dispositivo de alias *\_ aliaselementname* não static pai *hWnd* compartilhável</span><span class="sxs-lookup"><span data-stu-id="3c89f-124">alias *device\_aliaselementname* nostatic parent *hwnd* sharable</span></span> | <span data-ttu-id="3c89f-125">tipo de *estilo \_* de estilo filho estilo sobreposto Style tipo de *dispositivo \_* tipo</span><span class="sxs-lookup"><span data-stu-id="3c89f-125">style child style overlapped style popup style *style\_type* type *device\_type*</span></span> |
| <span data-ttu-id="3c89f-126">overlay</span><span class="sxs-lookup"><span data-stu-id="3c89f-126">overlay</span></span>      | <span data-ttu-id="3c89f-127">alias *de \_ dispositivo* de alias pai *hWnd* de estilo compartilhável filho</span><span class="sxs-lookup"><span data-stu-id="3c89f-127">alias *device\_alias* parent *hwnd* sharable style child</span></span>         | <span data-ttu-id="3c89f-128">estilo de estilo sobreposto estilo *de \_ tipo de estilo* não tipo tipo de *dispositivo \_*</span><span class="sxs-lookup"><span data-stu-id="3c89f-128">style overlapped style popup style *style\_type* type *device\_type*</span></span>             |
| <span data-ttu-id="3c89f-129">sequenciador</span><span class="sxs-lookup"><span data-stu-id="3c89f-129">sequencer</span></span>    | <span data-ttu-id="3c89f-130">*\_ alias de dispositivo* de alias compartilhável</span><span class="sxs-lookup"><span data-stu-id="3c89f-130">alias *device\_alias* sharable</span></span>                                 | <span data-ttu-id="3c89f-131">Digite *o \_ tipo de dispositivo*</span><span class="sxs-lookup"><span data-stu-id="3c89f-131">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="3c89f-132">videocassete</span><span class="sxs-lookup"><span data-stu-id="3c89f-132">vcr</span></span>          | <span data-ttu-id="3c89f-133">*\_ alias de dispositivo* de alias compartilhável</span><span class="sxs-lookup"><span data-stu-id="3c89f-133">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="3c89f-134">Digite *o \_ tipo de dispositivo*</span><span class="sxs-lookup"><span data-stu-id="3c89f-134">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="3c89f-135">videodisk</span><span class="sxs-lookup"><span data-stu-id="3c89f-135">videodisk</span></span>    | <span data-ttu-id="3c89f-136">*\_ alias de dispositivo* de alias compartilhável</span><span class="sxs-lookup"><span data-stu-id="3c89f-136">alias *device\_alias* sharable</span></span>                                  | <span data-ttu-id="3c89f-137">Digite *o \_ tipo de dispositivo*</span><span class="sxs-lookup"><span data-stu-id="3c89f-137">type *device\_type*</span></span>                                                             |
| <span data-ttu-id="3c89f-138">waveaudio</span><span class="sxs-lookup"><span data-stu-id="3c89f-138">waveaudio</span></span>    | <span data-ttu-id="3c89f-139">*\_ tamanho do buffer* de buffer do *\_ alias de dispositivo* de alias</span><span class="sxs-lookup"><span data-stu-id="3c89f-139">alias *device\_alias* buffer *buffer\_size*</span></span>                     | <span data-ttu-id="3c89f-140">tipo de *dispositivo \_* compartilhável</span><span class="sxs-lookup"><span data-stu-id="3c89f-140">sharable type *device\_type*</span></span>                                                    |



 

<span data-ttu-id="3c89f-141">A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszOpenFlags** e seus significados.</span><span class="sxs-lookup"><span data-stu-id="3c89f-141">The following table lists the flags that can be specified in the **lpszOpenFlags** parameter and their meanings.</span></span>



| <span data-ttu-id="3c89f-142">Valor</span><span class="sxs-lookup"><span data-stu-id="3c89f-142">Value</span></span>                 | <span data-ttu-id="3c89f-143">Significado</span><span class="sxs-lookup"><span data-stu-id="3c89f-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c89f-144">*\_ alias de dispositivo* de alias</span><span class="sxs-lookup"><span data-stu-id="3c89f-144">alias *device\_alias*</span></span> | <span data-ttu-id="3c89f-145">Especifica um nome alternativo para o dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3c89f-145">Specifies an alternate name for the given device.</span></span> <span data-ttu-id="3c89f-146">Se especificado, ele deve ser usado como a *\_ ID do dispositivo* em comandos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="3c89f-146">If specified, it must be used as the *device\_id* in subsequent commands.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="3c89f-147">*ElementName*</span><span class="sxs-lookup"><span data-stu-id="3c89f-147">*elementname*</span></span>         | <span data-ttu-id="3c89f-148">Especifica o nome do elemento do dispositivo (arquivo) carregado quando o dispositivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="3c89f-148">Specifies the name of the device element (file) loaded when the device opens.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3c89f-149">*\_ tamanho do buffer* de buffer</span><span class="sxs-lookup"><span data-stu-id="3c89f-149">buffer *buffer\_size*</span></span> | <span data-ttu-id="3c89f-150">Define o tamanho, em segundos, do buffer usado pelo dispositivo de formato de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="3c89f-150">Sets the size, in seconds, of the buffer used by the waveform-audio device.</span></span> <span data-ttu-id="3c89f-151">O tamanho padrão do buffer é definido quando o dispositivo de formato de onda-áudio é instalado ou configurado.</span><span class="sxs-lookup"><span data-stu-id="3c89f-151">The default size of the buffer is set when the waveform-audio device is installed or configured.</span></span> <span data-ttu-id="3c89f-152">Normalmente, o tamanho do buffer é definido como 4 segundos.</span><span class="sxs-lookup"><span data-stu-id="3c89f-152">Typically the buffer size is set to 4 seconds.</span></span> <span data-ttu-id="3c89f-153">Com o dispositivo MCIWAVE, o tamanho mínimo é de 2 segundos e o tamanho máximo é de 9 segundos.</span><span class="sxs-lookup"><span data-stu-id="3c89f-153">With the MCIWAVE device, the minimum size is 2 seconds and the maximum size is 9 seconds.</span></span>                                                |
| <span data-ttu-id="3c89f-154">*HWND* pai</span><span class="sxs-lookup"><span data-stu-id="3c89f-154">parent *hwnd*</span></span>         | <span data-ttu-id="3c89f-155">Especifica o identificador de janela da janela pai.</span><span class="sxs-lookup"><span data-stu-id="3c89f-155">Specifies the window handle of the parent window.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3c89f-156">compartilháveis</span><span class="sxs-lookup"><span data-stu-id="3c89f-156">sharable</span></span>              | <span data-ttu-id="3c89f-157">Inicializa o dispositivo ou o arquivo como compartilhável.</span><span class="sxs-lookup"><span data-stu-id="3c89f-157">Initializes the device or file as sharable.</span></span> <span data-ttu-id="3c89f-158">As tentativas subsequentes de abrir o dispositivo ou arquivo falham, a menos que você especifique "compartilhável" nos comandos **abertos** original e subseqüente.</span><span class="sxs-lookup"><span data-stu-id="3c89f-158">Subsequent attempts to open the device or file fail unless you specify "sharable" in both the original and subsequent **open** commands.</span></span> <span data-ttu-id="3c89f-159">O MCI retornará um erro de dispositivo inválido se o dispositivo já estiver aberto e não puder ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="3c89f-159">MCI returns an invalid device error if the device is already open and not sharable.</span></span><br/> <span data-ttu-id="3c89f-160">Os dispositivos MCISEQ Sequencer e MCIWAVE não dão suporte a arquivos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="3c89f-160">The MCISEQ sequencer and MCIWAVE devices do not support shared files.</span></span><br/> |
| <span data-ttu-id="3c89f-161">filho do estilo</span><span class="sxs-lookup"><span data-stu-id="3c89f-161">style child</span></span>           | <span data-ttu-id="3c89f-162">Abre uma janela com um estilo de janela filho.</span><span class="sxs-lookup"><span data-stu-id="3c89f-162">Opens a window with a child window style.</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3c89f-163">estilo sobreposto</span><span class="sxs-lookup"><span data-stu-id="3c89f-163">style overlapped</span></span>      | <span data-ttu-id="3c89f-164">Abre uma janela com um estilo de janela sobreposto.</span><span class="sxs-lookup"><span data-stu-id="3c89f-164">Opens a window with an overlapped window style.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3c89f-165">pop-up de estilo</span><span class="sxs-lookup"><span data-stu-id="3c89f-165">style popup</span></span>           | <span data-ttu-id="3c89f-166">Abre uma janela com um estilo de janela pop-up.</span><span class="sxs-lookup"><span data-stu-id="3c89f-166">Opens a window with a pop-up window style.</span></span>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3c89f-167">*\_ tipo de estilo* de estilo</span><span class="sxs-lookup"><span data-stu-id="3c89f-167">style *style\_type*</span></span>   | <span data-ttu-id="3c89f-168">Indica um estilo de janela.</span><span class="sxs-lookup"><span data-stu-id="3c89f-168">Indicates a window style.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3c89f-169">Digite *o \_ tipo de dispositivo*</span><span class="sxs-lookup"><span data-stu-id="3c89f-169">type *device\_type*</span></span>   | <span data-ttu-id="3c89f-170">Especifica o tipo de dispositivo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-170">Specifies the device type of a file.</span></span>                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="3c89f-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="3c89f-171"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3c89f-172">Pode ser "Wait", "notificar" ou ambos.</span><span class="sxs-lookup"><span data-stu-id="3c89f-172">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="3c89f-173">Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="3c89f-173">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c89f-174">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3c89f-174">Return Value</span></span>

<span data-ttu-id="3c89f-175">Retornará zero se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="3c89f-175">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c89f-176">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c89f-176">Remarks</span></span>

<span data-ttu-id="3c89f-177">O MCI reserva "cdaudio" para o tipo de dispositivo de áudio de CD, "VIDEODISC" para o tipo de dispositivo VIDEODISC, "Sequencer" para o tipo de dispositivo Sequencer MIDI, "AVIVideo" para o tipo de dispositivo digital-video e "WaveAudio" para o tipo de dispositivo wave de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="3c89f-177">MCI reserves "cdaudio" for the CD audio device type, "videodisc" for the videodisc device type, "sequencer" for the MIDI sequencer device type, "AVIVideo" for the digital-video device type, and "waveaudio" for the waveform-audio device type.</span></span>

<span data-ttu-id="3c89f-178">Como uma alternativa ao sinalizador "tipo", o MCI pode selecionar o dispositivo com base na extensão usada pelo arquivo, conforme registrado no registro ou na \[ seção extensão MCI \] do arquivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="3c89f-178">As an alternative to the "type" flag, MCI can select the device based on the extension used by the file, as recorded in the registry or the \[mci extension\] section of the SYSTEM.INI file.</span></span>

<span data-ttu-id="3c89f-179">O MCI pode abrir arquivos AVI usando um ponteiro de interface de arquivo ou um ponteiro de interface de fluxo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-179">MCI can open AVI files by using a file-interface pointer or a stream-interface pointer.</span></span> <span data-ttu-id="3c89f-180">Para abrir um arquivo usando qualquer tipo de ponteiro de interface, especifique um sinal de arroba (@) seguido pelo ponteiro de interface no lugar do nome do arquivo ou do dispositivo para o parâmetro *lpszDevice* .</span><span class="sxs-lookup"><span data-stu-id="3c89f-180">To open a file by using either type of interface pointer, specify an at sign (@) followed by the interface pointer in place of the file or device name for the *lpszDevice* parameter.</span></span> <span data-ttu-id="3c89f-181">Para obter mais informações sobre as interfaces de arquivo e fluxo, consulte " [funções e macros do avifile](avifile-functions-and-macros.md)".</span><span class="sxs-lookup"><span data-stu-id="3c89f-181">For more information about the file and stream interfaces, see " [AVIFile Functions and Macros](avifile-functions-and-macros.md)."</span></span>

<span data-ttu-id="3c89f-182">O comando a seguir abre o dispositivo "mysound".</span><span class="sxs-lookup"><span data-stu-id="3c89f-182">The following command opens the "mysound" device.</span></span>

``` syntax
open new type waveaudio alias mysound buffer 6
```

<span data-ttu-id="3c89f-183">Com o nome do dispositivo "novo", o driver de formato de onda prepara um novo recurso de formato de onda.</span><span class="sxs-lookup"><span data-stu-id="3c89f-183">With device name "new", the waveform driver prepares a new waveform resource.</span></span> <span data-ttu-id="3c89f-184">O comando atribui o alias de dispositivo "mysound" e especifica um buffer de 6 segundos.</span><span class="sxs-lookup"><span data-stu-id="3c89f-184">The command assigns the device alias "mysound" and specifies a 6-second buffer.</span></span>

<span data-ttu-id="3c89f-185">Você pode eliminar o sinalizador "tipo" se combinar o nome do dispositivo com o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-185">You can eliminate the "type" flag if you combine the device name with the filename.</span></span> <span data-ttu-id="3c89f-186">O MCI reconhece essa combinação quando você usa a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="3c89f-186">MCI recognizes this combination when you use the following syntax:</span></span>

<span data-ttu-id="3c89f-187">*\_ nome do dispositivo* !</span><span class="sxs-lookup"><span data-stu-id="3c89f-187">*device\_name* !</span></span> <span data-ttu-id="3c89f-188">*nome do elemento \_*</span><span class="sxs-lookup"><span data-stu-id="3c89f-188">*element\_name*</span></span>

<span data-ttu-id="3c89f-189">O ponto de exclamação separa o nome do dispositivo do nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3c89f-189">The exclamation point separates the device name from the filename.</span></span> <span data-ttu-id="3c89f-190">O ponto de exclamação não deve ser delimitado por espaços em branco.</span><span class="sxs-lookup"><span data-stu-id="3c89f-190">The exclamation point should not be delimited by white spaces.</span></span>

<span data-ttu-id="3c89f-191">O exemplo a seguir abre a direita. Arquivo WAV usando o dispositivo "WaveAudio".</span><span class="sxs-lookup"><span data-stu-id="3c89f-191">The following example opens the RIGHT.WAV file using the "waveaudio" device.</span></span>

``` syntax
open waveaudio!right.wav
```

<span data-ttu-id="3c89f-192">O driver MCIWAVE requer um dispositivo de áudio de onda assíncrono.</span><span class="sxs-lookup"><span data-stu-id="3c89f-192">The MCIWAVE driver requires an asynchronous waveform-audio device.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c89f-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c89f-193">Requirements</span></span>



| <span data-ttu-id="3c89f-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c89f-194">Requirement</span></span> | <span data-ttu-id="3c89f-195">Valor</span><span class="sxs-lookup"><span data-stu-id="3c89f-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c89f-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c89f-196">Minimum supported client</span></span><br/> | <span data-ttu-id="3c89f-197">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c89f-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3c89f-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c89f-198">Minimum supported server</span></span><br/> | <span data-ttu-id="3c89f-199">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c89f-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3c89f-200">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3c89f-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c89f-201"><dt>Corecrt \_ Io. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c89f-201"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c89f-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c89f-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c89f-203">MCI</span><span class="sxs-lookup"><span data-stu-id="3c89f-203">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="3c89f-204">Cadeias de caracteres de comando MCI</span><span class="sxs-lookup"><span data-stu-id="3c89f-204">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

