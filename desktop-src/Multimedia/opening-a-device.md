---
title: Abrindo um dispositivo
description: Abrindo um dispositivo
ms.assetid: d4881d32-e8b7-45e6-b00b-b4cd69b738f1
keywords:
- MCI_OPEN comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd975b0dd5004fb4b1209003568b7fd5901cfc4e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007397"
---
# <a name="opening-a-device"></a><span data-ttu-id="e12cd-104">Abrindo um dispositivo</span><span class="sxs-lookup"><span data-stu-id="e12cd-104">Opening a Device</span></span>

<span data-ttu-id="e12cd-105">Antes de usar um dispositivo, você deve inicializá-lo usando o comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="e12cd-105">Before using a device, you must initialize it by using the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span> <span data-ttu-id="e12cd-106">Esse comando carrega o driver na memória (se ele ainda não estiver carregado) e recupera o identificador de dispositivo que você usará para identificar o dispositivo em comandos MCI subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e12cd-106">This command loads the driver into memory (if it isn't already loaded) and retrieves the device identifier you will use to identify the device in subsequent MCI commands.</span></span> <span data-ttu-id="e12cd-107">Você deve verificar o valor de retorno da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ou [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) antes de usar um novo identificador de dispositivo para garantir que o identificador seja válido.</span><span class="sxs-lookup"><span data-stu-id="e12cd-107">You should check the return value of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function before using a new device identifier to ensure that the identifier is valid.</span></span> <span data-ttu-id="e12cd-108">(Você também pode recuperar um identificador de dispositivo usando a função [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) .)</span><span class="sxs-lookup"><span data-stu-id="e12cd-108">(You can also retrieve a device identifier by using the [**mciGetDeviceID**](/previous-versions//dd757156(v=vs.85)) function.)</span></span>

<span data-ttu-id="e12cd-109">Como todas as mensagens de comando MCI, o **MCI \_ Open** tem uma estrutura associada.</span><span class="sxs-lookup"><span data-stu-id="e12cd-109">Like all MCI command messages, **MCI\_OPEN** has an associated structure.</span></span> <span data-ttu-id="e12cd-110">Essas estruturas são, às vezes, chamadas de *blocos de parâmetro*.</span><span class="sxs-lookup"><span data-stu-id="e12cd-110">These structures are sometimes called *parameter blocks*.</span></span> <span data-ttu-id="e12cd-111">A estrutura padrão para o **MCI \_ Open** é o [**MCI \_ Open \_ parms**](mci-open-parms.md).</span><span class="sxs-lookup"><span data-stu-id="e12cd-111">The default structure for **MCI\_OPEN** is [**MCI\_OPEN\_PARMS**](mci-open-parms.md).</span></span> <span data-ttu-id="e12cd-112">Determinados dispositivos (como forma de *onda* e *sobreposição*) têm estruturas estendidas (como o [**MCI \_ Wave \_ Open \_ parms**](mci-wave-open-parms.md) e o [**MCI \_ OVLY \_ Open \_ parms**](mci-ovly-open-parms.md)) para acomodar parâmetros opcionais adicionais.</span><span class="sxs-lookup"><span data-stu-id="e12cd-112">Certain devices (such as *waveform* and *overlay*) have extended structures (such as [**MCI\_WAVE\_OPEN\_PARMS**](mci-wave-open-parms.md) and [**MCI\_OVLY\_OPEN\_PARMS**](mci-ovly-open-parms.md)) to accommodate additional optional parameters.</span></span> <span data-ttu-id="e12cd-113">A menos que você precise usar esses parâmetros adicionais, poderá usar a estrutura **MCI \_ Open \_ parms** com qualquer dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="e12cd-113">Unless you need to use these additional parameters, you can use the **MCI\_OPEN\_PARMS** structure with any MCI device.</span></span>

<span data-ttu-id="e12cd-114">O número de dispositivos que você pode ter aberto é limitado apenas pela quantidade de memória disponível.</span><span class="sxs-lookup"><span data-stu-id="e12cd-114">The number of devices you can have open is limited only by the amount of available memory.</span></span>

## <a name="using-an-alias"></a><span data-ttu-id="e12cd-115">Usando um alias</span><span class="sxs-lookup"><span data-stu-id="e12cd-115">Using an Alias</span></span>

