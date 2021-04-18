---
title: Registro de plug-in do DVC
description: Descreve a sintaxe para a entrada de plug-in de canal virtual dinâmico (DVC) para o cliente de Conexão de Área de Trabalho Remota (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810106"
---
# <a name="dvc-plug-in-registration"></a><span data-ttu-id="47cab-103">Registro de plug-in do DVC</span><span class="sxs-lookup"><span data-stu-id="47cab-103">DVC plug-in registration</span></span>

<span data-ttu-id="47cab-104">O plug-in de DVC (canal virtual dinâmico) é registrado para uso pelo cliente de Conexão de Área de Trabalho Remota (RDC) usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="47cab-104">The dynamic virtual channel (DVC) plug-in is registered for use by the Remote Desktop Connection (RDC) client using one of the following methods:</span></span>

-   <span data-ttu-id="47cab-105">Invocar o método [**IMsTscAdvancedSettings::p UT \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) do controle ActiveX protocolo RDP (RDP).</span><span class="sxs-lookup"><span data-stu-id="47cab-105">Invoking the [**IMsTscAdvancedSettings::put\_PluginDlls**](imstscadvancedsettings-plugindlls.md) method of the Remote Desktop Protocol (RDP) ActiveX control.</span></span> <span data-ttu-id="47cab-106">Várias entradas devem ser separadas por vírgula.</span><span class="sxs-lookup"><span data-stu-id="47cab-106">Multiple entries must be comma separated.</span></span>
-   <span data-ttu-id="47cab-107">Gravando a entrada de plug-in no seguinte local no registro no computador em que o processo de cliente de Conexão de Área de Trabalho Remota (RDC) é iniciado:</span><span class="sxs-lookup"><span data-stu-id="47cab-107">Writing the plug-in entry to the following location in the registry on the computer where the Remote Desktop Connection (RDC) client process is started:</span></span>

    <span data-ttu-id="47cab-108">**HKEY \_ Software \_ atual** \\  \\ **do usuário Microsoft** \\ **Terminal Server cliente** \\  \\ **suplementos** padrão \\ ***nome do plug-in exclusivo***</span><span class="sxs-lookup"><span data-stu-id="47cab-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**AddIns**\\***unique plug-in name***</span></span>

    > [!Note]  
    > <span data-ttu-id="47cab-109">Você deve criar a subchave de *nome de plug-in exclusivo* se ela não existir.</span><span class="sxs-lookup"><span data-stu-id="47cab-109">You must create the *unique plug-in name* subkey if it does not exist.</span></span> <span data-ttu-id="47cab-110">O nome de subchave de *nome de plug-in exclusivo* é uma cadeia de caracteres arbitrária que pode identificar o plug-in.</span><span class="sxs-lookup"><span data-stu-id="47cab-110">The *unique plug-in name* subkey name is an arbitrary string that can identify the plug-in.</span></span> <span data-ttu-id="47cab-111">A cadeia de caracteres pode ser qualquer combinação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="47cab-111">The string can be any combination of characters.</span></span>

     

    <span data-ttu-id="47cab-112">Em *nome de plug-in exclusivo*, você deve adicionar uma entrada que identifique o plug-in.</span><span class="sxs-lookup"><span data-stu-id="47cab-112">Under *unique plug-in name*, you must add an entry that identifies the plug-in.</span></span>

    <span data-ttu-id="47cab-113">Nome da entrada = **nome**</span><span class="sxs-lookup"><span data-stu-id="47cab-113">Entry name = **Name**</span></span>

    <span data-ttu-id="47cab-114">Tipo de dados = **reg \_ sz** ou **reg \_ Expand \_ sz**</span><span class="sxs-lookup"><span data-stu-id="47cab-114">Data type = **REG\_SZ** or **REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="47cab-115">Em ambos os casos, o valor de entrada deve estar de acordo com um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="47cab-115">In both cases, the entry value must conform to one of the following formats:</span></span>

<dl> <dt>

<span data-ttu-id="47cab-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-indllname*: {*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="47cab-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="47cab-117">O plug-in não está necessariamente registrado no registro do Windows como um objeto de Component Object Model (COM), mas a DLL é implementada como um objeto COM em processo.</span><span class="sxs-lookup"><span data-stu-id="47cab-117">The plug-in is not necessarily registered in the Windows registry as a Component Object Model (COM) object, but the DLL is implemented as an in-process COM object.</span></span> <span data-ttu-id="47cab-118">O cliente RDC carregará a DLL especificada pelo *plug-indllname* e recuperará o objeto com diretamente usando *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="47cab-118">The RDC client will load the DLL specified by *Plug-inDLLName* and retrieve the COM object directly using *CLSID*.</span></span>

</dd> <dt>

<span data-ttu-id="47cab-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-indllname*"</span><span class="sxs-lookup"><span data-stu-id="47cab-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span></span>
</dt> <dd>

<span data-ttu-id="47cab-120">A DLL implementa a função [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) e a exporta por nome.</span><span class="sxs-lookup"><span data-stu-id="47cab-120">The DLL implements the [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) function and exports it by name.</span></span> <span data-ttu-id="47cab-121">O cliente RDC usará a função **VirtualChannelGetInstance** para obter ponteiros de interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos os plug-ins implementados pela dll.</span><span class="sxs-lookup"><span data-stu-id="47cab-121">The RDC client will use the **VirtualChannelGetInstance** function to obtain [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface pointers for all of the plug-ins implemented by the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="47cab-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span><span class="sxs-lookup"><span data-stu-id="47cab-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="47cab-123">O cliente RDC criará uma instância do plug-in como um objeto COM normal usando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com o *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="47cab-123">The RDC client will instantiate the plug-in as a regular COM object using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with the *CLSID*.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="47cab-124">O *plug-indllname* representa o caminho completo e o nome do arquivo. dll.</span><span class="sxs-lookup"><span data-stu-id="47cab-124">*Plug-inDLLName* represents the full path and file name of the .dll file.</span></span> <span data-ttu-id="47cab-125">Se o tipo de dados for **reg \_ Expand \_ sz**, o caminho poderá conter variáveis de ambiente não expandidas que são expandidas no tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="47cab-125">If the data type is **REG\_EXPAND\_SZ**, the path can contain unexpanded environment variables that are expanded at runtime.</span></span>

 

<span data-ttu-id="47cab-126">Quando o cliente de Conexão de Área de Trabalho Remota (RDC) concluir sua inicialização, ele executará o seguinte para cada plug-in registrado:</span><span class="sxs-lookup"><span data-stu-id="47cab-126">When the Remote Desktop Connection (RDC) client finishes its initialization, it will perform the following for every registered plug-in:</span></span>

1.  <span data-ttu-id="47cab-127">Obtenha uma instância da interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para cada plug-in usando um dos métodos descritos acima.</span><span class="sxs-lookup"><span data-stu-id="47cab-127">Obtain an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for each plug-in using one of the methods described above.</span></span>
2.  <span data-ttu-id="47cab-128">Chame o método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) de cada interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .</span><span class="sxs-lookup"><span data-stu-id="47cab-128">Call the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of each [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface.</span></span>
3.  <span data-ttu-id="47cab-129">Se o cliente se conecta várias vezes ao mesmo ou a um servidor diferente, pode haver várias chamadas para os métodos [**conectados**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) e [**desconectados**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) .</span><span class="sxs-lookup"><span data-stu-id="47cab-129">If the client connects multiple times to the same or to a different server, there may be multiple calls to the [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) and [**Disconnected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) methods.</span></span>
4.  <span data-ttu-id="47cab-130">A última chamada que o plug-in deve tratar é [**encerrada**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span><span class="sxs-lookup"><span data-stu-id="47cab-130">The last call that the plug-in should handle is [**Terminated**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span></span> <span data-ttu-id="47cab-131">É um sinal de que o cliente de Conexão de Área de Trabalho Remota (RDC) está prestes a descarregar o plug-in.</span><span class="sxs-lookup"><span data-stu-id="47cab-131">It is a signal that the Remote Desktop Connection (RDC) client is about to unload the plug-in.</span></span>

 

 