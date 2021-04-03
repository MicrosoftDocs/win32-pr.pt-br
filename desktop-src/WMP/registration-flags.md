---
title: Sinalizadores de registro
description: Sinalizadores de registro
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Plug-ins do Windows Media Player, sinalizadores de registro
- plug-ins, sinalizadores de registro
- plug-ins de interface do usuário, sinalizadores de registro
- Plug-ins de interface do usuário, sinalizadores de registro
- sinalizadores, plug-ins de interface do usuário
- registro, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007123"
---
# <a name="registration-flags"></a>Sinalizadores de registro

Quando o assistente de plug-in do Windows Media Player cria um novo projeto de plug-in de interface do usuário, ele cria uma chave no registro que contém informações sobre o plug-in. Essa chave é criada no seguinte local:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassID* é a ID de classe do plug-in.

Essa chave inclui os valores a seguir.



| Nome                     | Tipo       | Descrição                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funcionalidades             | REG \_ DWORD | Um valor DWORD que consiste em pelo menos um sinalizador de tipo de plug-in que pode ser combinado com um ou mais sinalizadores de recursos de plug-in usando binary ou operações.                             |
| Descrição              | REG \_ sz    | Uma cadeia de caracteres que contém a descrição do plug-in. O assistente de plug-in cria um recurso de cadeia de caracteres e fornece a URL do recurso (usando o protocolo res) para esse valor.         |
| FriendlyName             | REG \_ sz    | Uma cadeia de caracteres que contém o nome legível pelo usuário para o plug-in. O assistente de plug-in cria um recurso de cadeia de caracteres e fornece a URL do recurso (usando o protocolo res) para esse valor. |
| UninstallPath (opcional) | REG \_ sz    | Uma cadeia de caracteres que contém o caminho para um arquivo executável que desinstala o plug-in.                                                                                                        |



 

Para obter mais informações sobre o protocolo res, consulte o SDK de desenvolvimento da Internet.

A tabela a seguir detalha os sinalizadores de tipo de plug-in.



| Sinalizador de tipo de plug-in                | Valor | Descrição                                       |
|----------------------------------|-------|---------------------------------------------------|
| **plano de fundo do \_ tipo de plugin \_**     | 0x1   | O plug-in da IU não exibe uma interface do usuário. |
| **tipo de plug-in \_ \_ SEPARATEWINDOW** | 0x2   | O plug-in da interface do usuário é um plug-in de janela separado.      |
| **tipo de plug-in \_ \_ DISPLAYAREA**    | 0x3   | O plug-in da interface do usuário é um plug-in de área de exibição.         |
| **tipo de plug-in \_ \_ SETTINGSAREA**   | 0x4   | O plug-in da interface do usuário é um plug-in de área de configurações.        |
| **tipo de plug-in \_ \_ METADATAAREA**   | 0x5   | O plug-in da interface do usuário é um plug-in de área de metadados.        |



 

A tabela a seguir detalha os sinalizadores de recursos de plug-in.



| Sinalizador de recursos de plug-in             | Valor      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sinalizadores de plug-in \_ \_ ACCEPTSMEDIA**       | 0x10000000 | O plug-in da interface do usuário pode aceitar matrizes de ponteiro de objeto de **mídia** quando o Windows Media Player chama [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                           |
| **sinalizadores de plug-in \_ \_ ACCEPTSPLAYLISTS**   | 0x8000000  | O plug-in da interface do usuário pode aceitar matrizes de ponteiro de objeto de **lista de reprodução** quando o Windows Media Player chama [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                        |
| **sinalizadores de plug-in \_ \_ HASPRESETS**         | 0x4000000  | O plug-in da interface do usuário usa predefinições. Se o plug-in especificar esse sinalizador, o Windows Media Player consultará o plug-in para obter informações predefinidas chamando [**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .                                                                                                                                                                                                      |
| **sinalizadores de plug-in \_ \_ HASPROPERTYPAGE**    | 0x80000000 | O plug-in da interface do usuário fornece uma caixa de diálogo de página de propriedades. O Windows Media Player chamará [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) se esse sinalizador for definido quando a página de Propriedades for chamada.                                                                                                                                                                                                 |
| **sinalizadores de plug-in \_ \_ ocultos**             | 0x02000000 | O plug-in da interface do usuário em segundo plano não aparece no menu **plug-ins** que é acessado por meio dos menus **Exibir** ou **ferramentas** ou o botão **selecionar opções em execução** agora está em execução. Ela aparece na guia **plug-ins** da caixa de diálogo opções. Isso faz com que o ícone de execução de plug-in em segundo plano apareça na barra de status. Esse sinalizador não tem efeito sobre plug-ins diferentes de plug-ins de interface do usuário em segundo plano.<br/> |
| **sinalizadores de plug-in \_ \_ INSTALLAUTORUN**     | 0x40000000 | O Windows Media Player executa o plug-in da interface do usuário automaticamente quando o plug-in é instalado.                                                                                                                                                                                                                                                                                                                               |
| **sinalizadores de plug-in \_ \_ LAUNCHPROPERTYPAGE** | 0x20000000 | O Windows Media Player chama [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) quando o plug-in da interface do usuário é executado pela primeira vez. Se esse sinalizador for especificado, **os \_ sinalizadores \_ de plug-in HASPROPERTYPAGE** também deverão ser especificados.<br/>                                                                                                                                                             |



 

As constantes a seguir são definidas em wmpplug. h. Não altere os valores associados a essas constantes.



| Nome                                    | Descrição                               |
|-----------------------------------------|-------------------------------------------|
| **INSTALLREGKEY do plug-in \_**               | O local da chave do registro de plug-in. |
| **PLUGIN \_ INSTALLREGKEY \_ amigável** | O nome do valor de nome amigável.      |
| **Descrição do plug-in \_ INSTALLREGKEY \_**  | O nome do valor da descrição.        |
| **\_recursos de INSTALLREGKEY do plug-in \_** | O nome do valor de recursos.       |
| **desinstalação do PLUGIN \_ INSTALLREGKEY \_**    | O nome do valor do caminho de desinstalação.     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Referência de programação de plug-ins de interface do usuário**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