<span data-ttu-id="e12cd-116">Ao abrir um dispositivo, você pode usar o sinalizador "alias" para especificar um identificador de dispositivo para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-116">When you open a device, you can use the "alias" flag to specify a device identifier for the device.</span></span> <span data-ttu-id="e12cd-117">Esse sinalizador permite que você atribua um pequeno identificador de dispositivo para dispositivos compostos com nomes de arquivo longos e permite abrir várias instâncias do mesmo arquivo ou dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-117">This flag lets you assign a short device identifier for compound devices with lengthy filenames, and it lets you open multiple instances of the same file or device.</span></span>

<span data-ttu-id="e12cd-118">Por exemplo, o comando a seguir atribui o identificador de dispositivo "birdcall" ao nome de arquivo longo: \\ NABIRDS \\ sons \\ MOCKMTNG. WAV</span><span class="sxs-lookup"><span data-stu-id="e12cd-118">For example, the following command assigns the device identifier "birdcall" to the lengthy filename C:\\NABIRDS\\SOUNDS\\MOCKMTNG.WAV:</span></span>


```C++
mciSendString(
    "open c:\nabirds\sounds\mockmtng.wav type waveaudio alias birdcall", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="e12cd-119">Na interface de mensagem de comando, você especifica um alias usando o membro **lpstrAlias** da estrutura de [**\_ \_ parâmetros abertos do MCI**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="e12cd-119">In the command-message interface, you specify an alias by using the **lpstrAlias** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="specifying-a-device-type"></a><span data-ttu-id="e12cd-120">Especificando um tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e12cd-120">Specifying a Device Type</span></span>

<span data-ttu-id="e12cd-121">Ao abrir um dispositivo, você pode usar o sinalizador "tipo" para se referir a um tipo de dispositivo, e não a um driver de dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="e12cd-121">When you open a device, you can use the "type" flag to refer to a device type, rather than to a specific device driver.</span></span> <span data-ttu-id="e12cd-122">O exemplo a seguir abre o arquivo de formato de onda-áudio C: \\ Windows \\ Chimes. WAV (usando o sinalizador "Type" para especificar o tipo de dispositivo **WaveAudio** ) e atribui o alias "Chimes":</span><span class="sxs-lookup"><span data-stu-id="e12cd-122">The following example opens the waveform-audio file C:\\WINDOWS\\CHIMES.WAV (using the "type" flag to specify the **waveaudio** device type) and assigns the alias "chimes":</span></span>


```C++
mciSendString(
    "open c:\windows\chimes.wav type waveaudio alias chimes", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="e12cd-123">Na interface de mensagem de comando, a funcionalidade do sinalizador "Type" é fornecida pelo membro **lpstrDeviceType** da estrutura [**MCI \_ Open \_ parms**](mci-open-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="e12cd-123">In the command-message interface, the functionality of the "type" flag is supplied by the **lpstrDeviceType** member of the [**MCI\_OPEN\_PARMS**](mci-open-parms.md) structure.</span></span>

## <a name="simple-and-compound-devices"></a><span data-ttu-id="e12cd-124">Dispositivos simples e compostos</span><span class="sxs-lookup"><span data-stu-id="e12cd-124">Simple and Compound Devices</span></span>

<span data-ttu-id="e12cd-125">O MCI classifica os drivers de dispositivo como *compostos* ou *simples*.</span><span class="sxs-lookup"><span data-stu-id="e12cd-125">MCI classifies device drivers as *compound* or *simple*.</span></span> <span data-ttu-id="e12cd-126">Os drivers para dispositivos compostos exigem o nome de um arquivo de dados para reprodução; os drivers para dispositivos simples não fazem isso.</span><span class="sxs-lookup"><span data-stu-id="e12cd-126">Drivers for compound devices require the name of a data file for playback; drivers for simple devices do not.</span></span>

<span data-ttu-id="e12cd-127">Dispositivos simples incluem dispositivos **cdaudio** e **VIDEODISC** .</span><span class="sxs-lookup"><span data-stu-id="e12cd-127">Simple devices include **cdaudio** and **videodisc** devices.</span></span> <span data-ttu-id="e12cd-128">Há duas maneiras de abrir dispositivos simples:</span><span class="sxs-lookup"><span data-stu-id="e12cd-128">There are two ways to open simple devices:</span></span>

-   <span data-ttu-id="e12cd-129">Especifique um ponteiro para uma cadeia de caracteres terminada em nulo que contenha o nome do dispositivo do registro ou o arquivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="e12cd-129">Specify a pointer to a null-terminated string containing the device name from the registry or the SYSTEM.INI file.</span></span>

    <span data-ttu-id="e12cd-130">Por exemplo, você pode abrir um dispositivo **VIDEODISC** usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="e12cd-130">For example, you can open a **videodisc** device by using the following command:</span></span>


```C++
    mciSendString("open videodisc", lpszReturnString, 
        lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="e12cd-131">Nesse caso, "VIDEODISC" é o nome do dispositivo no registro ou na \[ seção MCI \] de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="e12cd-131">In this case, "videodisc" is the device name from the registry or the \[mci\] section of SYSTEM.INI.</span></span>

-   <span data-ttu-id="e12cd-132">Especifique o nome real do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-132">Specify the actual name of the device driver.</span></span> <span data-ttu-id="e12cd-133">No entanto, abrir um dispositivo usando o nome de arquivo do driver do dispositivo torna o aplicativo específico ao dispositivo e pode impedir que o aplicativo seja executado se a configuração do sistema for alterada.</span><span class="sxs-lookup"><span data-stu-id="e12cd-133">Opening a device using the device-driver filename, however, makes the application device-specific and can prevent the application from running if the system configuration changes.</span></span> <span data-ttu-id="e12cd-134">Se você usar um nome de arquivo, não será necessário especificar o caminho completo ou a extensão de nome de arquivo; O MCI pressupõe que os drivers estejam localizados em um diretório do sistema e tenham o. Extensão de nome de arquivo DRV.</span><span class="sxs-lookup"><span data-stu-id="e12cd-134">If you use a filename, you do not need to specify the complete path or the filename extension; MCI assumes drivers are located in a system directory and have the .DRV filename extension.</span></span>

<span data-ttu-id="e12cd-135">Os dispositivos compostos incluem dispositivos **WaveAudio** e **Sequencer** .</span><span class="sxs-lookup"><span data-stu-id="e12cd-135">Compound devices include **waveaudio** and **sequencer** devices.</span></span> <span data-ttu-id="e12cd-136">Os dados de um dispositivo composto, às vezes, são chamados de um *elemento de dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="e12cd-136">The data for a compound device is sometimes called a *device element*.</span></span> <span data-ttu-id="e12cd-137">Esse documento, no entanto, geralmente se refere a esses dados como um arquivo, embora, em alguns casos, os dados possam não ser armazenados como um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-137">This document, however, generally refers to this data as a file, even though in some cases the data might not be stored as a file.</span></span>

<span data-ttu-id="e12cd-138">Há três maneiras de abrir um dispositivo composto:</span><span class="sxs-lookup"><span data-stu-id="e12cd-138">There are three ways to open a compound device:</span></span>

-   <span data-ttu-id="e12cd-139">Especifique apenas o nome do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-139">Specify only the device name.</span></span> <span data-ttu-id="e12cd-140">Isso permite que você abra um dispositivo composto sem associar um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-140">This lets you open a compound device without associating a filename.</span></span> <span data-ttu-id="e12cd-141">A maioria dos dispositivos compostos processa apenas os comandos de [**capacidade**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) e [**fechar**](close.md) ([**MCI \_ fechar**](mci-close.md)) quando eles são abertos dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="e12cd-141">Most compound devices process only the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)) commands when they are opened this way.</span></span>
-   <span data-ttu-id="e12cd-142">Especifique somente o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-142">Specify only the filename.</span></span> <span data-ttu-id="e12cd-143">O nome do dispositivo é determinado das associações no registro.</span><span class="sxs-lookup"><span data-stu-id="e12cd-143">The device name is determined from the associations in the registry.</span></span>
-   <span data-ttu-id="e12cd-144">Especifique o nome do arquivo e do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-144">Specify the filename and the device name.</span></span> <span data-ttu-id="e12cd-145">O MCI ignora as entradas no registro e abre o nome do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e12cd-145">MCI ignores the entries in the registry and opens the specified device name.</span></span>

<span data-ttu-id="e12cd-146">Para associar um arquivo de dados a um dispositivo específico, você pode especificar o nome do arquivo e do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-146">To associate a data file with a particular device, you can specify the filename and device name.</span></span> <span data-ttu-id="e12cd-147">Por exemplo, o comando a seguir abre o dispositivo **WaveAudio** com o nome de arquivo myvoice. SND</span><span class="sxs-lookup"><span data-stu-id="e12cd-147">For example, the following command opens the **waveaudio** device with the filename MYVOICE.SND:</span></span>


```C++
mciSendString("open myvoice.snd type waveaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="e12cd-148">Na interface de cadeia de caracteres de comando, você também pode abreviar a especificação do nome do dispositivo usando o formato de ponto de exclamação alternativo, conforme documentado com o comando [**abrir**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="e12cd-148">In the command-string interface, you can also abbreviate the device name specification by using the alternative exclamation-point format, as documented with the [**open**](open.md) command.</span></span>

## <a name="opening-a-device-using-the-filename-extension"></a><span data-ttu-id="e12cd-149">Abrindo um dispositivo usando a extensão de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="e12cd-149">Opening a Device Using the Filename Extension</span></span>

<span data-ttu-id="e12cd-150">Se o comando [**abrir**](open.md) ([**MCI \_ aberto**](mci-open.md)) especificar apenas o nome do arquivo, o MCI usará a extensão de nome de arquivo para selecionar o dispositivo apropriado na lista no registro ou na \[ seção de extensões MCI \] do arquivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="e12cd-150">If the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command specifies only the filename, MCI uses the filename extension to select the appropriate device from the list in the registry or the \[mci extensions\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="e12cd-151">As entradas na \[ seção de extensões MCI \] usam o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="e12cd-151">The entries in the \[mci extensions\] section use the following form:</span></span>

<span data-ttu-id="e12cd-152">nome do dispositivo de *\_ extensão de nome de arquivo*  =  *\_*</span><span class="sxs-lookup"><span data-stu-id="e12cd-152">*filename\_extension* = *device\_name*</span></span>

<span data-ttu-id="e12cd-153">O MCI usa implicitamente o *\_ nome do dispositivo* se a extensão for encontrada e se um nome de dispositivo não tiver sido especificado no comando **Open** .</span><span class="sxs-lookup"><span data-stu-id="e12cd-153">MCI implicitly uses *device\_name* if the extension is found and if a device name has not been specified in the **open** command.</span></span>

<span data-ttu-id="e12cd-154">O exemplo a seguir mostra uma \[ seção típica de extensões MCI \] :</span><span class="sxs-lookup"><span data-stu-id="e12cd-154">The following example shows a typical \[mci extensions\] section:</span></span>


```C++
[mci extensions]
wav=waveaudio
mid=sequencer
rmi=sequencer
```



<span data-ttu-id="e12cd-155">Usando essas definições, o MCI abrirá o dispositivo **WaveAudio** se o seguinte comando for emitido:</span><span class="sxs-lookup"><span data-stu-id="e12cd-155">Using these definitions, MCI opens the **waveaudio** device if the following command is issued:</span></span>


```C++
mciSendString("open train.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="new-data-files"></a><span data-ttu-id="e12cd-156">Novos arquivos de dados</span><span class="sxs-lookup"><span data-stu-id="e12cd-156">New Data Files</span></span>

<span data-ttu-id="e12cd-157">Para criar um novo arquivo de dados, basta especificar um nome de arquivo em branco.</span><span class="sxs-lookup"><span data-stu-id="e12cd-157">To create a new data file, simply specify a blank filename.</span></span> <span data-ttu-id="e12cd-158">O MCI não salva um novo arquivo até que você o salve usando o comando [**salvar**](save.md) ([**\_ salvar como MCI**](mci-save.md)).</span><span class="sxs-lookup"><span data-stu-id="e12cd-158">MCI does not save a new file until you save it by using the [**save**](save.md) ([**MCI\_SAVE**](mci-save.md)) command.</span></span> <span data-ttu-id="e12cd-159">Ao criar um novo arquivo, você deve incluir um alias de dispositivo com o comando [**abrir**](open.md) ([**MCI \_ aberto**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="e12cd-159">When creating a new file, you must include a device alias with the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="e12cd-160">O exemplo a seguir abre um novo arquivo **WaveAudio** , inicia e interrompe a gravação e, em seguida, salva e fecha o arquivo:</span><span class="sxs-lookup"><span data-stu-id="e12cd-160">The following example opens a new **waveaudio** file, starts and stops recording, then saves and closes the file:</span></span>


```C++
mciSendString("open new type waveaudio alias capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("record capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("stop capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("save capture orca.wav", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close capture", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



## <a name="sharable-devices"></a><span data-ttu-id="e12cd-161">Dispositivos compartilháveis</span><span class="sxs-lookup"><span data-stu-id="e12cd-161">Sharable Devices</span></span>

<span data-ttu-id="e12cd-162">O sinalizador "compartilhável" (MCI \_ Open \_ Shareable) do comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) permite que vários aplicativos acessem o mesmo dispositivo (ou arquivo) e instância de dispositivo simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="e12cd-162">The "sharable" (MCI\_OPEN\_SHAREABLE) flag of the [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command lets multiple applications access the same device (or file) and device instance simultaneously.</span></span> <span data-ttu-id="e12cd-163">Se seu aplicativo abrir um dispositivo ou arquivo como compartilhável, outros aplicativos também poderão acessá-lo, abrindo-o como compartilhável.</span><span class="sxs-lookup"><span data-stu-id="e12cd-163">If your application opens a device or file as sharable, other applications can also access it by opening it as sharable.</span></span> <span data-ttu-id="e12cd-164">O dispositivo ou arquivo compartilhado fornece a cada aplicativo a capacidade de alterar os parâmetros que regem seu estado operacional.</span><span class="sxs-lookup"><span data-stu-id="e12cd-164">The shared device or file gives each application the ability to change the parameters governing its operating state.</span></span> <span data-ttu-id="e12cd-165">Cada vez que um dispositivo ou arquivo é aberto como compartilhável, o MCI retorna um identificador de dispositivo exclusivo, embora os identificadores façam referência à mesma instância.</span><span class="sxs-lookup"><span data-stu-id="e12cd-165">Each time a device or file is opened as sharable, MCI returns a unique device identifier, even though the identifiers refer to the same instance.</span></span>

<span data-ttu-id="e12cd-166">Se seu aplicativo abrir um dispositivo ou arquivo sem especificar que ele é compartilhável, nenhum outro aplicativo poderá acessá-lo até que seu aplicativo o feche.</span><span class="sxs-lookup"><span data-stu-id="e12cd-166">If your application opens a device or file without specifying that it is sharable, no other application can access it until your application closes it.</span></span> <span data-ttu-id="e12cd-167">Além disso, se um dispositivo der suporte a apenas uma instância aberta, o comando **abrir** falhará se você especificar o sinalizador compartilhável.</span><span class="sxs-lookup"><span data-stu-id="e12cd-167">Also, if a device supports only one open instance, the **open** command will fail if you specify the sharable flag.</span></span>

<span data-ttu-id="e12cd-168">Se seu aplicativo abrir um dispositivo e especificar que ele pode ser compartilhado, seu aplicativo não deverá fazer suposições sobre o estado desse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-168">If your application opens a device and specifies that it is sharable, your application should not make any assumptions about the state of this device.</span></span> <span data-ttu-id="e12cd-169">Seu aplicativo pode precisar compensar as alterações feitas por outros aplicativos que acessam o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-169">Your application might need to compensate for changes made by other applications accessing the device.</span></span>

<span data-ttu-id="e12cd-170">A maioria dos arquivos compostos não é compartilhável; no entanto, você pode abrir vários arquivos ou pode abrir um único arquivo várias vezes.</span><span class="sxs-lookup"><span data-stu-id="e12cd-170">Most compound files are not sharable; however, you can open multiple files, or you can open a single file multiple times.</span></span> <span data-ttu-id="e12cd-171">Se você abrir um único arquivo várias vezes, o MCI criará uma instância independente para cada uma, com cada instância com um status operacional exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-171">If you open a single file multiple times, MCI creates an independent instance for each, with each instance having a unique operating status.</span></span>

<span data-ttu-id="e12cd-172">Se você abrir várias instâncias de um arquivo, deverá atribuir um identificador de dispositivo exclusivo a cada uma.</span><span class="sxs-lookup"><span data-stu-id="e12cd-172">If you open multiple instances of a file, you must assign a unique device identifier to each.</span></span> <span data-ttu-id="e12cd-173">Você pode usar um alias, conforme descrito na seção a seguir, para atribuir um nome exclusivo para cada arquivo.</span><span class="sxs-lookup"><span data-stu-id="e12cd-173">You can use an alias, as described in the following section, to assign a unique name for each file.</span></span>

 

 