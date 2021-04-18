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
# <a name="dvc-plug-in-registration"></a>Registro de plug-in do DVC

O plug-in de DVC (canal virtual dinâmico) é registrado para uso pelo cliente de Conexão de Área de Trabalho Remota (RDC) usando um dos seguintes métodos:

-   Invocar o método [**IMsTscAdvancedSettings::p UT \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) do controle ActiveX protocolo RDP (RDP). Várias entradas devem ser separadas por vírgula.
-   Gravando a entrada de plug-in no seguinte local no registro no computador em que o processo de cliente de Conexão de Área de Trabalho Remota (RDC) é iniciado:

    **HKEY \_ Software \_ atual** \\  \\ **do usuário Microsoft** \\ **Terminal Server cliente** \\  \\ **suplementos** padrão \\ ***nome do plug-in exclusivo***

    > [!Note]  
    > Você deve criar a subchave de *nome de plug-in exclusivo* se ela não existir. O nome de subchave de *nome de plug-in exclusivo* é uma cadeia de caracteres arbitrária que pode identificar o plug-in. A cadeia de caracteres pode ser qualquer combinação de caracteres.

     

    Em *nome de plug-in exclusivo*, você deve adicionar uma entrada que identifique o plug-in.

    Nome da entrada = **nome**

    Tipo de dados = **reg \_ sz** ou **reg \_ Expand \_ sz**

Em ambos os casos, o valor de entrada deve estar de acordo com um dos seguintes formatos:

<dl> <dt>

<span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-indllname*: {*CLSID*}"
</dt> <dd>

O plug-in não está necessariamente registrado no registro do Windows como um objeto de Component Object Model (COM), mas a DLL é implementada como um objeto COM em processo. O cliente RDC carregará a DLL especificada pelo *plug-indllname* e recuperará o objeto com diretamente usando *CLSID*.

</dd> <dt>

<span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-indllname*"
</dt> <dd>

A DLL implementa a função [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) e a exporta por nome. O cliente RDC usará a função **VirtualChannelGetInstance** para obter ponteiros de interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos os plug-ins implementados pela dll.

</dd> <dt>

<span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"
</dt> <dd>

O cliente RDC criará uma instância do plug-in como um objeto COM normal usando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com o *CLSID*.

</dd> </dl>

> [!Note]  
> O *plug-indllname* representa o caminho completo e o nome do arquivo. dll. Se o tipo de dados for **reg \_ Expand \_ sz**, o caminho poderá conter variáveis de ambiente não expandidas que são expandidas no tempo de execução.

 

Quando o cliente de Conexão de Área de Trabalho Remota (RDC) concluir sua inicialização, ele executará o seguinte para cada plug-in registrado:

1.  Obtenha uma instância da interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para cada plug-in usando um dos métodos descritos acima.
2.  Chame o método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) de cada interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .
3.  Se o cliente se conecta várias vezes ao mesmo ou a um servidor diferente, pode haver várias chamadas para os métodos [**conectados**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) e [**desconectados**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) .
4.  A última chamada que o plug-in deve tratar é [**encerrada**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated). É um sinal de que o cliente de Conexão de Área de Trabalho Remota (RDC) está prestes a descarregar o plug-in.

 

 