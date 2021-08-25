---
title: Sinalizadores de registro
description: Sinalizadores de registro
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Windows Media Player plug-ins, sinalizadores de registro
- plug-ins, sinalizadores de registro
- plug-ins de interface do usuário, sinalizadores de registro
- Plug-ins de interface do usuário, sinalizadores de registro
- sinalizadores, plug-ins de interface do usuário
- registro, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbd34ed98236f8a02c936d52b092b82be60b986fb7b16edce1f3b1cbb91d6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002806"
---
# <a name="registration-flags"></a>Sinalizadores de registro

Quando o Windows Media Player de Plug-in cria um novo projeto de plug-in de interface do usuário, ele cria uma chave no Registro que contém informações sobre o plug-in. Essa chave é criada no seguinte local:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassId* é a ID de classe do plug-in.

Essa chave inclui os valores a seguir.



| Nome                     | Tipo       | Descrição                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funcionalidades             | REG \_ DWORD | Um valor DWORD que consiste em pelo menos um sinalizador de tipo de plug-in que pode ser combinado com um ou mais sinalizadores de funcionalidades de plug-in usando operações OR binárias.                             |
| Descrição              | REG \_ SZ    | Uma cadeia de caracteres que contém a descrição do plug-in. O assistente de plug-in cria um recurso de cadeia de caracteres e fornece a URL do recurso (usando o protocolo res) para esse valor.         |
| FriendlyName             | REG \_ SZ    | Uma cadeia de caracteres que contém o nome acessível pelo usuário para o plug-in. O assistente de plug-in cria um recurso de cadeia de caracteres e fornece a URL do recurso (usando o protocolo res) para esse valor. |
| UninstallPath (opcional) | REG \_ SZ    | Uma cadeia de caracteres que contém o caminho para um arquivo executável que desinstala o plug-in.                                                                                                        |



 

Para obter mais informações sobre o protocolo res, consulte o SDK de Desenvolvimento na Internet.

A tabela a seguir detalha os sinalizadores de tipo de plug-in.



| Sinalizador de tipo de plug-in                | Valor | Descrição                                       |
|----------------------------------|-------|---------------------------------------------------|
| **PLANO DE \_ FUNDO DO TIPO DE \_ PLUG-IN**     | 0x1   | O plug-in da interface do usuário não exibe uma interface do usuário. |
| **TIPO \_ DE \_ PLUG-IN SEPARATEWINDOW** | 0x2   | O plug-in da interface do usuário é um plug-in de janela separado.      |
| **\_DISPLAYAREA DO TIPO DE \_ PLUG-IN**    | 0x3   | O plug-in da interface do usuário é um plug-in de área de exibição.         |
| **CONFIGURAÇÕES \_ \_ DE TIPO DE PLUG-INAREA**   | 0x4   | O plug-in da interface do usuário é um plug-in de área de configurações.        |
| **TIPO \_ DE \_ PLUG-IN METADATAAREA**   | 0x5   | O plug-in da interface do usuário é um plug-in de área de metadados.        |



 

A tabela a seguir detalha os sinalizadores de funcionalidades de plug-in.



| Sinalizador de funcionalidades de plug-in             | Valor      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SINALIZADORES \_ DE \_ PLUG-IN ACCEPTSMEDIA**       | 0x10000000 | O plug-in da  interface do usuário pode aceitar matrizes de ponteiro de objeto de mídia quando Windows Media Player [**chama IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                           |
| **SINALIZADORES \_ DE \_ PLUG-IN ACCEPTSPLAYLISTS**   | 0x8000000  | O plug-in da interface do usuário pode aceitar **matrizes** de ponteiro de objeto playlist quando Windows Media Player chama [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                        |
| **SINALIZADORES \_ DE \_ PLUG-IN HASPRESETS**         | 0x4000000  | O plug-in da interface do usuário usa predefinições. Se o plug-in especificar esse sinalizador, Windows Media Player consultará o plug-in para obter informações predefinidas chamando [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .                                                                                                                                                                                                      |
| **SINALIZADORES \_ DE \_ PLUG-IN HASPROPERTYPAGE**    | 0x80000000 | O plug-in da interface do usuário fornece uma caixa de diálogo de página de propriedades. Windows Media Player [**chamará IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) se esse sinalizador for definido quando a página de propriedades for invocada.                                                                                                                                                                                                 |
| **SINALIZADORES \_ DE \_ PLUG-IN OCULTOS**             | 0x02000000 | O plug-in da interface do usuário em segundo plano não  aparece no menu **Plug-ins** acessado nos **menus** Exibir ou Ferramentas ou no botão Selecionar Opções Agora Em Reprodução.  Ele aparece na guia **Plug-ins** da caixa de diálogo Opções. Isso faz com que o ícone de Execução do Plug-in em Segundo Plano apareça na barra de status. Esse sinalizador não tem nenhum efeito em plug-ins diferentes dos plug-ins da interface do usuário em segundo plano.<br/> |
| **SINALIZADORES \_ DE \_ PLUG-IN INSTALLAUTORUN**     | 0x40000000 | Windows Media Player executa o plug-in da interface do usuário automaticamente quando o plug-in é instalado.                                                                                                                                                                                                                                                                                                                               |
| **SINALIZADORES \_ DE \_ PLUG-IN LAUNCHPROPERTYPAGE** | 0x20000000 | Windows Media Player chama [**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) quando o plug-in da interface do usuário é executado pela primeira vez. Se esse sinalizador for especificado, **OS \_ SINALIZADORES DE \_ PLUG-IN HASPROPERTYPAGE** também deverão ser especificados.<br/>                                                                                                                                                             |



 

As constantes a seguir são definidas em wmpplug.h. Não altere os valores associados a essas constantes.



| Nome                                    | Descrição                               |
|-----------------------------------------|-------------------------------------------|
| **\_PLUG-IN INSTALLREGKEY**               | O local da chave do Registro de plug-in. |
| **PLUGIN \_ INSTALLREGKEY \_ FRIENDLYNAME** | O nome do valor de nome amigável.      |
| **\_PLUG-IN INSTALLREGKEY \_ DESCRIPTION**  | O nome do valor de descrição.        |
| **\_PLUG-IN \_ INSTALLREGKEY CAPABILITIES** | O nome do valor das funcionalidades.       |
| **\_PLUG-IN INSTALLREGKEY \_ UNINSTALL**    | O nome do valor do caminho de desinstalação.     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Interface do Usuário de programação de plug-ins do Interface do Usuário**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





